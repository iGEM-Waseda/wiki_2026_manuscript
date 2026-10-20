# **CPI Module**

# Introduction

Cargo Protein Injection (CPI) is a protein delivery module in SUNRISE designed to deliver an Adaptor into target drug-resistant bacteria to induce the degradation of resistance proteins. In CPI, a protein-based injector is intended to specifically recognize and bind to surface structures of the target bacterium and subsequently inject the Adaptor loaded inside the injector into the cell as a protein. We designed CPI with interchangeable targeting regions and protein payloads to support the delivery of diverse proteins to different drug-resistant bacteria. 

![overview-cpi](https://static.igem.wiki/teams/6144/wiki/description/10-19cpi.avif =500x)  
:::c

**Fig. 2.2.1.** Overview of the CPI module in SUNRISE

:::

# Background

For TPD to function inside the target bacterium, the Adaptor must be delivered into the bacterial cytoplasm. We consulted Dr. Kiga of the JIHS National Institute of Infectious Diseases, whose research focuses on novel treatments for drug-resistant bacterial infections ([**Human Practices**](https://2026.igem.wiki/waseda-tokyo/human-practices/)). Our discussions addressed safety considerations related to future in vivo administration and potential environmental impacts. On this basis, we considered direct delivery of the Adaptor protein preferable to introducing an Adaptor-encoding gene into the target bacterium. We therefore focused on the Photorhabdus Virulence Cassette (PVC), which can directly inject proteins into target cells. 

PVC is a type of extracellular contractile injection system (eCIS) found in entomopathogenic bacteria of the genus *Photorhabdus* [^1][^2][^3]. It is a protein complex structurally similar to the contractile tail of a bacteriophage and can carry protein payloads inside. PVC binds to the target cell surface, which is thought to trigger sheath contraction. This contraction drives the inner tube and spike toward the target cell, enabling payload delivery [^2][^3][^4]. In addition, the mechanism by which PVC recognizes target cells can be engineered. Kreitz et al. showed that the target cell specificity of PVC can be altered by replacing the C-terminal region of Pvc13 involved in target recognition with different receptor-binding domains [^3]. Using this strategy, they retargeted PVC and demonstrated protein delivery to human cells and mouse tissues beyond its native target range. 

Below, we describe in detail the structure of PVC, which served as the basis of CPI, its mechanisms of target recognition and injection, and its payload-loading mechanism.

:::details What Is PVC?

PVC is an eCIS found in the genus *Photorhabdus* and has a structure similar to the contractile tail of a bacteriophage [^1][^2][^3][^4]. In the *P. asymbiotica* PVC*pnf* system used for CPI, 16 core genes (*pvc1–pvc16*) required for assembly of functional particles are encoded within a region of approximately 20 kb [^3]. Downstream of these genes, endogenous payloads such as Pdp1 and Pnf are encoded. PVC particles consist of components including a tail fiber involved in interactions with the target cell surface, a baseplate that transmits structural changes, a contractile sheath, an inner tube that accommodates the payload, and a spike involved in penetration of the target cell surface [^3][^4]. Structural analysis of *P. asymbiotica* PVC reported a sheath–tube trunk length of approximately 117 nm [^7]. In contrast, extended particles of PlPVC1 from *P. luminescens* have an average length of approximately 280 nm, indicating that particle length and structure vary among different PVC systems [^4]. In addition, endogenous payloads Pdp1 and Pnf are retained inside the inner tube of *P. asymbiotica* PVC and delivered to target cells [^2][^5].

![pvc-structure2](https://static.igem.wiki/teams/6144/wiki/design/pvc-structure2.avif =500x)  

:::c

**Fig. 2.2.2.** Overall structure of the PVC particle  
Adapted from Kreitz, J. et al. (2023), licensed under CC BY 4.0 [^3].

:::

:::details Target Recognition and Injection

In PVC, the tail fiber Pvc13 plays an important role in interactions with target cells [^3]. Kreitz et al. identified residues 403–476 at the C-terminal region of Pvc13 as a putative target recognition domain and demonstrated that PVC target specificity can be altered by replacing this region with different receptor-binding domains [^3]. For example, introducing the trimeric knob domain of human adenovirus type 5 (Ad5) or the epidermal growth factor receptor (EGFR)-binding designed ankyrin repeat protein (DARPin) E01 into Pvc13 enabled binding and payload delivery to specific human cells [^3]. Although the detailed firing mechanism following target recognition remains under investigation, a model is supported in which structural changes in the baseplate associated with target recognition by the tail fiber are transmitted to the sheath, and sheath contraction drives the inner tube and spike toward the target cell [^4]. Importantly, the tail fiber and the contractile injection machinery are structurally distinct. This enables the delivery destination to be changed by modifying the target-recognition region of Pvc13 while retaining the basic injection machinery of PVC.

![pvc-replacement](https://static.igem.wiki/teams/6144/wiki/design/pvc-replacement.avif =500x)  
:::c

**Fig. 2.2.3.** Retargeting of Pvc13 by replacement of the C-terminal targeting domain  
Adapted from Kreitz, J. et al. (2023), licensed under CC BY 4.0 [^3].

:::

:::details Payload Loading

In PVC, endogenous payloads are loaded into the particle while being retained within the lumen of the inner tube. In *P. asymbiotica* PVC, Pdp1, a dNTP pyrophosphatase, and Pnf, a deamidase, have been reported to be retained inside the inner tube in a “Peas in the Pod” arrangement [^5]. The N-terminal regions of these endogenous payloads serve as packaging signals, enabling heterologous proteins to be loaded into PVC when fused to these regions. Jiang et al. demonstrated that the N-terminal sequences of Pdp1 and Pnf are important for payload loading and can be used to load heterologous proteins into PVC [^6]. Kreitz et al. further showed that intrinsically disordered regions at the N termini of Pdp1 and Pnf function as packaging domains [^3]. By fusing these regions to GFP, Cre recombinase, zinc finger nuclease, and other proteins, they successfully loaded non-native payloads into PVC and delivered them to target cells. Based on these findings, we selected the N-terminal region of Pdp1 (Pdp1_NTD) as the payload-loading signal for CPI. 

![pvc-pdp1-ntd](https://static.igem.wiki/teams/6144/wiki/design/pvc-pdp1-ntd.avif =500x)  
:::c

**Fig. 2.2.4.** Cargo packaging using Pdp1_NTD  
Adapted from Kreitz, J. et al. (2023), licensed under CC BY 4.0 [^3].

:::

As described above, PVC enables the separate engineering of target recognition, protein injection, and payload loading. In addition, rather than producing the protein of interest inside the target cell through gene expression, PVC can directly deliver the protein itself as a payload. These features make PVC well suited to the purpose of CPI, which is to deliver the desired Adaptor into target bacteria. We therefore adopted PVC as the basis of the CPI module. 

However, programmable protein delivery using PVC, including the PVC*pnf* system used as the basis of our design, has primarily been validated in eukaryotic cells [^3]. Since we aimed to achieve protein delivery to bacteria, we needed to address two key challenges: bacterial target recognition and payload delivery across the bacterial cell envelope. We selected drug-resistant E. coli as our target and designed modifications to the PVC tail fiber for selective binding to E. coli. We also evaluated the feasibility of injection across the bacterial cell envelope and constructed a receptor-binding protein (RBP) library to enable targeting of diverse bacterial strains. 

![pvc-for-sunrise](https://static.igem.wiki/teams/6144/wiki/design/pvc-for-sunrise-1.avif =500x)  
:::c

**Fig. 2.2.5. From PVC to the SUNRISE CPI module**

:::

 

# Design of the CPI Module

## Components of the CPI Module

CPI consists of the following three components.

:::c

**Table. 2.2.1** Components of the CPI module

:::

| Component | Function | Design | Parts |
| :---- | :---- | :---- | :---- |
| Targeting system | Recognizes the target bacterium and binds CPI to the cell surface | Introduces a bacteria-specific RBP into Pvc13 |  |
| Injection system | Penetrates the cell surface and delivers the payload into the cell | Uses the basic injection machinery derived from PVC |  |
| Payload | Protein to be delivered into the cell | Fuses Pdp1_NTD to the TPD Adaptor for loading into PVC |  |

We designed CPI to retain the core PVC injection machinery as a common component while allowing **the targeting system and payload** to be exchanged independently. This modular architecture enables CPI to be extended to different drug-resistant bacteria and different payloads without substantially modifying the core injection machinery.

![cpi-components](https://static.igem.wiki/teams/6144/wiki/design/cpi-components-1.avif =500x)  
:::c

**Fig. 2.2.6.** Modular architecture of the CPI module

:::

 

## Detailed Design

To assess the feasibility of PVC-mediated protein delivery to bacteria, we selected drug-resistant E. coli as the target of CPI. We designed a targeting system and a payload-loading strategy, and evaluated whether the PVC injection machinery could penetrate the bacterial cell envelope. With future in vivo applications in mind, we also developed an RBP library to facilitate the selection of suitable targeting modules for diverse drug-resistant E. coli strains. 

### (i) Retargeting CPI toward E. coli

To selectively bind PVC to *E. coli*, a molecule capable of recognizing the *E. coli* surface must be introduced into the tail fiber. In PVC, the C-terminal region of Pvc13 mediates interactions with target cells, and modifying this region can alter the target cell [^3].

In SUNRISE, we focused on **Gp17**, the tail fiber protein of bacteriophage T7, as a candidate molecule for recognizing *E. coli*. Each T7 tail fiber consists of a gp17 homotrimer whose C-terminal region is involved in binding to **E. coli** lipopolysaccharide (LPS) [^8][^9]. To retarget CPI to E. coli, we designed several Pvc13–gp17 fusions with different connection sites and linker configurations. We evaluated these designs using AlphaFold 3 and molecular docking, and selected a promising candidate based on its predicted structure and interactions with the target. Details of these analyses are provided on the Model page. 

![pvc-pvc13-gp17](https://static.igem.wiki/teams/6144/wiki/design/pvc-pvc13-gp17-1.avif =500x)  
:::c

**Fig. 2.2.7.** Design and in silico screening of the Pvc13–gp17 targeting system

:::

 

### (ii) Designing CPI for Injection into Prokaryotic Cells

Although PVC*pnf* has been demonstrated to deliver payloads to various eukaryotic cells following retargeting [^3], application to prokaryotic cells requires consideration of differences in cell surface structure. In Gram-negative bacteria such as *E. coli*, the payload must cross the cell envelope, which consists of the outer membrane, periplasm, peptidoglycan layer, and inner membrane, to reach the cytoplasm. Therefore, even if CPI can bind to the *E. coli* surface, it is necessary to evaluate whether the PVC inner tube and spike can sufficiently penetrate this cell envelope and deliver the payload to the cytoplasmic side.

Accordingly, we evaluated the feasibility of penetrating the E. coli cell envelope from both geometric and mechanical perspectives. We compared the PVC injection distance with the envelope thickness and simulated the mechanics of spike penetration through the outer membrane, peptidoglycan layer, and inner membrane. Our model suggested that the PVC injection machinery could penetrate the E. coli cell envelope without substantial modifications to its structure or length. We therefore designed CPI to retain the existing PVC injection machinery. Details of the analysis are described on [**the Model page**](https://2026.igem.wiki/waseda-tokyo/model/).

:::c

**Fig. 2.2.8.** Geometric evaluation of CPI penetration into the *E. coli* cell envelope

:::

 

### (iii) Loading the TPD Adaptor as the Payload

The ultimate purpose of CPI is to bind to the target bacteria and subsequently deliver the TPD Adaptor into the cell. For the molecular design of TPD itself, see [**the TPD Module**](https://2026.igem.wiki/waseda-tokyo/design/). To achieve this function, the desired TPD Adaptor must be loaded into CPI as a payload. In PVC, the N-terminal regions of endogenous payloads are important for payload loading [^3][^6].

We therefore designed a fusion of the N-terminal region of Pdp1 (Pdp1_NTD) and the TPD Adaptor for loading into PVC. We also performed simulations to estimate the payload-loading capacity of CPI particles based on the size of the Pdp1_NTD–Adaptor fusion and the internal space of the PVC inner tube. Detailed analyses of payload capacity and payload arrangement within CPI are described on [**the Model page**](https://2026.igem.wiki/waseda-tokyo/model/]).

:::c

**Fig. 2.2.9.** Packaging the TPD Adaptor into CPI using Pdp1_NTD

:::

 

### (iv) Expanding the Target Range of CPI

Although CPI carrying gp17 is intended to enable retargeting to *E. coli*, a design based on only a single RBP may be limited to a restricted range of strains. Through discussions with Professor Tsuneda of Waseda University ([**Human Practices**](https://2026.igem.wiki/waseda-tokyo/human-practices/])), we recognized the importance of accounting for differences in surface structures among clinical strains. Surface structures such as LPS, O antigen, capsules, and outer membrane proteins vary among strains, and surrounding structures may also limit receptor accessibility.    
In order to extend CPI to a wider range of drug-resistant *E. coli*, we constructed a library of candidate RBPs that recognize diverse bacterial surface structures based on bacteriophage host-recognition mechanisms.We categorized their targets into four groups: the LPS core, outer membrane proteins, O antigen, and capsule, and compiled candidate RBPs that recognize each category. We then evaluated the binding of each RBP to its target receptor and its accessibility on the cell surface *in silico*. This library provided a design framework for selecting an appropriate RBP to introduce into CPI based on the surface structure of the target bacterium. Details of the RBP library and simulation results are described on [**the Model page**](https://2026.igem.wiki/waseda-tokyo/model/).

:::c

**Fig. 2.2.10.** RBP library for expanding the targeting range of CPI 

:::  
 

# Advantages of the CPI Design

### **Protein-based**

CPI is designed to deliver the protein of interest itself directly as a payload rather than expressing a gene inside the target bacterium. This allows the TPD Adaptor to be delivered in protein form without depending on transcription or translation of foreign genes inside the target bacterium. By avoiding the introduction of Adaptor-encoding nucleic acids, CPI may reduce safety concerns associated with the persistence and unintended spread of genetic information.

### **Extending PVC to Prokaryotic Targets**

Programmable protein delivery using PVC*pnf* has primarily been developed for eukaryotic cells. To adapt PVC for protein delivery into bacteria, we redesigned the targeting system, evaluated the feasibility of injection across the bacterial cell envelope, and designed a payload-loading strategy for the TPD Adaptor. 

### **Modular**

We designed CPI to enable independent exchange of the targeting system and protein payload while retaining the core PVC injection machinery. Our *in silico* RBP library provides candidate targeting modules for diverse bacterial strains. This modularity enables CPI to be designed for different combinations of target bacteria and resistance proteins without substantially modifying the core injection machinery.


 

[^1]: Yang G, Dowling AJ, Gerike U, ffrench-Constant RH, Waterfield NR. Photorhabdus virulence cassettes confer injectable insecticidal activity against the wax moth. *J Bacteriol.* 2006;188(6):2254–2261. doi:10.1128/JB.188.6.2254-2261.2006

[^2]: Vlisidou I, Hapeshi A, Healey JRJ, Smart K, Yang G, Waterfield NR. The *Photorhabdus asymbiotica* virulence cassettes deliver protein effectors directly into target eukaryotic cells. *eLife.* 2019;8:e46259. doi:10.7554/eLife.46259

[^3]: Kreitz J, Friedrich MJ, Guru A, et al. Programmable protein delivery with a bacterial contractile injection system. *Nature.* 2023;616:357–364. doi:10.1038/s41586-023-05870-7

[^4]: Marín-Arraiza L, Roa-Eguiara A, Pape T, et al. Structural characterization of an extracellular contractile injection system from *Photorhabdus luminescens* in extended and contracted states. *Nat Commun.* 2025;16:9327. doi:10.1038/s41467-025-64377-z

[^5]: Wang X, Cheng J, Shen J, et al. Characterization of Photorhabdus Virulence Cassette as a causative agent in the emerging pathogen *Photorhabdus asymbiotica*. *Sci China Life Sci.* 2022;65(3):618–630. doi:10.1007/s11427-021-1955-4

[^6]: Jiang F, Shen J, Cheng J, et al. N-terminal signal peptides facilitate the engineering of PVC complex as a potent protein delivery system. *Sci Adv.* 2022;8(17):eabm2343. doi:10.1126/sciadv.abm2343

[^7]: Jiang F, Li N, Wang X, et al. Cryo-EM structure and assembly of an extracellular contractile injection system. *Cell.* 2019;177(2):370–383.e15. doi:10.1016/j.cell.2019.02.020

[^8]: Garcia-Doval C, van Raaij MJ. Structure of the receptor-binding carboxy-terminal domain of bacteriophage T7 tail fibers. *Proc Natl Acad Sci U S A.* 2012;109(24):9390–9395. doi:10.1073/pnas.1119719109

[^9]: González-García VA, Pulido-Cid M, Garcia-Doval C, et al. Conformational changes leading to T7 DNA delivery upon interaction with the bacterial receptor. *J Biol Chem.* 2015;290(16):10038–10044. doi:10.1074/jbc.M114.614222