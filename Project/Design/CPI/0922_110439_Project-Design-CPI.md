# **CPI Module**

# 1. Introduction

Cargo Protein Injection (CPI) is a protein delivery module in SUNRISE designed to inject an Adaptor that induces the degradation of resistance proteins into target drug-resistant bacteria. In CPI, a protein complex-based protein injector specifically recognizes and binds to surface structures of the target bacterium and subsequently injects the Adaptor loaded inside the injector into the cell. By making both the target-recognition region and the loaded protein exchangeable, we designed CPI as a module capable of delivering diverse proteins to target drug-resistant bacteria.

:::c

**Fig. 1. Overview of the CPI module in SUNRISE**

:::

# 2. Background

For TPD to function inside the target bacterium, the Adaptor must be delivered into the bacterial cytoplasm. Furthermore, through discussions with experts, we considered that, from a safety perspective and with future in vivo administration and environmental impact in mind, it would be preferable to deliver the protein-based Adaptor itself directly to the target bacterium rather than introducing a gene.  
We therefore focused on the **Photorhabdus Virulence Cassette (PVC)**, which can directly inject proteins into target cells.

PVC is a type of **extracellular contractile injection system (eCIS)** found in entomopathogenic bacteria of the genus *Photorhabdus* [^1][^2][^3]. It is a protein complex structurally similar to the contractile tail of a bacteriophage and can carry protein payloads inside. PVC functions as an extracellular, independent particle, and binding to the target cell surface is thought to trigger sheath contraction, which drives the inner tube and spike toward the target cell to deliver the payload [^2][^3][^4]. In addition, the mechanism by which PVC recognizes target cells can be engineered. Kreitz et al. showed that the target cell specificity of PVC can be altered by replacing the C-terminal region of Pvc13 involved in target recognition with different binding domains [^3]. Using this strategy, retargeting and protein delivery to human cells and mouse tissues distinct from the native targets were demonstrated.

Below, we describe in detail the structure of PVC, which served as the basis of CPI, its mechanisms of target recognition and injection, and its payload-loading mechanism.

:::details What Is PVC?

PVC is an eCIS found in the genus *Photorhabdus* and has a structure similar to the contractile tail of a bacteriophage [^1][^2][^3][^4]. In the *P. asymbiotica* PVC*pnf* system used for CPI, 16 core genes (*pvc1–pvc16*) required for assembly of functional particles are encoded within a region of approximately 20 kb [^3]. Downstream of these genes, endogenous payloads such as Pdp1 and Pnf are encoded. PVC particles consist of components including a tail fiber involved in interactions with the target cell surface, a baseplate that transmits structural changes, a contractile sheath, an inner tube that accommodates the payload, and a spike involved in penetration of the target cell surface [^3][^4]. Structural analysis of *P. asymbiotica* PVC reported a sheath–tube trunk length of approximately 117 nm [^7]. In contrast, extended particles of PlPVC1 from *P. luminescens* have an average length of approximately 280 nm, indicating that particle length and structure vary among different PVC systems [^4]. In addition, endogenous payloads Pdp1 and Pnf are retained inside the inner tube of *P. asymbiotica* PVC and delivered to target cells [^2][^5].

:::c

**Fig. 2. Overall structure of the PVC particle**

:::



:::details Target Recognition and Injection

In PVC, the tail fiber Pvc13 plays an important role in interactions with target cells [^3]. Kreitz et al. identified residues 403–476 at the C-terminal region of Pvc13 as a putative target recognition domain and demonstrated that PVC target specificity can be altered by replacing this region with different binding domains [^3]. For example, introducing the trimeric knob domain of human adenovirus type 5 (Ad5) or the epidermal growth factor receptor (EGFR)-binding designed ankyrin repeat protein (DARPin) E01 into Pvc13 enabled binding and payload delivery to specific human cells [^3]. Although the detailed firing mechanism following target recognition remains under investigation, a model is supported in which structural changes in the baseplate associated with target recognition by the tail fiber are transmitted to the sheath, and sheath contraction drives the inner tube and spike toward the target cell [^4]. Importantly, **the tail fiber responsible for target recognition and the contractile injection machinery responsible for physically penetrating the cell surface and delivering the payload are structurally separated**. This enables the delivery destination to be changed by modifying the target-recognition region of Pvc13 while retaining the basic injection machinery of PVC.

