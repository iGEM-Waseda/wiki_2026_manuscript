# Introduction

This page lists all the parts we registered for SUNRISE, grouped into the sets we actually used (5 for TPD and 5 for CPI). Each collection links to the related Design, Experiments and Model pages.

**SUNRISE** delivers a modified protein into drug-resistant bacteria to remove a resistance protein. It has two modules, and our parts follow the same split.

The **TPD (Targeted Protein Degradation) module** breaks down a target protein inside the cell. Its core is an Adaptor, which joins a Binder that binds the target and a degron that pulls in the ClpXP protease with a flexible linker. Changing the Binder changes the target.

The **CPI (Cargo Protein Injection) module** delivers that protein into the resistant bacteria. It uses PVC, a contractile injector, and has three parts that can be swapped. Changing the tail fibre changes the target of the injector. Changing the cargo changes what is carried. Changing the reporter changes the readout.

Both modules are built from swappable parts. The collections below split those parts so that you can take them one by one.

- **62** parts registered
- **7** existing parts reused
- **2** existing parts with Documentation added
- **10** collections

Labels used in the tables:

- **New**: registered by our team.
- **Reused**: an existing Registry part that we reused.
- **Pending**: the part number will be given after the biosafety review.
- **Documentation added**: we added our own data to another team's existing part.

Related pages:

