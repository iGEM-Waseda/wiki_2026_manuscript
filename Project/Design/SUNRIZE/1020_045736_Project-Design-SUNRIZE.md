# SUNRISE

# Introduction

SUNRISE is a platform developed by Waseda-Tokyo 2026 to restore antibiotic susceptibility in drug-resistant bacteria by integrating the TPD and CPI modules. The CPI Injector is designed to recognize the target bacterium and inject the TPD Adaptor directly into the cell as a protein. Once delivered, the Adaptor is intended to recruit resistance proteins to the endogenous bacterial protease ClpXP for degradation [^1]. By reducing the abundance of these proteins, SUNRISE aims to restore susceptibility to existing antibiotics.

A key feature of SUNRISE is that bacterial targeting and resistance protein recognition can be designed independently. This page describes how the two modules are integrated and how a mathematical model is used to evaluate the integrated system. Details of each module are provided on the TPD Module and CPI Module pages.

![](https://static.igem.wiki/teams/6144/wiki/description/10-19.avif =500x)

:::c

Fig. 2.3.1. Overview of SUNRISE

:::

# Design of SUNRISE

## Components of SUNRISE

SUNRISE consists of two components: the TPD Adaptor and the CPI Injector.

:::c

Table. 2.3.1. Components of SUNRISE

:::

| Component | Intended function | Design |
| :---- | :---- | :---- |
| **TPD Adaptor** | Recognizes resistance proteins and induces their degradation by ClpXP | Combines an interchangeable Binder with a shared Linker–XB module; fuses Pdp1_NTD to the Adaptor’s N terminus via a linker for loading into CPI |
| **CPI Injector** | Recognizes the target bacterium and injects the TPD Adaptor into the cell | Combines an interchangeable receptor-binding protein (RBP) introduced into Pvc13 with the PVC injection machinery |

SUNRISE integrates the TPD and CPI modules to enable independent selection of the target bacterium and resistance protein. The Binder in the TPD Adaptor can be exchanged to change the resistance protein targeted for degradation, while the RBP in the CPI Injector’s tail fiber can be exchanged to change the target bacterium. 

To integrate the two modules, we designed a Pdp1_NTD–Adaptor fusion for loading into CPI, with Pdp1_NTD connected to the Adaptor’s N terminus via a flexible linker. We selected Pdp1_NTD, the N-terminal region of the native PVC payload Pdp1, because it can be used to load proteins into PVC [^2]. In this fusion, XB, which mediates binding to ClpXP, occupies a non-terminal position in the polypeptide chain. Because XB binds to the ClpX zinc-binding domain (ZBD) rather than its substrate-entry pore, it does not need to be positioned at a terminus [^1]. We therefore expected this arrangement to support both TPD-mediated degradation and payload loading into CPI.

This design allows SUNRISE to be adapted to different combinations of bacteria and resistance proteins by exchanging the Binder and RBP while retaining the core degradation and injection machinery.

![](https://static.igem.wiki/teams/6144/wiki/description/description-fig16.avif =500x)

:::c

Fig. 2.3.2. Modular architecture of SUNRISE

:::

## Model-based Functional Evaluation

Even if TPD and CPI each function individually, their integration does not necessarily yield sufficient resensitization. For example, insufficient delivery of the Adaptor into bacterial cells may limit susceptibility restoration, even if the Adaptor can efficiently induce resistance protein degradation . We therefore developed an Integrated Mathematical Model linking CPI-mediated delivery, TPD-mediated degradation, restoration of antibiotic susceptibility, and inhibition of bacterial growth.

The model estimates intracellular Adaptor delivery from the administered dose of SUNRISE and calculates the resulting dynamics of resistance protein degradation. It then incorporates the relationship between resistance protein abundance and antibiotic susceptibility to predict the effects on bacterial growth in the presence of antibiotics.

This calculation allows us to estimate the amount of Adaptor needed for resensitization, the delivery efficiency required of CPI, and the degradation performance required of TPD. The model can also help identify factors that limit overall SUNRISE performance and guide improvements to each module. Rather than evaluating the modules only in isolation, the model supports assessment of the integrated system’s feasibility at the design stage. Details are provided on the Model page.

:::c

Fig. 2.3.3. Integrated Mathematical Model connecting CPI-mediated delivery, TPD-mediated degradation, and antibiotic susceptibility

:::

# Advantages of the SUNRISE Design

## Modular and Programmable

Because the TPD Binder and CPI RBP can be exchanged independently, SUNRISE can be redesigned for different combinations of bacteria and resistance proteins without substantially changing the core degradation or injection machinery. In silico design of each module supports this approach.Together, these features provide a basis for extending SUNRISE to diverse drug-resistant bacteria.

## All-protein and Non-replicating

SUNRISE is designed to deliver the Adaptor directly as a protein, eliminating the need to introduce an Adaptor-encoding gene into the treated bacteria. The CPI Injector is a non-replicating protein complex, so the design also avoids risks arising from replication of the delivery system. Together, these features support our aim of developing a therapeutic platform with safety in mind. 

[^1]: Izert-Nowakowska MA, Klimecka MM, Antosiewicz A, et al. Targeted protein degradation in *Escherichia coli* using CLIPPERs. EMBO Reports. 2025;26:3994–4016. doi:10.1038/s44319-025-00510-9

[^2]: Kreitz J, Friedrich MJ, Guru A, et al. Programmable protein delivery with a bacterial contractile injection system. Nature. 2023;616:357–364. doi:10.1038/s41586-023-05870-7