:::c

**Fig. 3. Retargeting of Pvc13 by replacement of the C-terminal targeting domain**

:::



:::details Payload Loading

In PVC, endogenous payloads are loaded into the particle while being retained within the lumen of the inner tube. In *P. asymbiotica* PVC, Pdp1, a dNTP pyrophosphatase, and Pnf, a deamidase, have been reported to be retained inside the inner tube in a “Peas in the Pod” arrangement [^5]. The N-terminal region of the payload is important for payload loading. Jiang et al. showed that the N-terminal sequences of Pdp1 and Pnf are important for payload loading into PVC and that fusion of these sequences to heterologous proteins allows the heterologous proteins to be loaded into PVC [^6].  
Kreitz et al. also showed that intrinsically disordered regions at the N termini of Pdp1 and Pnf function as packaging domains [^3]. By fusing these regions to GFP, Cre recombinase, zinc finger nuclease, and other proteins, non-native payloads were successfully loaded into PVC and delivered to target cells. Thus, in PVC, **heterologous proteins can be loaded as payloads by fusing an N-terminal packaging domain to the protein of interest**. In this project, we use the N-terminal region of Pdp1 (Pdp1_NTD) as the payload-loading signal.

:::c

**Fig. 4. Cargo packaging using Pdp1_NTD**

:::



As described above, PVC enables the separate engineering of target recognition, protein injection, and payload loading. In addition, rather than producing the protein of interest inside the target cell through gene expression, PVC can directly deliver the protein itself as a payload. This modularity is well suited to the purpose of CPI, which is to deliver the desired Adaptor into target bacteria. We therefore adopted PVC as the basis of the CPI module.

However, programmable protein delivery using PVC, including the PVC*pnf* system used as the basis of our design, has primarily been validated in eukaryotic cells [^3]. Therefore, to apply CPI to *E. coli*, additional design and validation are required for bacterial target recognition and for payload delivery across the prokaryotic cell envelope. We therefore selected drug-resistant *E. coli* as the target and designed modifications to the tail fiber for selective binding to *E. coli*, evaluated the feasibility of injection across the prokaryotic cell surface, and constructed a receptor-binding protein (RBP) library to enable targeting of diverse bacterial strains.

:::c

**Fig. 5. From PVC to the SUNRISE CPI module**

:::

&nbsp;

# 3. Design of the CPI Module

## 3.1 Components of the CPI Module

CPI consists of the following three components.

:::c

**Table. 1. Components of the CPI module**

:::

| Component | Function | Design | Parts |
| ----- | ----- | ----- | ----- |
| Targeting system | Recognizes the target bacterium and binds CPI to the cell surface | Introduces a bacteria-specific RBP into Pvc13 |  |
| Injection system | Penetrates the cell surface and delivers the payload into the cell | Uses the basic injection machinery derived from PVC |  |
| Payload | Protein to be delivered into the cell | Fuses Pdp1_NTD to TPD and loads it into PVC |  |

We designed CPI so that the basic PVC injection machinery remains as a common component while **the targeting system and payload are exchangeable**. This enables CPI to be extended to different drug-resistant bacteria and different payloads without substantially altering the core injection machinery.

:::c

**Fig. 6. Modular architecture of the CPI module**

:::

&nbsp;

## 3.2 Detailed Design

We selected drug-resistant *E. coli* as the target of CPI. Because the PVC*pnf* system underlying CPI has mainly been validated for payload delivery into eukaryotic cells, applying it to the prokaryotic cell *E. coli* requires design or validation of the targeting system, injection system, and payload. In addition, because a single RBP is likely to target only a limited range of strains, a tail-fiber design strategy is also required to extend CPI to diverse drug-resistant *E. coli* strains.

### (i) Retargeting CPI toward E. coli

