To ensure reproducibility, we organized all experimental procedures used in our project into three categories: General Protocols, TPD Experiments, and CPI Experiments.Select a category below to explore the protocols used throughout our project.

# General Experiments

## General Wet Lab Overview

Our basic experimental workflow follows a cycle of plasmid construction, transformation, culture, and verification. Plasmids are assembled by [NEBuilder HiFi DNA Assembly](../results/#gp01) or [KOD -Plus- Mutagenesis](../results/#gp02), introduced into *E. coli* DH5α by heat-shock [transformation](../results/#gp03), and selected on antibiotic-supplemented [LB agar plates](../results/#gp04). Colonies are grown overnight in [liquid culture](../results/#gp05) and plasmid DNA is isolated by [miniprep](../results/#gp06). The plasmid is verified by [agarose gel electrophoresis](../results/#gp07), [restriction enzyme digestion](../results/#gp08), and [Sanger sequencing](../results/#gp09). The verified plasmid is then transformed into the appropriate host and cultured while monitoring growth by [OD₆₀₀](../results/#gp05).

## General Protocols

:::details General Protocol 1 - NEBuilder HiFi DNA Assembly  
<div style="display: flex; justify-content: center; margin: 24px auto;">  
 <iframe src="https://static.igem.wiki/teams/6144/wiki/experiments/gp01-nebuilder-hifi-dna-assembly.pdf" width="80%" height="800px"></iframe>  
</div>

:::

:::details General Protocol 2 - KOD -Plus- Mutagenesis  
<div style="display: flex; justify-content: center; margin: 24px auto;">  
 <iframe src="https://static.igem.wiki/teams/6144/wiki/experiments/gp02-kod-plus-mutagenesis.pdf" width="80%" height="800px"></iframe>  
</div>

:::

:::details General Protocol 3 - Transformation  
<div style="display: flex; justify-content: center; margin: 24px auto;">  
 <iframe src="https://static.igem.wiki/teams/6144/wiki/experiments/gp03-transformation.pdf" width="80%" height="800px"></iframe>  
</div>

:::

:::details General Protocol 4 - Preparation of LB Broth and LB Agar Plates  
<div style="display: flex; justify-content: center; margin: 24px auto;">  
 <iframe src="https://static.igem.wiki/teams/6144/wiki/experiments/gp04-preparation-of-lb-broth-and-agar-plates.pdf" width="80%" height="800px"></iframe>  
</div>

:::

:::details General Protocol 5 - Liquid Culture and OD600 Measurement  
<div style="display: flex; justify-content: center; margin: 24px auto;">  
 <iframe src="https://static.igem.wiki/teams/6144/wiki/experiments/gp05-liquid-culture-and-od600-measurement.pdf" width="80%" height="800px"></iframe>  
</div>

:::

:::details General Protocol 6 - Miniprep  
<div style="display: flex; justify-content: center; margin: 24px auto;">  
 <iframe src="https://static.igem.wiki/teams/6144/wiki/experiments/gp06-miniprep.pdf" width="80%" height="800px"></iframe>  
</div>

:::

:::details General Protocol 7 - Sanger Sequencing Submission  
<div style="display: flex; justify-content: center; margin: 24px auto;">  
 <iframe src="https://static.igem.wiki/teams/6144/wiki/experiments/gp07-sanger-sequencing-submission.pdf" width="80%" height="800px"></iframe>  
</div>

:::

:::details General Protocol 8 - Agarose Gel Electrophoresis  
<div style="display: flex; justify-content: center; margin: 24px auto;">  
 <iframe src="https://static.igem.wiki/teams/6144/wiki/experiments/gp08-agarose-gel-electrophoresis.pdf" width="80%" height="800px"></iframe>  
</div>

:::

:::details General Protocol 9 - Restriction Enzyme Digestion  
<div style="display: flex; justify-content: center; margin: 24px auto;">  
 <iframe src="https://static.igem.wiki/teams/6144/wiki/experiments/gp09-restriction-enzyme-digestion.pdf" width="80%" height="800px"></iframe>  
</div>

:::

# TPD Experiments

## TPD Wet Lab Overview

The TPD module aims to de novo design adaptors that target antibiotic resistance proteins and to induce their degradation by the endogenous protease ClpXP, thereby resensitizing bacteria to antibiotics. The wet lab divided this proof of concept into two phases.

In Phase A, we validated that the adaptor (CLIPPER) developed in a previous study (Checking your browser - reCAPTCHA) functions as reported, and that it remains functional when its bait region is replaced with a de novo designed binder. In Phase B, using kanamycin as a model, we validated the resensitization of bacteria to an antibiotic through degradation of a drug resistance protein, and went on to evaluate resensitization by a de novo designed adaptor. Phase B was evaluated quantitatively in close collaboration with dry lab modeling (iGEM 2026 Waseda-Tokyo). For the basic principle of the TPD module, see the Design section.

First, In Section A-1, "Degradation assay of degron-fused eGFP," we confirmed that XB, a peptide derived from SspB, functions as a degradation-inducing tag (degron). We fused ssrA and XB, both known degrons, to the C-terminus of the reporter protein eGFP and expressed them from the arabinose-inducible promoter pBAD. By measuring fluorescence, we evaluated degron-mediated degradation of eGFP.

Next, In Section A-2, "Growth inhibition assay for adaptor-mediated GroEL degradation," we examined whether GroTAC (XB-GGSGGSGG-SBP), an adaptor that employs SBP, a peptide ligand of the chaperone GroEL, induces degradation of GroEL and thereby inhibits bacterial growth. Growth inhibition was quantified by OD600 measurement and CFU counting.

In Section A-3, "Direct detection of GroEL degradation by SDS-PAGE," we verified by SDS-PAGE that the amount of GroEL protein decreases as a result of adaptor (GroTAC) function.

In Section B-1, "Kanamycin dose-response assay across promoter strengths," we examined how a change in the expression level of the kanamycin resistance protein aminoglycoside-3'-phosphotransferase-IIa (APH(3')-IIa) alters the kanamycin concentration that still permits growth. KanR was constitutively expressed from three promoters of differing strength, and OD600 was measured across a seven-point kanamycin concentration series.

