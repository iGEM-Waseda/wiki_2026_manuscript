**TPD Wet Lab Overview**

The TPD module aims to de novo design adaptors that target antibiotic resistance proteins and to induce their degradation by the endogenous protease ClpXP, thereby resensitizing bacteria to antibiotics. The wet lab divided this proof of concept into two phases.

In Phase A, we validated that the adaptor (CLIPPER) developed in a previous study [^1] functions as reported, and that it remains functional when its bait region is replaced with a de novo designed binder. In Phase B, using kanamycin as a model, we validated the resensitization of bacteria to an antibiotic through degradation of a drug resistance protein, and went on to evaluate resensitization by a de novo designed adaptor. Phase B was evaluated quantitatively in close collaboration with dry lab modeling ([iGEM 2026 Waseda-Tokyo](https://2026.igem.wiki/waseda-tokyo/model/)). For the basic principle of the TPD module, see the Design section.

First, In Section A-1, "Degradation assay of degron-fused eGFP," we confirmed that XB, a peptide derived from SspB, functions as a degradation-inducing tag (degron). We fused ssrA and XB, both known degrons, to the C-terminus of the reporter protein eGFP and expressed them from the arabinose-inducible promoter pBAD. By measuring fluorescence, we evaluated degron-mediated degradation of eGFP.

Next, In Section A-2, "Growth inhibition assay for adaptor-mediated GroEL degradation," we examined whether GroTAC (XB-GGSGGSGG-SBP), an adaptor that employs SBP, a peptide ligand of the chaperone GroEL, induces degradation of GroEL and thereby inhibits bacterial growth. Growth inhibition was quantified by OD600 measurement and CFU counting.

In Section A-3, "Direct detection of GroEL degradation by SDS-PAGE," we verified by SDS-PAGE that the amount of GroEL protein decreases as a result of adaptor (GroTAC) function.

In Section B-1, "Kanamycin dose-response assay across promoter strengths," we examined how a change in the expression level of the kanamycin resistance protein aminoglycoside-3'-phosphotransferase-IIa (APH(3')-IIa) alters the kanamycin concentration that still permits growth. KanR was constitutively expressed from three promoters of differing strength, and OD600 was measured across a seven-point kanamycin concentration series.

In Section B-2, "eGFP fluorescence measurement across promoter strengths (quantification of expression from J23100, J23110, and J23114)," we determined the amount of KanR protein expressed in Section B-1 by measuring the fluorescence intensity of eGFP expressed from the same three constitutive promoters. The measurements from Sections B-1 and B-2 are used in the Model section.

In Section B-3, "Kanamycin dose-response assay of degron-fused KanR," we examined whether degron-mediated degradation of the kanamycin resistance protein lowers the kanamycin concentration that suppresses growth. XB and ssrA tags were fused to the C-terminus of KanR, and the assay was evaluated by measuring OD600 across a kanamycin concentration series.

Finally, In Section B-4, "Kanamycin dose-response assay using a KanR-targeting adaptor," we examined whether a de novo designed adaptor induces degradation of KanR and lowers the kanamycin concentration that suppresses growth. Both KanR and the adaptor were expressed constitutively, and the assay was evaluated by measuring OD600 across a kanamycin concentration series.

Through these two phases of experiments, we stepwise validated the function of the degron, the function of the non-fused adaptor, the direct degradation of the target protein, and the resensitization of bacteria to an antibiotic through degradation of a drug resistance protein.

:::c
**Fig. 1.3.** Overview
:::

[^1]: Izert-Nowakowska, M. A., Klimecka, M. M., Antosiewicz, A., Wróblewski, K., Kowalski, J. J., Bandyra, K. J., Góral, T., Kmiecik, S., Serwa, R. A., & Górna, M. W. (2025). Targeted protein degradation in Escherichia coli using CLIPPERs. EMBO reports, 26(16), 3994–4016. https://doi.org/10.1038/s44319-025-00510-9