To selectively bind PVC to *E. coli*, a molecule capable of recognizing the *E. coli* surface must be introduced into the tail fiber. In PVC, the C-terminal region of Pvc13 mediates interactions with target cells, and modifying this region can alter the target cell [^3].

In SUNRISE, we therefore focused on **gp17**, the tail fiber protein of bacteriophage T7, as a candidate molecule for recognizing *E. coli*. The T7 tail fiber is formed by a trimer of gp17, and its C-terminal region is involved in receptor recognition [^8]. The T7 tail fiber is known to mediate initial interactions with the lipopolysaccharide (LPS) of *E. coli*, and LPS plays an important role in host recognition by T7 [^8][^9]. We therefore aimed to retarget CPI to *E. coli* by introducing a gp17-derived receptor-binding structure into Pvc13. To position Pvc13 and gp17 appropriately, we designed multiple Pvc13–gp17 structures with different connection sites and linker configurations. For each design, the three-dimensional structure was predicted using AlphaFold 3, and structurally plausible candidates were subjected to molecular docking simulations to compare their interactions with the target. Based on this analysis, we selected a targeting structure considered capable of maintaining both binding to the *E. coli* surface and the basic structure of PVC. Details of the analysis are described on the Model page.

:::c

**Fig. 7. Design and in silico screening of the Pvc13–gp17 targeting system**

:::

&nbsp;

### (ii) Designing CPI for Injection into Prokaryotic Cells

Although PVC*pnf* has been demonstrated to deliver payloads to various eukaryotic cells following retargeting [^3], application to prokaryotic cells requires consideration of differences in cell surface structure. In Gram-negative bacteria such as *E. coli*, the payload must cross the cell envelope, which consists of the outer membrane, periplasm, peptidoglycan layer, and inner membrane, to reach the cytoplasm. Therefore, even if CPI can bind to the *E. coli* surface, it is necessary to evaluate whether the PVC inner tube and spike can sufficiently penetrate this cell envelope and deliver the payload to the cytoplasmic side.

We therefore compared the structure of the PVC inner tube and spike with the thickness of the *E. coli* cell envelope and analyzed the feasibility of membrane penetration by CPI from geometric and mechanical perspectives. Our model suggested that even when a structure and length close to those of wild-type PVC are maintained, penetration of the *E. coli* cell envelope may be possible. Based on this analysis, we adopted a design strategy in which the PVC structure involved in injection is not substantially modified and the existing PVC injection machinery is used in CPI. Details of the analysis are described on the Model page.

:::c

**Fig. 8. Geometric evaluation of CPI penetration into the** ***E. coli*** **cell envelope**

:::

&nbsp;

### (iii) Loading TPD as the Payload

The ultimate purpose of CPI is to bind to the target *E. coli* and subsequently deliver the TPD Adaptor into the cell. For the molecular design of TPD itself, see the TPD Module. To achieve this function, the desired TPD must be loaded into CPI as a payload. In PVC, the N-terminal regions of endogenous payloads are important for payload loading [^3][^6].

We therefore adopted a design in which Pdp1_NTD, the N-terminal region of Pdp1, is fused to TPD. By using Pdp1_NTD as a packaging signal, we aim to load Pdp1_NTD–TPD into PVC. In addition, considering the size of Pdp1_NTD–TPD and the internal space of the PVC inner tube, we performed simulations to estimate the amount of payload that could be loaded into a CPI particle. Detailed analyses of payload capacity and payload arrangement within CPI are described on the Model page.

:::c

**Fig. 9. Packaging TPD into CPI using Pdp1_NTD**

:::

&nbsp;

### (iv) Expanding the Target Range of CPI

Although CPI carrying gp17 is intended to enable retargeting to *E. coli*, a design based on only a single RBP may be limited to a restricted range of strains. Similar to bacteriophage host specificity, this limitation arises because molecular recognition between RBPs and bacterial surface receptors varies among strains. Surface structures such as LPS, O antigen, and outer membrane proteins differ in structure and availability among bacterial strains. In addition, even when the intended receptor is present, surrounding glycans or other structures may physically shield it and reduce RBP accessibility. We therefore constructed an **RBP library** that recognizes diverse bacterial surface structures in order to extend CPI to a wider range of drug-resistant *E. coli*.