In Section B-2, "eGFP fluorescence measurement across promoter strengths (quantification of expression from J23100, J23110, and J23114)," we determined the amount of KanR protein expressed in Section B-1 by measuring the fluorescence intensity of eGFP expressed from the same three constitutive promoters. The measurements from Sections B-1 and B-2 are used in the Model section.

In Section B-3, "Kanamycin dose-response assay of degron-fused KanR," we examined whether degron-mediated degradation of the kanamycin resistance protein lowers the kanamycin concentration that suppresses growth. XB and ssrA tags were fused to the C-terminus of KanR, and the assay was evaluated by measuring OD600 across a kanamycin concentration series.

Finally, In Section B-4, "Kanamycin dose-response assay using a KanR-targeting adaptor," we examined whether a de novo designed adaptor induces degradation of KanR and lowers the kanamycin concentration that suppresses growth. Both KanR and the adaptor were expressed constitutively, and the assay was evaluated by measuring OD600 across a kanamycin concentration series.

Through these two phases of experiments, we stepwise validated the function of the degron, the function of the non-fused adaptor, the direct degradation of the target protein, and the resensitization of bacteria to an antibiotic through degradation of a drug resistance protein.  
![]()

:::c

**Fig. 1.9.** Integrated Mathematical Model of SUNRISE

:::

## TPD Protocols

:::details TPD Protocol 1 - 実験のタイトル  
<div style="display: flex; justify-content: center; margin: 24px auto;">  
 <iframe src="PDFのリンク" width="80%" height="800px"></iframe>  
</div>

