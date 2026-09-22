# 1. Introduction

Targeted Protein Degradation (TPD) is a protein degradation module in SUNRISE designed to selectively degrade resistance proteins in drug-resistant bacteria and restore their susceptibility to existing antibiotics. In TPD, a protein-based Adaptor recognizes a target resistance protein and brings it into proximity with ClpXP, an endogenous bacterial protease, thereby inducing its degradation. By making the Binder responsible for target recognition exchangeable, we designed TPD as a module that can be extended not only to a specific resistance factor but also to a wide range of resistance proteins.

:::c

**Fig. 1. Overview of the TPD module in SUNRISE**

:::

# 2. Background

TPD aims to eliminate resistance proteins that are already expressed in drug-resistant bacteria. We therefore focused on CLIPPERs (Clp-Interacting Peptidic Protein Erasers), a technology that induces selective degradation by recruiting target proteins to ClpXP inside bacterial cells [^1].

CLIPPERs were developed as molecules consisting of a Bait that binds to the target protein and an Anchor that binds to ClpX, connected by a Linker [^1]. In the previous study, the ClpX-binding peptide XB was used as the Anchor and combined with a peptide that binds to the target protein as the Bait, enabling degradation of endogenous proteins without the artificial addition of a degron. In particular, CLIPPERs targeting GroEL, a chaperone in *Escherichia coli*, were termed GroTACs, and were shown to cause a time-dependent decrease in GroEL levels together with inhibition of bacterial growth [^1].

Below, we describe in detail the structure of CLIPPERs, which served as the basis of TPD, and the mechanism of target degradation using ClpXP.

:::details What Are CLIPPERs?

CLIPPERs are peptide-based degraders that induce target protein degradation by artificially bringing a target protein into proximity with the endogenous bacterial ClpXP protease [^1]. CLIPPERs consist of a **Bait** that binds to the target protein, an **Anchor** that recruits ClpXP, and a **Linker** that connects the two. In the previous study, several Anchor candidates for recruiting ClpXP were compared, and the **XB peptide**, derived from the C-terminal region of the SspB adaptor, was selected [^1]. XB binds to the **zinc-binding domain (ZBD)** of ClpX, the ATPase subunit of ClpXP. Unlike strategies in which a degron is added to the target protein to make it a direct substrate of ClpX, this design uses ClpX binding to bring the target protein into proximity with the degradation machinery. In the previous study, GroTACs were constructed by linking a GroEL-binding peptide as the Bait to XB, and binding to both GroEL and ClpX, as well as GroEL degradation, was confirmed [^1].

:::c

**Fig. 2. Overall architecture of CLIPPERs**

:::


:::details Target Degradation by ClpXP

ClpXP is an ATP-dependent protease widely found in bacteria and consists of the ATPase ClpX and the protease ClpP. In general ClpXP-mediated proteolysis, ClpX recognizes a substrate and uses ATP hydrolysis to unfold it while translocating it into the proteolytic chamber of ClpP. The substrate is then proteolyzed inside ClpP. In CLIPPERs, XB binds to the ZBD of ClpX, while the Bait within the same molecule binds to the target protein, thereby inducing proximity between ClpX and the target protein [^1]. The original CLIPPERs study showed that XB-containing GroTACs not only bind to ClpX but also increase ClpX ATPase activity. Formation of a GroEL–ClpX ternary complex by GroTACs and ClpXP-dependent GroEL degradation were also confirmed [^1]. Thus, CLIPPERs can induce **ClpXP-dependent degradation through induced proximity without genetically adding a known degron to the target protein itself**. However, the complete molecular mechanism by which a target lacking a degron is ultimately engaged by ClpX and proceeds to unfolding has not yet been fully elucidated. In SUNRISE, we aim to use this experimentally demonstrated XB-mediated recruitment to bring resistance proteins into proximity with ClpXP.

:::c

**Fig. 3. Recruitment of target proteins to ClpXP by the TPD adaptor**

:::


As described above, in CLIPPERs, target protein recognition and recruitment to ClpXP are mediated by different regions. This modularity is well suited to the purpose of TPD, in which the Binder can be changed to target different resistance proteins. We therefore adopted CLIPPERs as the basis of the TPD module.

However, the only target for which degradation by CLIPPERs has been experimentally demonstrated is GroEL, and the system **has not yet been extended to a wide range of antimicrobial resistance factors.** To make TPD applicable to diverse resistance factors, a system is needed that can rapidly generate new Binders for each target. We therefore used **BindCraft**, which enables the design of novel Binders from protein structures, and designed a TPD system that retains the CLIPPERs-derived Linker–XB as a common component while de novo designing a Binder for each target, thereby enabling expansion to diverse resistance factors. In addition, to address not only a single resistance protein variant but multiple variants, we adopted a Binder design strategy targeting surface regions that are conserved among variants.

:::c

**Fig. 4. From CLIPPERs to the SUNRISE TPD module**

:::


## 3. Design of the TPD Module

### 3.1 Components of the TPD Module

TPD consists of the following three components.

:::c

**Table. 1. Components of the TPD module**

