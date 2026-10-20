# **TPD Module**

# **1. Introduction**

Targeted Protein Degradation (TPD) is SUNRISE’s protein degradation module designed to selectively degrade resistance proteins inside drug-resistant bacteria and restore their susceptibility to existing antibiotics. It uses a peptide Adaptor with three components: a Binder that recognizes the target resistance protein, an Anchor that recruits the endogenous bacterial protease ClpXP, and a Linker connecting the two. The Adaptor is intended to bring the target protein into proximity with ClpXP and induce its degradation. We designed TPD to accommodate diverse resistance proteins by making the Binder interchangeable and targeting structural features (common structural cores) shared by multiple proteins.

![](https://static.igem.wiki/teams/6144/wiki/description/fig1-1.avif =600x)

:::c

Fig. 2.1.1. Overview of the TPD module in SUNRISE

:::

# **2. Background**

Bacteria can resist antibiotics through resistance proteins, including enzymes that inactivate antibiotics or modify their cellular targets [^1]. Through discussions with Meiji Seika Pharma (Human Practices), we explored the potential and challenges of restoring antibiotic susceptibility by inhibiting these proteins. Some inhibitors act at an enzyme’s active site or substrate-binding site to suppress its function. However, the diversity of resistance proteins and their variants can make it difficult to achieve broad coverage with a single inhibitor [^2].

We therefore turned to degradation of the resistance protein itself as an alternative to directly inhibiting its function. To implement this approach, we focused on Clp-Interacting Peptidic Protein Erasers (CLIPPERs), which use the endogenous bacterial protease ClpXP to induce target protein degradation [^3]. CLIPPERs are peptides consisting of a target-binding Bait and a ClpXP-recruiting Anchor connected by a Linker. Izert-Nowakowska et al. developed CLIPPERs targeting the *Escherichia coli* chaperone GroEL and demonstrated GroEL degradation and inhibition of bacterial growth [^3].

The following sections describe the architecture of CLIPPERs and the mechanism of ClpXP-mediated target degradation that underpin the TPD design.

:::details What Are CLIPPERs?

CLIPPERs are a peptide-based approach that recruits endogenous bacterial proteins to ClpXP for degradation without adding an artificial degradation tag to the target protein [^3]. They consist of a target-binding Bait, an Anchor that recruits ClpXP, and a flexible Linker connecting the two. In the original study, the authors compared several candidate Anchors and selected the ClpX-binding peptide (XB), derived from the C-terminal region of the SspB adaptor [^3]. XB binds to the zinc-binding domain (ZBD) of ClpX, and crystallographic analysis has confirmed this binding mode [^4].

The ssrA tag, a commonly used degradation signal, is recognized at the substrate-entry pore of ClpX. Using ssrA as the Anchor would therefore be expected to make the CLIPPER itself susceptible to degradation. XB instead binds to the ZBD, which may help limit degradation of the CLIPPER itself. It also imposes fewer constraints than ssrA on its position within a polypeptide [^3].

In the original study, the authors used the GroEL-binding strong binding peptide (SBP) as the Bait and connected it to XB via a Linker to create GroTACs. SBP alone does not directly inhibit GroEL function, but GroTACs reduced GroEL abundance and affected bacterial growth and viability, particularly under heat stress [^3].

:::c

Fig. 2.1.2. Overall architecture of CLIPPERs


:::

:::details Target Degradation by ClpXP

ClpXP is an ATP-dependent protease widely distributed in bacteria. It consists of the ATPase ClpX and the proteolytic component ClpP. ClpX recognizes substrate proteins and uses ATP hydrolysis to unfold them and translocate them into ClpP, where they are degraded [^5]. In CLIPPERs, the Bait binds to the target protein while XB binds to the ZBD of ClpX, bringing the target protein into proximity with ClpXP [^3].

The original study demonstrated formation of a ternary complex comprising GroEL, a GroTAC, and the ClpX ZBD, as well as stimulation of ClpX ATPase activity and ClpXP-dependent GroEL degradation [^3]. CLIPPERs can thus use the endogenous bacterial degradation machinery to induce target degradation without adding a degradation tag to the target protein. However, degradation efficiency may depend on the target’s structure and its orientation relative to ClpXP, and some proteins may be unsuitable for this approach [^3]. In SUNRISE, we aim to adapt this XB-based degradation mechanism to resistance proteins.

:::c

Fig. 2.1.3. Recruitment of target proteins to ClpXP by the TPD Adaptor

:::



In CLIPPERs, distinct regions mediate target recognition and recruitment to ClpXP. This modular architecture is well suited to TPD, in which the Binder can be exchanged to match the target protein. We therefore adopted CLIPPERs as the basis of the TPD module.

Although the original study demonstrated GroEL degradation, the use of CLIPPERs to degrade diverse resistance proteins remains to be established. Because the original design used a known binding peptide, extending the approach to new targets requires suitable Binders [^3]. To address this limitation, we adopted BindCraft for de novo Binder design based on target protein structures [^6]. We also used FoldMason to compare the structures of multiple resistance proteins as a basis for designing Binders against shared structural features [^7]. By combining the CLIPPER degradation mechanism with de novo Binder design and the search for shared structural features, we designed TPD to address a broad range of resistance proteins.

:::c

Fig. 2.1.4. From CLIPPERs to the SUNRISE TPD module

:::

# **3. Design of the TPD Module**

## **3.1 Components of the TPD Module**

The TPD Adaptor consists of three components.

:::c

Table. 2.1.2. Components of the TPD module

:::

| Component | Function | Design | Parts |
| :---: | :---- | :---- | :---: |
| **Binder** | Recognizes the target resistance protein | Designed de novo with BindCraft for the intended target |  |
| **Linker** | Connects the Binder and Anchor | Flexible GGS repeats based on the CLIPPER design |  |
| **Anchor (XB)** | Binds to the ClpX ZBD to bring the target into proximity with ClpXP | XB from the CLIPPER design, retained across Adaptors |  |

We designed the Adaptor with an interchangeable Binder while retaining the CLIPPER-derived XB and a flexible Linker. This modular architecture allows the design to be adapted to different resistance proteins without substantially changing how ClpXP is recruited.

:::c

Fig. 2.1.5. Modular architecture of the TPD module

:::

## **3.2 Detailed Design**

To design TPD Adaptors that target multiple resistance proteins, we developed a **TPD Design Pipeline** integrating three stages: identifying common structural cores, designing Adaptors, and evaluating their potential safety risks. The pipeline also supports designs for a single resistance protein. The following sections describe the design and evaluation steps in this pipeline.

### **(i) Identifying Common Structural Core**

To enable a single Binder to recognize multiple resistance proteins, we searched for structural regions shared by those proteins, referred to here as common structural cores.The pipeline begins by selecting a group of resistance proteins and obtaining their three-dimensional structures. FoldMason is then used to identify common structural cores through multiple structure alignment, comparing local structural similarities across the proteins [^7].Details of the structural alignment and identification of common structural cores are provided on the Model page.

:::c

Fig. 2.1.6. Identification of common structural regions in resistance proteins using FoldMason

:::

### **(ii) In Silico Adaptor Design**

To design an Adaptor for a resistance protein, we needed a Binder that could bind the target. We used BindCraft to design such Binders de novo [^6].Binder design begins with the structure of a target protein, which is used to generate candidate Binders. For designs intended to recognize multiple resistance proteins, a common structural core identified in step (i) is selected as the target region. The candidates are then screened by predicted binding affinity to prioritize those most likely to bind the target.Using this approach, we designed Adaptors to target the selected resistance proteins.For designs intended to target multiple resistance proteins, we also predicted the structures of complexes between the Adaptor and the other resistance proteins to assess potential binding to each target. Before experimental testing, we also used molecular dynamics (MD) simulations to assess the Adaptor’s potential to function. We evaluated the structural stability of a ternary complex comprising the target protein, the Adaptor, and the ClpX ZBD, as well as Linker flexibility. Details of the Binder design settings, screening by predicted binding affinity, binding predictions for multiple targets, and MD simulations are provided on the Model page.

:::c

Fig. 2.1.7. In silico design and screening of target-specific Binders

:::

### **(iii) Adaptor Safety Assessment**

Adaptors may bind to unintended proteins, making careful assessment of target specificity essential. This is especially important for Adaptors designed to recognize multiple resistance proteins. Because the Binders are designed de novo, information about their toxicity is limited. We therefore assessed the specificity and potential toxicity of the designed Adaptors in silico. To assess specificity, we predicted the structures of complexes between the Adaptor and essential proteins from *E. coli* and humans. We included *E. coli* proteins because the Adaptor is intended to act inside this bacterium, and human proteins to account for possible unintended exposure during future in vivo administration. To assess potential toxicity, we screened for sequence similarity to known toxins and allergens and for domains associated with harmful functions. We also used machine learning to predict peptide toxicity and hemolytic activity. These analyses allowed us to assess potential safety risks before experimental testing. Details of these methods and results are provided on the Model and Safety pages.

:::c

Fig. 2.1.8. In silico evaluation of the specificity and toxicity of the TPD Adaptor

:::

# **4. Advantages of the TPD Design**

## **Degradation Beyond Functional Sites**

The Binder does not need to inhibit the resistance protein’s function directly. Binding sites for TPD can therefore extend beyond active sites and substrate-binding sites to other regions of the protein structure. This may allow TPD to target protein structural regions that are difficult to exploit with conventional inhibitors.

## **Broad Target Coverage**

By targeting structural features shared by multiple resistance proteins or their variants, a single Adaptor may recognize several resistance factors. This could reduce the need to develop a separate Adaptor for each resistance protein and broaden the target range of TPD.

## **Modularity**

We designed TPD with an interchangeable Binder while retaining Linker–XB for ClpXP recruitment. The in silico design pipeline combining BindCraft and FoldMason supports Binder design and evaluation for new resistance proteins. This modularity allows the design to be adapted to diverse resistance proteins without changing the underlying degradation mechanism. Beyond antimicrobial resistance (AMR), the approach may eventually be adapted for selective degradation of other proteins in *E. coli*.

# 

[^1]: Wachino JI, Doi Y, Arakawa Y. Aminoglycoside resistance: Updates with a focus on acquired 16S ribosomal RNA methyltransferases. Infectious Disease Clinics of North America. 2020;34(4):887–902. doi:10.1016/j.idc.2020.06.002

[^2]: Tehrani KHME, Martin NI. β-Lactam/β-lactamase inhibitor combinations: an update. MedChemComm. 2018;9(9):1439–1456. doi:10.1039/C8MD00342D

[^3]: Izert-Nowakowska MA, Klimecka MM, Antosiewicz A, et al. Targeted protein degradation in *Escherichia coli* using CLIPPERs. EMBO Reports. 2025;26:3994–4016. doi:10.1038/s44319-025-00510-9

[^4]: Park EY, Lee BG, Hong SB, Kim HW, Jeon H, Song HK. Structural basis of SspB-tail recognition by the zinc binding domain of ClpX. Journal of Molecular Biology. 2007;367(2):514–526. doi:10.1016/j.jmb.2007.01.003

[^5]: Baker TA, Sauer RT. ClpXP, an ATP-powered unfolding and protein-degradation machine. Biochimica et Biophysica Acta - Molecular Cell Research. 2012;1823(1):15–28. doi:10.1016/j.bbamcr.2011.06.007

[^6]: Pacesa M, Nickel L, Schellhaas C, et al. One-shot design of functional protein binders with BindCraft. Nature. 2025;646:483–492. doi:10.1038/s41586-025-09429-6

[^7]: Gilchrist CLM, Mirdita M, Steinegger M. Multiple protein structure alignment at scale with FoldMason. Science. 2026;391(6784):485–488. doi:10.1126/science.ads6733