[Click to see Result](../results/#)

:::

:::details TPD Protocol 2 - 実験のタイトル  
<div style="display: flex; justify-content: center; margin: 24px auto;">  
 <iframe src="PDFのリンク" width="80%" height="800px"></iframe>  
</div>

[Click to see Result](../results/#)

:::

:::details TPD Protocol 3 - 実験のタイトル  
<div style="display: flex; justify-content: center; margin: 24px auto;">  
 <iframe src="PDFのリンク" width="80%" height="800px"></iframe>  
</div>

[Click to see Result](../results/#)

:::

:::details TPD Protocol 4 - 実験のタイトル  
<div style="display: flex; justify-content: center; margin: 24px auto;">  
 <iframe src="PDFのリンク" width="80%" height="800px"></iframe>  
</div>

[Click to see Result](../results/#)

:::

:::details TPD Protocol 5 - 実験のタイトル  
<div style="display: flex; justify-content: center; margin: 24px auto;">  
 <iframe src="PDFのリンク" width="80%" height="800px"></iframe>  
</div>

[Click to see Result](../results/#)

:::

# CPI Experiments

## CPI Wet Lab Overview

The CPI module aims to deliver proteins into bacteria using PVCs with engineered tails, and to have the delivered protein exert its function inside the cell. As a proof of concept for this function, the wet lab used Cre recombinase as the functional protein, delivered it into the model target cell E. coli BL21(DE3), and assessed functional protein delivery by monitoring whether an intracellular Cre-responsive reporter was activated. To verify this ultimate goal in a stepwise manner, the wet lab divided the experiments into the following five sections. For the basic principle of the CPI module, see the Design section; for the strategy behind the PVC tail modification, see the Model section.

First, In Section 1, "Validation of the reporter system," we confirmed that the reporter system used to detect intracellular Cre activity works as intended. We constructed a system in which the reporter is activated by Cre-mediated DNA recombination between loxP sites, and evaluated whether Cre activity could be detected as a reporter signal.

Next, In Section 2, "Functional validation of the cargo protein," we examined whether Cre retains its recombinase activity when fused to Pdp1_NTD, the domain required for loading the protein into PVC. This allowed us to assess whether Pdp1_NTD-Cre could be used as the functional protein in PVC delivery experiments.

In Section 3, "Validation of protein loading into PVC," we tested whether Pdp1_NTD-Cre is packaged into PVC particles. PVCs were produced and purified under conditions in which Pdp1_NTD-Cre was expressed, and the purified PVC particles were analyzed for the presence of Cre in order to evaluate Pdp1_NTD-mediated cargo loading.

In Section 4, "Validation of binding to target cells," we tested whether tail-engineered PVCs can bind to the model target cell BL21(DE3). By observing the localization of PVC-derived and BL21(DE3)-derived signals, we evaluated binding of the engineered PVC to the target cells.

Finally, In Section 5, "Validation of functional protein delivery," we integrated all of the elements validated above and applied engineered PVCs loaded with Pdp1_NTD-Cre to BL21(DE3). Using activation of the Cre-responsive reporter introduced into BL21(DE3) as the readout, we evaluated whether Cre is delivered into the target cell by PVC and remains functional after delivery.

Through these five stages of experiments, we stepwise validated the loading of a functional protein into PVC, binding to the target cell, delivery into the cell, and functional activity after delivery.

![]()

:::c

**Fig. 1.9.** Integrated Mathematical Model of SUNRISE

:::

## CPI Protocols

:::details CPI Protocol 1 - 実験のタイトル  
<div style="display: flex; justify-content: center; margin: 24px auto;">  
 <iframe src="PDFのリンク" width="80%" height="800px"></iframe>  
</div>

[Click to see Result](../results/#)

:::

:::details CPI Protocol 2 - 実験のタイトル  
<div style="display: flex; justify-content: center; margin: 24px auto;">  
 <iframe src="PDFのリンク" width="80%" height="800px"></iframe>  
</div>

[Click to see Result](../results/#)

:::

:::details CPI Protocol 3 - 実験のタイトル  
<div style="display: flex; justify-content: center; margin: 24px auto;">  
 <iframe src="PDFのリンク" width="80%" height="800px"></iframe>  
</div>

[Click to see Result](../results/#)

:::

:::details CPI Protocol 4 - 実験のタイトル  
<div style="display: flex; justify-content: center; margin: 24px auto;">  
 <iframe src="PDFのリンク" width="80%" height="800px"></iframe>  
</div>

[Click to see Result](../results/#)

:::

:::details CPI Protocol 5 - 実験のタイトル  
<div style="display: flex; justify-content: center; margin: 24px auto;">  
 <iframe src="PDFのリンク" width="80%" height="800px"></iframe>  
</div>

[Click to see Result](../results/#)

:::