- [Design: Module design](https://2026.igem.wiki/waseda-tokyo/design/)
- [Model: Mathematical model](https://2026.igem.wiki/waseda-tokyo/model/#tpd-tpd-introduction)
- [Results](https://2026.igem.wiki/waseda-tokyo/results/)

# TPD: Targeted Protein Degradation

The five collections below are the tests that led to the Adaptor, and the Adaptors we designed.

## Collection 1: Degron and ClpXP degradation activity

Two degron tags are fused to eGFP, and degradation is followed directly by fluorescence.

This set fuses the two degron tags **XB** and **ssrA** to eGFP. ClpXP protease degrades eGFP that carries a degron, so degradation shows up directly as lower fluorescence.

Comparing with eGFP without a tag gives a number for how strong each degron is, and for how much protein ClpXP can degrade. No Adaptor, linker or Binder is present, so the drop in fluorescence comes only from the degron and ClpXP.

Related pages:

- [Experiment 1: Degron function validation](https://2026.igem.wiki/waseda-tokyo/experiments/#tpd-experiments-1---degron-function-validation)
- [Design: Target degradation by ClpXP](https://2026.igem.wiki/waseda-tokyo/design/#tpd-target-degradation-by-clpxp)

:::c
Table. 1.1. Parts for the degron test.
:::
| Registry ID | Name | Status | Role | Length |
|---|---|---|---|---|
| [BBa_S03452](https://registry.igem.org/parts/bba-s03452) | eGFP | Reused | Reporter (basic) | 720 bp |
| [BBa_2611O63X](https://registry.igem.org/parts/bba-2611o63x) | XB | New | Degradation tag (basic) | 36 bp |
| [BBa_26MRXNL2](https://registry.igem.org/parts/bba-26mrxnl2) | ssrA | New | Degradation tag (basic) | 33 bp |
| [BBa_263OQAOO](https://registry.igem.org/parts/bba-263oqaoo) | eGFP-XB | New | Reporter + degradation tag (basic) | 756 bp |
| [BBa_26TWF32J](https://registry.igem.org/parts/bba-26twf32j) | eGFP-ssrA | New | Reporter + degradation tag (basic) | 753 bp |

## Collection 2: GroTAC, the idea behind the TPD module

A degradation module from earlier work that joins a target-binding part and a degron with a linker.

Unlike ssrA, **XB** works at any position in a fusion. It recruits ClpXP when placed at either the N-terminus or the C-terminus of a protein.

**GroTAC** is XB joined to a target-binding part (a binder) by a flexible linker. Here the binder is **SBP**, and the target is the chaperone GroEL. GroTAC binds GroEL, recruits ClpXP protease and gets GroEL degraded, as shown in earlier work[^1]. The SUNRISE TPD module started from this idea.

The three parts are registered separately. By changing the binder, the same XB and linker can be used against another target.

Related pages:

- [Design: Adaptor background](https://2026.igem.wiki/waseda-tokyo/design/#tpd-what-are-clippers?)
- [Design: Components of the TPD module](https://2026.igem.wiki/waseda-tokyo/design/#tpd-3.1-components-of-the-tpd-module)
- [Experiment 2: Adaptor-mediated GroEL degradation](https://2026.igem.wiki/waseda-tokyo/experiments/#tpd-experiments-2---adaptor-mediated-groel-degradation)

:::c
Table. 1.2. Parts of GroTAC.
:::
| Registry ID | Name | Status | Role | Length |
|---|---|---|---|---|
| Pending | XB | New | Protease recruitment (basic) | 36 bp |
| [BBa_26VS0ISV](https://registry.igem.org/parts/bba-26vs0isv) | GGSGGSGG linker | New | Linker (basic) | 24 bp |
| [BBa_26522HLO](https://registry.igem.org/parts/bba-26522hlo) | SBP | New | Binder from literature (basic) | 36 bp |
| [BBa_2621VP0V](https://registry.igem.org/parts/bba-2621vp0v) | XB-GGSGGSGG-SBP(GroTAC2) | New | Reference Adaptor (composite) | 99 bp |

## Collection 3: Target quantification and the re-sensitization model

KanR and eGFP under three promoters of different strength.

This set puts **KanR** and **eGFP** downstream of three promoters of different strength (J23100 > J23110 > J23114). We used KanR to test kanamycin resistance.

Measuring eGFP fluorescence from the same promoters gives a rough number for the amount of KanR protein. We used this link to build the re-sensitization model. If the target is changed to another resistance protein, the same method can model that resistance too.

We used **J23110-KanR-XB** and **J23110-KanR-ssrA** to check whether degrading the resistance factor leads to re-sensitization. With another target, they can also be used to measure how degradation changes function.

Related pages:

- [Experiment 3: KanR expression and resistance quantification](https://2026.igem.wiki/waseda-tokyo/experiments/#tpd-experiments-3---kanr-expression-and-resistance-quantification)
- [Experiment 4: Dose response of degron-fused KanR](https://2026.igem.wiki/waseda-tokyo/experiments/#tpd-experiments-4---degron-fused-kanr-dose-response)
- [Experiment 6: SDS-PAGE of degron-fused KanR](https://2026.igem.wiki/waseda-tokyo/experiments/#tpd-experiments-6---degron-fused-kanr-sds-page)
- [Model: TPD module model](https://2026.igem.wiki/waseda-tokyo/model/#tpd-tpd-introduction)

:::c
Table. 1.3. Target and reporter parts under three promoters.
:::
| Registry ID | Name | Status | Role | Length |
|---|---|---|---|---|
| [BBa_26NCRBP5](https://registry.igem.org/parts/bba-26ncrbp5) | J23100-KanR | New | Target (drug resistance) (composite) | 1,025 bp |
| [BBa_263J5IL8](https://registry.igem.org/parts/bba-263j5il8) | J23110-KanR | New | Target (drug resistance) (composite) | 1,025 bp |
| [BBa_26QUHYD1](https://registry.igem.org/parts/bba-26quhyd1) | J23114-KanR | New | Target (drug resistance) (composite) | 1,025 bp |
| [BBa_26DRK4IZ](https://registry.igem.org/parts/bba-26drk4iz) | J23100-eGFP | New | Reporter (composite) | 950 bp |
| [BBa_26Z1N3S4](https://registry.igem.org/parts/bba-26z1n3s4) | J23110-eGFP | New | Reporter (composite) | 950 bp |
| [BBa_26UR0DYV](https://registry.igem.org/parts/bba-26ur0dyv) | J23114-eGFP | New | Reporter (composite) | 950 bp |
| [BBa_26YKL8GZ](https://registry.igem.org/parts/bba-26ykl8gz) | J23110-KanR-XB | New | Target + degradation tag (composite) | 1,061 bp |
| [BBa_26ORL0FN](https://registry.igem.org/parts/bba-26orl0fn) | J23110-KanR-ssrA | New | Target + degradation tag (composite) | 1,058 bp |

:::c
Table. 1.4. Existing parts reused inside the composite parts above.
:::
| Registry ID | Name | Status | Role | Length |
|---|---|---|---|---|
| [BBa_J23100](https://registry.igem.org/parts/bba-j23100) | J23100 | Reused | Promoter (basic) | 35 bp |
| [BBa_J23110](https://registry.igem.org/parts/bba-j23110) | J23110 | Reused | Promoter (basic) | 35 bp |
| [BBa_J23114](https://registry.igem.org/parts/bba-j23114) | J23114 | Reused | Promoter (basic) | 35 bp |
| [BBa_B0034](https://registry.igem.org/parts/bba-b0034) | B0034 | Reused | RBS (basic) | 12 bp |
| [BBa_K4850007](https://registry.igem.org/parts/bba-k4850007) | KanR | Reused | Target CDS (basic) | 795 bp |
| [BBa_S03452](https://registry.igem.org/parts/bba-s03452) | eGFP | Reused | Reporter CDS (basic) | 720 bp |
| [BBa_K4604043](https://registry.igem.org/parts/bba-k4604043) | rrnB T1/T7TE | Reused | Terminator (basic) | 147 bp |

## Collection 4: Adaptors against GroEL

Adaptors against GroEL, made with our binder design and evaluation pipeline.

These are Adaptors for the TPD module. We made **GB1–GB10** with our pipeline for designing and evaluating binders that bind the target GroEL. Each was joined to XB and a linker and designed as a TPD Adaptor that degrades GroEL.


Function has not been verified. The Adaptors in this collection are at the design stage, and we have not yet tested by experiment whether they degrade GroEL. We registered them to keep the design record and to let others reuse the output of our binder design pipeline as it is.


Each binder is registered both as a single basic part and as part of a finished Adaptor. You can take only the binder, or the whole Adaptor.

Related pages:

- [Design: In silico design of target-specific binders](https://2026.igem.wiki/waseda-tokyo/design/#tpd-(i)-in-silico-design-of-target-specific-binders)
- [Experiment 2: Adaptor-mediated GroEL degradation](https://2026.igem.wiki/waseda-tokyo/experiments/#tpd-experiments-2---adaptor-mediated-groel-degradation)

:::c
Table. 1.5. GroEL binders GB1–GB10.
:::
| Registry ID | Name | Status | Role | Length | Peptide |
|---|---|---|---|---|---|
| [BBa_26GY16NE](https://registry.igem.org/parts/bba-26gy16ne) | GB1 | New | De novo binder (basic) | 60 bp | SSSIRGQLMDAWEDVRASFA |
| [BBa_266M3B15](https://registry.igem.org/parts/bba-266m3b15) | GB2 | New | De novo binder (basic) | 39 bp | DPLEQLRENVWNM |
| [BBa_260G9U7F](https://registry.igem.org/parts/bba-260g9u7f) | GB3 | New | De novo binder (basic) | 60 bp | EPSIREKLLDAYNSVMEAMS |
| [BBa_26WNYNOF](https://registry.igem.org/parts/bba-26wnynof) | GB4 | New | De novo binder (basic) | 51 bp | NEEAVERLRESVEEMLA |
| [BBa_26KBDFHO](https://registry.igem.org/parts/bba-26kbdfho) | GB5 | New | De novo binder (basic) | 42 bp | SDEKVAQLRETVQQ |
| [BBa_26ITBIMG](https://registry.igem.org/parts/bba-26itbimg) | GB6 | New | De novo binder (basic) | 54 bp | SLSVREQLENTIADVKAR |
| [BBa_26E7DU7U](https://registry.igem.org/parts/bba-26e7du7u) | GB7 | New | De novo binder (basic) | 54 bp | MEKSIREQMEETVEWVRA |
| [BBa_26OEGG82](https://registry.igem.org/parts/bba-26oegg82) | GB8 | New | De novo binder (basic) | 51 bp | SSKIEDLRKIVDEANNK |
| [BBa_26NCZF9O](https://registry.igem.org/parts/bba-26nczf9o) | GB9 | New | De novo binder (basic) | 39 bp | SIEELRANVDRMA |
| [BBa_26KTOBXZ](https://registry.igem.org/parts/bba-26ktobxz) | GB10 | New | De novo binder (basic) | 36 bp | SPVEQLRELYDS |

:::c
Table. 1.6. GroEL Adaptors built from these binders.
:::
| Registry ID | Name | Status | Role | Length | Composition |
|---|---|---|---|---|---|
| [BBa_269HTZV6](https://registry.igem.org/parts/bba-269htzv6) | XB-GGSGGSGG-GB1 | New | Adaptor (composite) | 123 bp | XB + linker + GB1 |
| [BBa_26D2JGGT](https://registry.igem.org/parts/bba-26d2jggt) | XB-GGSGGSGG-GB2 | New | Adaptor (composite) | 102 bp | XB + linker + GB2 |
| [BBa_26CL9ZTU](https://registry.igem.org/parts/bba-26cl9ztu) | XB-GGSGGSGG-GB3 | New | Adaptor (composite) | 123 bp | XB + linker + GB3 |
| [BBa_26X4XUQ7](https://registry.igem.org/parts/bba-26x4xuq7) | XB-GGSGGSGG-GB4 | New | Adaptor (composite) | 114 bp | XB + linker + GB4 |
| [BBa_26Q451FS](https://registry.igem.org/parts/bba-26q451fs) | XB-GGSGGSGG-GB5 | New | Adaptor (composite) | 105 bp | XB + linker + GB5 |
| [BBa_26U6VEBG](https://registry.igem.org/parts/bba-26u6vebg) | XB-GGSGGSGG-GB6 | New | Adaptor (composite) | 117 bp | XB + linker + GB6 |
| [BBa_26C4PKU1](https://registry.igem.org/parts/bba-26c4pku1) | XB-GGSGGSGG-GB7 | New | Adaptor (composite) | 117 bp | XB + linker + GB7 |
| [BBa_26MJP0QW](https://registry.igem.org/parts/bba-26mjp0qw) | XB-GGSGGSGG-GB8 | New | Adaptor (composite) | 114 bp | XB + linker + GB8 |
| [BBa_26Q0U8UI](https://registry.igem.org/parts/bba-26q0u8ui) | XB-GGSGGSGG-GB9 | New | Adaptor (composite) | 102 bp | XB + linker + GB9 |
| [BBa_26OUXUDZ](https://registry.igem.org/parts/bba-26ouxudz) | XB-GGSGGSGG-GB10 | New | Adaptor (composite) | 99 bp | XB + linker + GB10 |

:::c
Table. 1.7. Backbone parts shared with Collection 2.
:::
| Registry ID | Name | Status | Role | Length |
|---|---|---|---|---|
| Pending | XB | New | Protease recruitment (basic) | 36 bp |
| [BBa_26VS0ISV](https://registry.igem.org/parts/bba-26vs0isv) | GGSGGSGG linker | New | Linker (basic) | 24 bp |

## Collection 5: Adaptors against KanR

Adaptors that degrade the kanamycin resistance factor, aiming at re-sensitization.

These are TPD Adaptors against the kanamycin resistance factor **KanR**. We made **KB1–KB10** with our pipeline for designing and evaluating de novo binders. They are designed so that KanR is degraded and the cells become sensitive to kanamycin again.

We tested the Adaptors in **Experiment 5** (dose response of KanR with Adaptors) and **Experiment 7** (SDS-PAGE of KanR with Adaptors).

If a binder is designed against another drug resistance protein, the same method gives an Adaptor that degrades that protein. All parts except the binder are shared, so only the binder is replaced.

Related pages:

- [Design: In silico design of target-specific binders](https://2026.igem.wiki/waseda-tokyo/design/#tpd-(i)-in-silico-design-of-target-specific-binders)
- [Design: Designing against conserved regions of resistance variants](https://2026.igem.wiki/waseda-tokyo/design/#tpd-(ii)-designing-binders-against-conserved-regions-of-resistance-variants)
- [Experiment 5: Adaptor-mediated KanR dose response](https://2026.igem.wiki/waseda-tokyo/experiments/#tpd-experiments-5---adaptor-mediated-kanr-dose-response)
- [Experiment 7: Adaptor-mediated KanR SDS-PAGE](https://2026.igem.wiki/waseda-tokyo/experiments/#tpd-experiments-7---adaptor-mediated-kanr-sds-page)

:::c
Table. 1.8. KanR binders KB1–KB10.
:::
| Registry ID | Name | Status | Role | Length | Peptide |
|---|---|---|---|---|---|
| [BBa_26TF3LHV](https://registry.igem.org/parts/bba-26tf3lhv) | KB1 | New | De novo binder (basic) | 45 bp | APTELEVMIEQARAY |
| [BBa_261UKC18](https://registry.igem.org/parts/bba-261ukc18) | KB2 | New | De novo binder (basic) | 48 bp | DEEMSRIAQRWIEEMQ |
| [BBa_2660GKBC](https://registry.igem.org/parts/bba-2660gkbc) | KB3 | New | De novo binder (basic) | 48 bp | NDSEEGNRVMKELLAS |
| [BBa_26CONADT](https://registry.igem.org/parts/bba-26conadt) | KB4 | New | De novo binder (basic) | 54 bp | SREMGNEMAKVVNAWLDS |
| [BBa_26L267DK](https://registry.igem.org/parts/bba-26l267dk) | KB5 | New | De novo binder (basic) | 54 bp | DPDRENQEKSKAWLESHQ |
| [BBa_26762SMB](https://registry.igem.org/parts/bba-26762smb) | KB6 | New | De novo binder (basic) | 54 bp | SEEMNRVGNAVMQELWDA |
| [BBa_26APH5C8](https://registry.igem.org/parts/bba-26aph5c8) | KB7 | New | De novo binder (basic) | 57 bp | DEIDEARNKEHMAWLKSVE |
| [BBa_264SKXWZ](https://registry.igem.org/parts/bba-264skxwz) | KB8 | New | De novo binder (basic) | 57 bp | PPSDNELAQAWLDRERDRL |
| [BBa_26ALR6FK](https://registry.igem.org/parts/bba-26alr6fk) | KB9 | New | De novo binder (basic) | 57 bp | MTRRERRRKKFREQESIWN |
| [BBa_26NO8PVP](https://registry.igem.org/parts/bba-26no8pvp) | KB10 | New | De novo binder (basic) | 60 bp | PTPEEVTLGKQKQAWLDSMM |

:::c
Table. 1.9. KanR Adaptors built from these binders.
:::
| Registry ID | Name | Status | Role | Length | Composition |
|---|---|---|---|---|---|
| [BBa_26DWYXKO](https://registry.igem.org/parts/bba-26dwyxko) | XB-GGSGGSGG-KB1 | New | Adaptor (composite) | 108 bp | XB + linker + KB1 |
| [BBa_26RKN3X3](https://registry.igem.org/parts/bba-26rkn3x3) | XB-GGSGGSGG-KB2 | New | Adaptor (composite) | 111 bp | XB + linker + KB2 |
| [BBa_26TE88YU](https://registry.igem.org/parts/bba-26te88yu) | XB-GGSGGSGG-KB3 | New | Adaptor (composite) | 111 bp | XB + linker + KB3 |
| [BBa_26WDHMTO](https://registry.igem.org/parts/bba-26wdhmto) | XB-GGSGGSGG-KB4 | New | Adaptor (composite) | 117 bp | XB + linker + KB4 |
| [BBa_26X0E8YJ](https://registry.igem.org/parts/bba-26x0e8yj) | XB-GGSGGSGG-KB5 | New | Adaptor (composite) | 117 bp | XB + linker + KB5 |
| [BBa_266Z2EBL](https://registry.igem.org/parts/bba-266z2ebl) | XB-GGSGGSGG-KB6 | New | Adaptor (composite) | 117 bp | XB + linker + KB6 |
| [BBa_2648LOV1](https://registry.igem.org/parts/bba-2648lov1) | XB-GGSGGSGG-KB7 | New | Adaptor (composite) | 120 bp | XB + linker + KB7 |
| [BBa_2657EN8G](https://registry.igem.org/parts/bba-2657en8g) | XB-GGSGGSGG-KB8 | New | Adaptor (composite) | 120 bp | XB + linker + KB8 |
| [BBa_26DBSPIU](https://registry.igem.org/parts/bba-26dbspiu) | XB-GGSGGSGG-KB9 | New | Adaptor (composite) | 120 bp | XB + linker + KB9 |
| [BBa_2615GEYJ](https://registry.igem.org/parts/bba-2615geyj) | XB-GGSGGSGG-KB10 | New | Adaptor (composite) | 123 bp | XB + linker + KB10 |

:::c
Table. 1.10. Backbone parts shared with Collection 2.
:::
| Registry ID | Name | Status | Role | Length |
|---|---|---|---|---|
| Pending | XB | New | Protease recruitment (basic) | 36 bp |
| [BBa_26VS0ISV](https://registry.igem.org/parts/bba-26vs0isv) | GGSGGSGG linker | New | Linker (basic) | 24 bp |

# CPI: Cargo Protein Injection

The CPI module uses the contractile injector PVC to deliver a modified protein into target cells. The parts are grouped into four sets: injector, tag, cargo and readout. Each set can be swapped on its own.

## Collection 1: Injector, the PVC production plasmids

Four plasmids covering three conditions: the sheath tag, the tail fibre and Pvc10.

All four plasmids were made from **pAWP78-PVCpnf_Δpvc10** (Addgene #198448, Kreitz et al., 2023[^2]). They differ in three points: the FLAG tag on the sheath protein Pvc2, the tail fibre Pvc13, and Pvc10.

V03 and V04 differ only in one codon of Pvc10, and V02 and V04 differ only in the tail fibre. These comparisons separate the effect of the tail fibre from the effect of Pvc10. In V01 and V03, Pvc10 is not deleted but cut short by an internal stop codon. V04 restores that codon (TAA to GTG), so full-length Pvc10 is made.

In the tail fibre, we inserted a 188-amino-acid region of a gp17-type tail fibre protein from a T7-like phage, flanked by GGSGG linkers. This fusion is our own design and is not in the plasmids of Kreitz et al.[^2]

Related pages:

- [Experiment 4: BL21(DE3) cell surface binding validation](https://2026.igem.wiki/waseda-tokyo/experiments/#cpi-experiments-4---bl21(de3)-cell-surface-binding-validation)
- [Experiment 5: Payload injection into BL21(DE3) validation](https://2026.igem.wiki/waseda-tokyo/experiments/#cpi-experiments-5---payload-injection-into-bl21(de3)-validation)
- [CPI plasmid master list](https://2026.igem.wiki/waseda-tokyo/experiments/#cpi---plasmid-master-list)

:::c
Table. 1.11. Injector production plasmids V01–V04.
:::
| Registry ID | Name | Status | Role | FLAG on Pvc2 | Tail fibre | Pvc10 |
|---|---|---|---|---|---|---|
| [BBa_26ZGZI08](https://registry.igem.org/parts/bba-26zgzi08) | pAWP78-PVCpnf_Δpvc10 (V01) | New | Parent plasmid, control without tag (plasmid) | None | Native | Truncated |
| [BBa_268PBNXY](https://registry.igem.org/parts/bba-268pbnxy) | pAWP78-PVCpnf_FLAG (V02) | New | Control for attachment (plasmid) | Yes | Native | Full length |
| [BBa_26FZ40IW](https://registry.igem.org/parts/bba-26fz40iw) | pAWP78-PVCpnf_Δpvc10_gp17_FLAG (V03) | New | Control expected to bind but not inject; intermediate of V04 (plasmid) | Yes | Modified (gp17) | Truncated |
| [BBa_26SXWO4N](https://registry.igem.org/parts/bba-26sxwo4n) | pAWP78-PVCpnf_PVC10_gp17_FLAG (V04) | New | Experimental plasmid (plasmid) | Yes | Modified (gp17) | Full length |

## Collection 2: Tag

An epitope tag for detecting injector particles with an antibody.

This tag lets an anti-FLAG antibody detect injector particles. In V02, V03 and V04 it is placed right after the start codon of the sheath protein Pvc2.

Related pages:

- [Wet Lab: CPI overview](https://2026.igem.wiki/waseda-tokyo/experiments/#cpi-wet-lab-overview)

:::c
Table. 1.12. Epitope tag.
:::
| Registry ID | Name | Status | Role | Length | Use |
|---|---|---|---|---|---|
| [BBa_26R7K35U](https://registry.igem.org/parts/bba-26r7k35u) | FLAG epitope tag (DYKDDDDK) | New | Epitope tag (basic) | 24 bp | Detects injector particles with an anti-FLAG antibody. Placed right after the start codon of Pvc2 in V02, V03 and V04. |

## Collection 3: Cargo, the protein that is carried

A control to show that loading depends on the transport signal.

The cargo is **Cre recombinase**, because its activity is easy to read out. A protein that carries the N-terminal domain of Pdp1 (**Pdp1_NTD**) is taken into the injector particle, so this domain acts as the transport signal.

We registered **Cre without a transport signal**. This control expresses the same Cre without Pdp1_NTD, and it shows that loading depends on Pdp1_NTD.

The cargo with the signal, a fusion of Pdp1_NTD and Cre, was **already registered by ETH-Zurich 2026 as BBa_26IXZE2Q**. We did not register it again. We added the background of our use and our Cre activity data to their part as Documentation (see Collection 5 of CPI).

Related pages:

- [Experiment 2: Pdp1_NTD–Cre activity validation](https://2026.igem.wiki/waseda-tokyo/experiments/#cpi-experiments-2---pdp1_ntd-cre-activity-validation)
- [Experiment 3: Pdp1_NTD-dependent payload loading validation](https://2026.igem.wiki/waseda-tokyo/experiments/#cpi-experiments-3---pdp1_ntd-dependent-payload-loading-validation)

:::c
Table. 1.13. Cargo control without a transport signal.
:::
| Registry ID | Name | Status | Role | Length | Use |
|---|---|---|---|---|---|
| [BBa_26HPRBH4](https://registry.igem.org/parts/bba-26hprbh4) | FLAG-NLS-Cre | New | Control cargo (basic) | 1,080 bp | Loading control. The same Cre without a transport signal, to show that loading depends on Pdp1_NTD. |

## Collection 4: Readout, the Cre-responsive reporter

A reporter that turns red only when Cre has acted.

The reporter has a promoter, a region with two terminators between two loxP sites, and **mRFP1**. When Cre removes the terminators and one loxP, mRFP1 is expressed. This lets us evaluate delivery cell by cell.

The **loxP-double terminator-loxP** region was already registered by Waseda-Tokyo 2024 as BBa_K5436202. Our reporter plasmid uses the same sequence, so we did not register it again. We added our methods and data to that part as Documentation.

Related pages:

- [Experiment 1: Reporter validation](https://2026.igem.wiki/waseda-tokyo/experiments/#cpi-experiments-1---reporter-validation)

:::c
Table. 1.14. Cre-responsive switch of the reporter.
:::
| Registry ID | Name | Status | Role | Length | Use |
|---|---|---|---|---|---|
| [BBa_K5436202](https://registry.igem.org/parts/bba-k5436202) | loxP-double terminator-loxP | Documentation added | Cre-responsive switch (basic) | — | When Cre removes the terminators and one loxP, the downstream mRFP1 is expressed. Registered by Waseda-Tokyo 2024. |

## Collection 5: Documentation added to existing parts

Two parts registered by other teams, where we added our data instead of registering again.

When we use the same sequence as an existing part, we add Documentation to that part and do not make a new one. This keeps the Registry knowledge graph from splitting, and the next team that uses the part also gets the information.

Related pages:

- [Experiment 1: Reporter validation](https://2026.igem.wiki/waseda-tokyo/experiments/#cpi-experiments-1---reporter-validation)
- [Experiment 2: Pdp1_NTD–Cre activity validation](https://2026.igem.wiki/waseda-tokyo/experiments/#cpi-experiments-2---pdp1_ntd-cre-activity-validation)

:::c
Table. 1.15. Documentation we added to existing parts.
:::
| Registry ID | Name | Team | What we added |
|---|---|---|---|
| [BBa_26IXZE2Q](https://registry.igem.org/parts/bba-26ixze2q) | Pdp1_NTD–Cre | ETH-Zurich 2026 | The background of our use, and data (n = 3) comparing the activity of the fused Cre with unfused Cre in E. coli BL21(DE3). |
| [BBa_K5436202](https://registry.igem.org/parts/bba-k5436202) | loxP-double terminator-loxP | Waseda-Tokyo 2024 | Methods and data of the reporter in E. coli BL21(DE3). |

# Notes

**About pending numbers.** Pending parts have been submitted. We will add the BBa number here once the review is done. The lengths are final values taken from sequence-verified constructs.

**Why there are two XB parts.** XB appears in TPD Collections 1 and 2 as separate parts. Both code for the same peptide `CYRGGRPALRVV`, but the codons differ. The XB in Collection 1 was added with the 5′ tail of a PCR primer. The XB in Collection 2 came on a synthesized fragment. The Registry matches sub-parts by exact sequence, so each one needs its own record.

**Plasmid construction.** The [TPD plasmid master list](https://2026.igem.wiki/waseda-tokyo/experiments/#tpd---plasmid-master-list) shows which plasmid each part was built on.

**Background.** GroTAC and the XB–linker–binder design are based on CLIPPER degraders[^1]. We used BindCraft to design the binders[^3].

[^1]: Izert-Nowakowska et al. (2025) Targeted protein degradation in Escherichia coli using CLIPPERs. EMBO Rep. doi: 10.1038/s44319-025-00510-9
[^2]: Kreitz J. et al. (2023) Programmable protein delivery with a bacterial contractile injection system. Nature 616, 357-364. doi: 10.1038/s41586-023-05870-7
[^3]: Pacesa et al. (2025) One-shot design of functional protein binders with BindCraft. Nature. doi: 10.1038/s41586-025-09429-6