Based on bacteriophage host-recognition mechanisms, we defined three categories of candidate CPI targets: the LPS core, outer membrane proteins, and O antigen, and compiled candidate RBPs that recognize each category. We further evaluated the binding of each RBP to its target receptor and its accessibility on the cell surface using coarse-grained molecular dynamics simulations. Through this approach, we established a design framework for selecting an appropriate RBP to introduce into CPI based on the surface structure of the target bacterium. Details of the RBP library and simulation results are described on the Model page.

:::c

**Fig. 10. RBP library for expanding the targeting range of CPI**

:::

&nbsp;

# 4. Advantages of the CPI Design

### **Extending PVC to Prokaryotic Targets**

Programmable protein delivery using PVC*pnf* has primarily been developed for eukaryotic cells. CPI integrates redesign of the targeting system, evaluation of injection feasibility across prokaryotic cell surfaces, and payload loading to establish a design framework for applying PVC to protein delivery into bacteria.

### **Protein-based**

CPI delivers the protein of interest itself directly as a payload rather than expressing a gene inside the target bacterium. This allows the TPD Adaptor to be delivered in protein form without depending on transcription or translation of foreign genes inside the target bacterium.

### **Expandable**

By designing an RBP library that accommodates diverse bacterial surface structures, we established a foundation for extending CPI beyond a single target strain to drug-resistant bacteria with different surface profiles.

### **Modular**

By making the targeting system and payload independently exchangeable, the combination of target bacterium and delivered protein can be changed. This modularity may enable future applications beyond antimicrobial resistance, including a variety of protein-delivery purposes.

# 

&nbsp;

[^1]: Yang G, Dowling AJ, Gerike U, ffrench-Constant RH, Waterfield NR. Photorhabdus virulence cassettes confer injectable insecticidal activity against the wax moth. *J Bacteriol.* 2006;188(6):2254–2261. doi:10.1128/JB.188.6.2254-2261.2006

[^2]: Vlisidou I, Hapeshi A, Healey JRJ, Smart K, Yang G, Waterfield NR. The *Photorhabdus asymbiotica* virulence cassettes deliver protein effectors directly into target eukaryotic cells. *eLife.* 2019;8:e46259. doi:10.7554/eLife.46259

[^3]: Kreitz J, Friedrich MJ, Guru A, et al. Programmable protein delivery with a bacterial contractile injection system. *Nature.* 2023;616:357–364. doi:10.1038/s41586-023-05870-7

[^4]: Marín-Arraiza L, Roa-Eguiara A, Pape T, et al. Structural characterization of an extracellular contractile injection system from *Photorhabdus luminescens* in extended and contracted states. *Nat Commun.* 2025;16:9327. doi:10.1038/s41467-025-64377-z

[^5]: Wang X, Cheng J, Shen J, et al. Characterization of Photorhabdus Virulence Cassette as a causative agent in the emerging pathogen *Photorhabdus asymbiotica*. *Sci China Life Sci.* 2022;65(3):618–630. doi:10.1007/s11427-021-1955-4

[^6]: Jiang F, Shen J, Cheng J, et al. N-terminal signal peptides facilitate the engineering of PVC complex as a potent protein delivery system. *Sci Adv.* 2022;8(17):eabm2343. doi:10.1126/sciadv.abm2343

[^7]: Jiang F, Li N, Wang X, et al. Cryo-EM structure and assembly of an extracellular contractile injection system. *Cell.* 2019;177(2):370–383.e15. doi:10.1016/j.cell.2019.02.020

[^8]: Garcia-Doval C, van Raaij MJ. Structure of the receptor-binding carboxy-terminal domain of bacteriophage T7 tail fibers. *Proc Natl Acad Sci U S A.* 2012;109(24):9390–9395. doi:10.1073/pnas.1119719109

[^9]: González-García VA, Pulido-Cid M, Garcia-Doval C, et al. Conformational changes leading to T7 DNA delivery upon interaction with the bacterial receptor. *J Biol Chem.* 2015;290(16):10038–10044. doi:10.1074/jbc.M114.614222