:::

| Component | Function | Design | Parts |
| ----- | ----- | ----- | ----- |
| Binder | Recognizes the target protein | De novo designed for each target using BindCraft |  |
| Linker | Flexibly connects the Binder and XB | Uses a common structure based on CLIPPERs |  |
| XB | Binds to the ZBD of ClpX and brings the target into proximity with ClpXP | Uses a common structure based on CLIPPERs |  |

**We designed the Adaptor so that the Linker–XB remains as a common component, while only the Binder can be exchanged according to the target protein.**  
This allows TPD to be extended to different resistance proteins without changing the basic mechanism that brings the target protein into proximity with ClpXP.

:::c

**Fig. 5. Modular architecture of the TPD module**


:::


### 3.2 Detailed Design

We selected aminoglycoside 3′-phosphotransferase IIa [APH(3′)-IIa], which is involved in kanamycin resistance, as a model target for TPD. To apply TPD to actual antimicrobial resistance factors, it is necessary to design a Binder that binds to the target resistance protein. In addition, because resistance factors often have many variants, Binder design should ideally enable recognition of multiple variants rather than only a single variant. We therefore designed TPD by combining de novo Binder design from target structures with a strategy that targets regions conserved among multiple variants.

### (i) In Silico Design of Target-Specific Binders

To make TPD applicable to diverse resistance factors, Binders that bind to each target must be prepared. Conventional CLIPPERs used known target-binding peptides as the Bait [^1]. However, suitable Binders are not necessarily known for all clinically important resistance factors. Therefore, a strategy that depends only on known Binders limits the range of resistance factors to which TPD can be extended.

In SUNRISE, we therefore established a workflow using BindCraft to **de novo design target-specific Binders directly from the three-dimensional structure of the target protein** [^2]. First, we obtain the three-dimensional structure of the target resistance protein and define candidate regions for Binder binding. Next, BindCraft is used to generate Binder candidates against these regions. The generated Binders are evaluated based on the predicted complex structure, interface-related confidence metrics, interactions with the target, and the predicted structure of the Binder itself, and promising candidates are selected. The selected Binder is then connected to the common Linker–XB to construct a target-specific TPD Adaptor. This design enables TPD candidates to be generated directly from target structures for new resistance factors without depending on the availability of known Binders. Details of Binder generation and in silico screening are described on the Model page.

:::c

**Fig. 6. In silico design and screening of target-specific binders**

:::


### (ii) Designing Binders against Conserved Regions of Resistance Variants

Many resistance factors have multiple variants with different amino acid sequences while retaining the same function. If a Binder recognizes only a region unique to a particular variant, the applicability of that TPD may be limited to that variant.

SUNRISE therefore adopted a design strategy that **targets protein surface regions that are conserved among multiple variants and are accessible to the Binder**. First, the amino acid sequences of multiple variants responsible for the same resistance mechanism are compared, and highly conserved regions are identified by multiple sequence alignment. However, sequence conservation alone is not sufficient for a region to serve as a Binder target. If a conserved region is buried inside the protein, it may be physically inaccessible to the Binder. Therefore, in addition to sequence conservation, we examine the position of the region in the three-dimensional structure and select conserved regions exposed on the protein surface as candidate Binder-design sites. BindCraft is then used to design Binders targeting these conserved regions, and their potential to bind structures of multiple variants is evaluated. Through this strategy, rather than designing a separate Adaptor for each variant, we aim to develop **a TPD capable of recognizing multiple resistance variants with a single Binder**. This approach is intended to broaden the applicability of TPD to sequence-diverse resistance factors. Details of sequence comparison, selection of conserved regions, and Binder design are described on the Model page.

:::c

**Fig. 7. Designing a common binder for multiple resistance variants**

:::


## 4. Advantages of the TPD Design

### Modular

By retaining the Linker–XB as a common component and making only the Binder exchangeable, the target protein can be changed without altering the basic ClpXP-mediated degradation mechanism. This may enable future expansion beyond antimicrobial resistance factors to the selective degradation of a variety of bacterial proteins.

### Expandable

By de novo designing Binders from the three-dimensional structures of target proteins, TPD can be designed against different resistance factors without depending on the availability of known Binders.

### Broad

By targeting surface regions conserved among multiple variants, we aim to enable a single Adaptor to recognize multiple resistance variants. This design allows TPD development to account for sequence diversity among resistance factors.

### Protein-based

TPD induces target protein degradation using a protein-based Adaptor composed of a Binder, Linker, and XB. Rather than introducing genes into the target bacterium, we aim to deliver the Adaptor itself through CPI and allow it to function directly.


[^1]: Izert-Nowakowska MA, Klimecka MM, Antosiewicz A, et al. Targeted protein degradation in *Escherichia coli* using CLIPPERs. *EMBO Rep.* 2025;26:7. doi:10.1038/s44319-025-00510-9

[^2]: Pacesa M, Nickel L, Schellhaas C, et al. One-shot design of functional protein binders with BindCraft. *Nature.* 2025;646:483–492. doi:10.1038/s41586-025-09429-6
