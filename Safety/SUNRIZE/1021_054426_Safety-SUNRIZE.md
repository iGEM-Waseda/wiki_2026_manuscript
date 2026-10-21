# **Project Safety**

## **1. Overview**

SUNRISE is a platform that aims to re-sensitize drug-resistant bacteria by combining the TPD Module, which degrades drug-resistance proteins inside bacteria, with the CPI Module, which delivers it to the target bacteria. In the future, we aim to administer SUNRISE to patients so that it acts on drug-resistant bacteria at the site of infection.

For the safety assessment, we assumed the use case that Waseda-Tokyo 2026 adopted when considering the real-world implementation of the project: treatment of patients with urinary tract infections caused by drug-resistant *E. coli*. In this use, the bladder is emptied with a catheter, SUNRISE is instilled into the bladder and kept there for a while, and it then leaves with the urine. This is repeated several times, and we assume in the model that kanamycin is given together by intramuscular injection. These are assumptions made for the assessment, and it has not been decided that SUNRISE will actually be administered this way. Systemic administration and release into the environment are outside the scope of this assessment.

With these considerations in mind,we aimed not only to evaluate its therapeutic efficacy but also to address safety and the risk of misuse from the outset. We therefore used the Progressive Safety Assessment Framework (PSAF) that we developed to explore the risks expected at each stage of the project, and organized the safety issues that should be considered from the design stage. We also incorporated insights from expert discussions through our Human Practices work into our design policy, and evaluated the characteristics and limits of SUNRISE’s safety through Dry Lab analyses and a literature review.

This page summarizes our design decisions and the results of the assessment. The methods and detailed results of the analyses are on the [Model](http://LINK_TO_MODEL_1) page, and the discussions that led to our designs are on the [Human Practices](http://LINK_TO_HUMAN_PRACTICES) page, so please refer to them as well. Please note that most of the assessments shown here are based on Dry Lab predictions and the literature, and verification by experiments or clinical data is still to come. For this reason, at the end of each section we state what has not yet been confirmed and what we plan to do next. For safety measures inside the laboratory, please see [General Laboratory Safety](http://LINK_TO_GENERAL_LAB_SAFETY), and for the background and method of PSAF, please see [PSAF](http://LINK_TO_PSAF).

## **2. Safety and Security by Design**

In each of the following sections, we show which risks identified by PSAF (Risk IDs) correspond to each design decision. The list of risks and the results of the assessment are summarized in Section 3.

### **2.1. Protein-Based Design**

Corresponding Risk IDs: R08, R20

To deliver the TPD Adaptor to the target bacteria, we considered two approaches: introducing a gene and expressing the Adaptor inside the bacteria, or delivering the protein directly. Through discussions with Dr. Kiga of the Japan Institute for Health Security (JIHS), and in order to reduce the risks that come with introducing genetic information, we adopted an all-protein system that introduces no new genetic information at the time of treatment and performs both delivery and induction of degradation with proteins alone. How we arrived at this choice is explained on the [Human Practices](http://LINK_TO_HUMAN_PRACTICES) page.

This system does not require introducing, replicating or spreading a gene that encodes the Adaptor, and the Injector functions as an independent, non-replicating protein complex. It therefore avoids the persistence and horizontal transfer of genetic information that must be considered when genes are delivered by phage or similar means, and the risks of growth and colonization that come with using live bacteria as a carrier. However, an all-protein system is not necessarily safe in the body. Proteins can also be immunogenic or toxic, and residual nucleic acids and endotoxin from production must also be controlled.

The final product is designed to contain no nucleic acid, and is considered unable to replicate itself or to pass on genes. The genes for the Injector and the genes for the Payload and regulation are carried on separate plasmids, and the vectors have no conjugation factors. On the other hand, we have not yet defined the clinical-grade purification process or the limits for residual DNA, host proteins and endotoxin (R08). We will standardize a purification process that includes removal and measurement of endotoxin, and set these limits.

### **2.2. Toxicity and Immunogenicity**

Corresponding Risk IDs: R08, R09, R10, R11, R12

In our discussions with Dr. Kiga of JIHS, we learned that immune responses to foreign proteins, toxicity, and impurities from production are important safety issues. The importance of immunogenicity assessment in the development of therapeutic proteins is also shown in FDA guidance[1]. In particular, because the Injector is a large protein complex derived from bacteria, immune responses and systemic exposure may become a problem with intravenous administration. We therefore chose to prioritize local administration, delivering it directly to the site of infection.

Among the components, the TPD Adaptor, which contains *de novo* designed sequences, has little similarity to known proteins, so conventional homology searches alone cannot adequately assess its potential toxicity. We therefore performed a two-layer assessment, combining Layer 1, which examines homology to known harmful factors, and Layer 2, which predicts toxicity from the properties of the sequence. We applied it to several Adaptors targeting GroEL and APH(3′)-IIa, and to an Adaptor targeting a structure shared by multiple resistance proteins (C1). In Layer 1 we used BLASTp to search for homology to known toxins, InterProScan to search for domains related to toxins and membrane damage, and AllergenOnline to search for cross-reactivity with allergens. In Layer 2 we used ToxinPred3.0 to predict toxicity and HemoPI2 to predict hemolysis[2]. The results for each Adaptor are shown on the [Model](http://LINK_TO_MODEL_2) page.

As a result, no candidate met the criteria for homology to known toxins or for allergenicity. Known protein domains were detected in some candidates, but none was annotated as a toxin. In the hemolysis prediction, some candidates met the criterion for being considered hemolytic and others did not (R11). We also used the HemoPI2 predictions to consider an upper limit for the administered concentration. These are predictions from sequences and we have no measured values, so we conservatively judged the severity as Severe. This assessment is a screening step to decide whether to proceed to wet experiments, and it does not show that SUNRISE is safe.

In addition, repeated administration may cause antibodies against CPI to form and weaken its effect (R09). In experiments on the system from which CPI was derived, particles with endotoxin removed were administered to the mouse brain, and no activation of immune cells, rise in inflammatory cytokines, loss of body weight or cytotoxicity was seen[3]. However, the conditions differ from our assumption of repeated administration to humans. Particles with an unstable structure may also break down or aggregate during storage or transport and stimulate the immune system (R10). Kanamycin, which is given together, is an aminoglycoside antibiotic known to damage the kidneys and hearing (R12). In the model assumptions, the dose and blood concentration are expected to stay below the reference and upper limit values, but these are model values and we have no clinical data.

The assessments so far rest on sequence-based predictions and the literature, and experimental verification is still to come. Next, we will confirm by experiments the hemolysis and cytotoxicity of the full-length Adaptor (R11), the production of antibodies against CPI and the effect of repeated administration (R09), and stability during storage and transport (R10).

### **2.3. Target Specificity**

Corresponding Risk IDs: R13, R14, R21

Through discussions with Meiji Seika Pharma, we learned that drug-resistance proteins exist in many types and variants. For the TPD Module, we therefore aimed for a design that recognizes a structural region shared by multiple resistance proteins, so that a single Binder can address a wide range of resistance types. In addition, through a discussion with Dr. Tsuneda of Waseda University, we recognized that clinically important *E. coli* strains have diverse surface structures and that a single RBP may not be sufficient, so we built a Targeting Library from which an RBP can be selected according to the target strain. How we arrived at these designs is explained on the [Human Practices](http://LINK_TO_HUMAN_PRACTICES) page.

However, widening the target range may also lead to unintended effects on bacteria or human cells. We therefore assessed off-target risk from two angles: binding of TPD to non-target proteins, and delivery of CPI to non-target cells.

For TPD, we obtained information on essentiality from the Keio collection[4] and DepMap[5], and information on abundance from PaxDb[6], and prioritized abundant essential proteins of *E. coli* and humans as targets of the assessment. We then examined the possibility of binding to the Adaptor by predicting complex structures with AlphaFold Server. No combination exceeded the criterion, but some Adaptors showed values close to it, so binding may still occur in practice. The targets and results of this assessment are described on the [Model](http://LINK_TO_MODEL_3) page.

For CPI, we evaluated gp17, which recognizes glycans, and Gp38, which recognizes a protein (OmpA), as representatives of the two recognition chemistries. For gp17, docking analysis with Vina-Carb gave the target *E. coli* LPS core a better score than the human glycans and non-target bacterial glycans we examined. However, most of the score is explained by the size of the ligand, so this does not fully demonstrate specificity. For Gp38, we searched OmpA, its receptor, by sequence with BLASTp and by structure with Foldseek. No receptor candidate was found on the surface of human cells, and the possibility of cross-reactivity in bacteria was strongly concentrated in *Escherichia*. On the other hand, a concern about cross-reactivity remains for *Salmonella*. We also examined with a mathematical model whether the requirement that several tail fibers bind at once could amplify differences in binding at the level of the whole particle. The targets, conditions and results of the CPI assessments are described on the [Model](http://LINK_TO_MODEL_4) page.

Within the range we examined, no receptor candidate accessible on the surface of human cells was found, but this is a relative comparison and does not guarantee that there is no binding. For glycan-recognizing RBPs, the basis for specificity is weaker than for protein-recognizing RBPs, and we have not yet assessed RBPs that target the O antigen or the capsule. Next, we will confirm binding and injection by wet experiments in human primary cells (R13) and in non-target bacteria such as bacteria of the normal flora and *Salmonella* in the environment (R14, R21). How lethal a cell with a hole in it is has not been tested, and because there are no data, we judged the severity of R21 as Severe.

### **2.4. Resistance to SUNRISE**

Corresponding Risk ID: R15

In our discussion with Dr. Matsunaga of the JIHS AMR Clinical Reference Center, we learned that even when a new antimicrobial is developed, treatment options are lost again once resistant bacteria appear against it. For SUNRISE too, we considered it necessary to examine the possibility that resistance to SUNRISE itself is acquired.

Acquiring resistance is not necessarily a one-sided benefit for bacteria, and is known to come with a decrease in growth rate or ability to adapt to the environment (fitness cost)[7]. From the mechanism of SUNRISE, we assumed four routes of escape and examined the burden each may carry, based on related studies.

**Table. 11.1.1.** Routes of escape from SUNRISE and the expected burden

| Route of escape | Expected burden |
| :---- | :---- |
| Amino acid substitution in the target protein | Because a conserved region is targeted, a substitution that abolishes binding is likely to impair enzyme function as well |
| Increased expression of the target protein | Gene amplification and increased copy number are unstable, and examples of a growth burden have been reported |
| Loss of ClpXP | Stress tolerance and virulence decrease, and the ability to sustain infection in the bladder is thought to fall |
| Alteration of the adhesion molecule | If a molecule whose loss weakens the bacterium is chosen, a disadvantage may arise, but how often such mutations occur is unknown |

For TPD, we aimed for a design that targets a conserved region shared by multiple aminoglycoside phosphotransferases. If we can recognize a functionally important conserved region, a substitution that avoids binding to the Binder may also lower the function of the enzyme as a resistance factor. Melnikov and colleagues, through comprehensive mutational analysis of APH(3′)II, showed that there are amino acid positions that are important for maintaining resistance[8]. For avoidance by increased expression of the target protein, instability and burden associated with higher gene copy number have also been reported[9].

Losing ClpXP, which is required for degradation by TPD, is also conceivable as a route of escape. However, ClpXP is involved in the homeostasis of bacteria, for example in degrading RpoS, a central regulator of the stress response[10]. It has indeed been reported that Clp protease deletion strains are little affected under ordinary growth conditions but show lower survival under starvation[11].

For CPI, a change in the receptor on the bacterial surface may let the bacterium avoid recognition by the RBP. From our discussion with Dr. Kiga of JIHS, we learned the importance of choosing receptors that are conserved, exposed on the surface, and whose mutation impairs the function of the bacterium. This idea is shared with phage steering, in which acquiring phage resistance leads, for example, to recovery of antibiotic susceptibility. For a phage that recognizes OprM, a component of the efflux pump of *Pseudomonas aeruginosa*, it has been reported that antibiotic susceptibility increased as phage resistance was acquired[12]. There is also a study in which combining phages that recognize different receptors delayed the appearance of resistant bacteria[13].

Based on these findings and our discussion with Dr. Kiga, we set the following as design guidelines: for TPD, target a functionally important conserved region; for CPI, prioritize receptors whose mutation may disadvantage the bacterium; do not restrict adhesion to a single target but prepare several tail fibers; and use SUNRISE together with an antibiotic. However, these ideas are based mainly on phage studies and have not been confirmed for CPI. In addition, some adhesion molecules allow escape not by mutation but by reversible switching of expression, and such molecules should not be chosen.

Furthermore, mutations can arise even in a conserved region. Estimating from the number of bacteria in the bladder, we think that bacteria carrying a mutation in part of the target may exist even before treatment. We therefore took the position of assuming that resistance to SUNRISE will arise, and of considering what happens to the bacteria that escape. Not every acquisition of resistance carries a fitness cost, and compensatory mutations may reduce the cost[7], so we treat this analysis as a hypothesis to be tested first in future passaging experiments and evolutionary models. The evidence for each route and the details of the evolutionary model are described on the [Model](http://LINK_TO_MODEL_5) page.

Next, we will measure how often resistant mutants appear by passaging experiments, follow the bacterial count and susceptibility during treatment, and change the target or the tail if susceptibility falls (R15).

### **2.5. Biosecurity and Misuse Prevention**

Corresponding Risk IDs: R07, R22

A major strength of SUNRISE is its modularity and versatility. By changing the Binder, the RBP and the Cargo, it can address a variety of resistance proteins and target bacteria. However, this feature can also lead to intentional misuse, such as changing the CPI Cargo to a harmful protein. It has been reported in earlier work that the target recognition site and the Cargo of PVC can be changed, and dual-use risk needs to be considered[3].

Because the current CPI is produced in *E. coli*, a Cargo that is strongly toxic to *E. coli* is hard to produce. However, this constraint is lost if the production host is changed, so we concluded that the possibility of misuse must be managed from the stage of designing and choosing modules. We therefore aim for a mechanism in which the RBP and Cargo can be exchanged during research and development, while a future medical formulation fixes a combination that matches the therapeutic purpose, and in which, whenever a new module is adopted or changed, misuse risk is also assessed by the Biosecurity assessment of PSAF.

The materials we currently use are designed to contain no toxin, not to replicate, and not to recognize human cells, so we assessed that they would be unlikely to cause harm if a third party obtained them (R07). On the other hand, we have not implemented a mechanism that prevents malicious modification of Cargo at the molecular level, and we have not yet decided the scope of what we publish on the Wiki or established a review process for cargo modification(R22). Next, we will review what we publish from the point of view of how it could be misused, and consult experts and the biosafety officer of our institution. The WHO also points out the importance of assessing and managing risks of dual-use research at each stage of research and development[14].

### **2.6. Laboratory Handling and Environmental Release**

Corresponding Risk IDs: R01–R06, R16–R20

In the research stage, we only carried out closed in vitro experiments, did not use animal or human samples, and did not release anything into the environment.For production and cloning we used non-pathogenic laboratory strains of E. coli, handled recombinant E. coli under P1 containment measures, and inactivated culture fluid, tools and liquid waste before disposal.For details of handling, please see [General Laboratory Safety](http://LINK_TO_GENERAL_LAB_SAFETY).

The genus *Photorhabdus*, from which the CPI genes originate, includes strains that infect humans[15][16]. For this reason, we do not bring in live donor bacteria or the wild-type Injector, and we do not load natural toxin payloads. Under the recombinant DNA experiment plan of our institution, the donor nucleic acid is Class 1 and the containment measures are approved as P1 (R02).

For the environmental impact in the implementation stage, we assumed that most of the administered particles leave with the urine (R19). The particles do not replicate and carry no toxin, and it has been reported for another antimicrobial peptide that peptides are broken down quickly in sewage[17], but we have not measured the half-life of SUNRISE particles in the environment. We assessed the effect on animals, insects and plants as small (R16–R18), but this is not based on measurement and rests on relative comparison. Next, we will design a procedure to inactivate urine and waste before discharge and measure the half-life in the environment (R19), and if we produce at industrial scale, we will redo the environmental risk assessment (R20).

## **3. Progressive Safety Assessment Framework (PSAF)**

We considered that the safety of SUNRISE should not be examined only for individual experiments or components, but must be assessed across the whole project, from research and development through future use to production and disposal. The framework we developed for this is the Progressive Safety Assessment Framework (PSAF).

PSAF consists of five STEPs (Project Definition, Hazard Identification, Risk Scenario Identification, Risk Assessment, and Risk Control). In exploring risks, we list situations in four areas (A–D) that combine two stages, the research stage and the implementation stage, with two perspectives, Biosafety and Biosecurity, and we also distinguish who is harmed (humans, animals, plants, environment) and how the harm arises (expected or unexpected).

We applied PSAF to SUNRISE and identified 18 Hazards (H01–H18) and 22 Risk Scenarios (R01–R22). For each risk, we judged severity and likelihood and determined the risk level. Twelve risks were judged Medium or above before measures, of which seven were High and five were Medium. The remaining ten were Low or Very low.

For the twelve risks at Medium or above, we planned additional measures and judged the risk again after the measures. The results are shown in the following table.

**Table. 11.1.2.** Risks at Medium or above identified by PSAF, and their judgment after measures

| Risk ID | Description | Before measures | After measures | Main measures |
| :---- | :---- | :---- | :---- | :---- |
| R02 | Exposure of laboratory workers to constructs derived from the donor organism (*Photorhabdus*) | Medium | Medium | Not bringing in live donor bacteria, sequence verification, approved containment measures |
| R08 | Administration of a preparation containing impurities (endotoxin, host proteins, residual DNA) | High | Low | Standardized purification process and limit values, removal and measurement of endotoxin |
| R09 | Immune response to repeated doses | High | Medium | Local dosing, shortest period and fewest doses, measurement of antibody titers and cytokines |
| R10 | Deterioration or aggregation during storage and transport | High | Medium | Stability tests, setting of storage and transport conditions |
| R11 | Hemolysis and tissue damage by the Adaptor | High | Medium | Local dosing, sequence modification, measurement of hemolysis and cytotoxicity, setting of the minimum effective dose |
| R13 | CPI binding human epithelial cells by mistake | Medium | Low | Docking comparison with human glycans, binding and injection tests in human primary cells |
| R14 | Effect on bacteria of the normal flora | Medium | Low | Two-level specificity (tail and Binder), local dosing, docking and experiments with normal flora bacteria |
| R15 | Selection of mutants that escape SUNRISE | High | Medium | Targeting a conserved region, passaging experiments, monitoring during treatment |
| R19 | Spread to the environment of particles excreted in urine | Medium | Low | Inactivation before discharge, measurement of the half-life in the environment |
| R20 | Release of the host and DNA into the environment at scale-up | Medium | Low | Production in a closed system, inactivation of liquid waste, redoing the environmental risk assessment |
| R21 | Binding and injection into non-target bacteria in the environment | High | Medium | Completing relative binding comparisons, tests with non-target bacteria |
| R22 | Diversion or misuse of design information or products | High | Medium | Review of what is published, consultation with experts and the responsible officer, re-checking when the payload changes |

All judgments after measures are “predicted”. For none of them have we yet confirmed the effect of the measures by experiments or measurements. The risks that remain at Medium after measures are seven: R02, R09, R10, R11, R15, R21 and R22. For a Medium risk, we proceed only after obtaining the confirmation of the biosafety officer of our institution. These are the items we will prioritize in future verification.

The PSAF Worksheet filled in for SUNRISE is shown below.

[PSAF Worksheet filled in for SUNRISE (PDF)](https://static.igem.wiki/teams/6144/wiki/safety/psaf-worksheet-waseda-tokyo-2026.pdf)

In this way, we used PSAF not simply as a checklist for confirming safety, but as a framework for systematically exploring risks and clarifying design measures and the priorities of assessment. We also aim for the assessment procedure applied to SUNRISE to be usable in the same way in other synthetic biology projects, and we have organized it as a reproducible procedure from exploring risks to considering measures. Its background, method and reusable Worksheet are explained in detail on the [PSAF](http://LINK_TO_PSAF) page.

Scope and Limitations

PSAF does not judge a project to be “safe”. This assessment is also a design assessment at the research stage, and it does not mean actual administration or release into the environment. In iGEM, releasing or using genetically modified organisms outside the laboratory is in principle not allowed, and taking products of synthetic biology out of the laboratory requires a Check-In beforehand[18]. The guide values for severity and likelihood and the decision categories are those defined in PSAF, and judgments may differ depending on who makes them. Conformity to Japanese laws (such as the Cartagena Act) and to regulations for pharmaceuticals cannot be judged by PSAF.

## **4. Conclusion**

With the future medical application of SUNRISE in mind, we emphasized Safety and Security by Design. By combining risk exploration with PSAF and discussions with experts through Human Practices, we examined safety from the viewpoints of the protein-based composition, toxicity, target specificity, acquisition of resistance, and the possibility of misuse. In addition, through Dry Lab analyses and a literature review, we evaluated the design features and potential risks of each.

Through these efforts, we not only clarified the safety issues of SUNRISE, but also built a safety assessment process that can be applied to the design of new Adaptors and RBPs, laying the foundation for future design choices and experimental verification. Safety is not guaranteed by a single assessment; it is improved by repeating exploration of risks, design, verification and improvement. We will continue to use PSAF and keep assessing both safety and misuse risk as we develop SUNRISE.

## **References**

[1] U.S. Food and Drug Administration (2014) Immunogenicity Assessment for Therapeutic Protein Products. https://www.fda.gov/regulatory-information/search-fda-guidance-documents/immunogenicity-assessment-therapeutic-protein-products

[2] Rathore, A. S. et al. (2025) Prediction of hemolytic peptides and their hemolytic concentration. Communications Biology, 8, 176. doi: 10.1038/s42003-025-07615-w

[3] Kreitz, J. et al. (2023) Programmable protein delivery with a bacterial contractile injection system. Nature, 616, 357–364. doi: 10.1038/s41586-023-05870-7

[4] Baba, T. et al. (2006) Construction of Escherichia coli K-12 in-frame, single-gene knockout mutants: the Keio collection. Molecular Systems Biology, 2, 2006.0008. doi: 10.1038/msb4100050

[5] Tsherniak, A. et al. (2017) Defining a cancer dependency map. Cell, 170(3), 564–576. doi: 10.1016/j.cell.2017.06.010

[6] Huang, Q. et al. (2026) PaxDb v6.0: reprocessed, LLM-selected, curated protein abundance data across organisms. Nucleic Acids Research, 54(D1), D427–D439. doi: 10.1093/nar/gkaf1066

[7] Andersson, D. I. & Hughes, D. (2010) Antibiotic resistance and its cost: is it possible to reverse resistance? Nature Reviews Microbiology, 8, 260–271. doi: 10.1038/nrmicro2319

[8] Melnikov, A. et al. (2014) Comprehensive mutational scanning of a kinase in vivo reveals substrate-dependent fitness landscapes. Nucleic Acids Research, 42(14), e112. doi: 10.1093/nar/gku511

[9] Nicoloff, H. et al. (2024) Three concurrent mechanisms generate gene copy number variation and transient antibiotic heteroresistance. Nature Communications, 15, 3981. doi: 10.1038/s41467-024-48233-0

[10] Zhou, Y. et al. (2001) The RssB response regulator directly targets σS for degradation by ClpXP. Genes & Development, 15(5), 627–637. doi: 10.1101/gad.864401

[11] Weichart, D. et al. (2003) Global role for ClpP-containing proteases in stationary-phase adaptation of Escherichia coli. Journal of Bacteriology, 185(1), 115–125. doi: 10.1128/JB.185.1.115-125.2003

[12] Chan, B. K. et al. (2016) Phage selection restores antibiotic sensitivity in MDR Pseudomonas aeruginosa. Scientific Reports, 6, 26717. doi: 10.1038/srep26717

[13] Gao, D. et al. (2022) Fitness trade-offs in phage cocktail-resistant Salmonella enterica serovar Enteritidis results in increased antibiotic susceptibility and reduced virulence. Microbiology Spectrum, 10(5), e02914-22. doi: 10.1128/spectrum.02914-22

[14] World Health Organization (2022) Global guidance framework for the responsible use of the life sciences: mitigating biorisks and governing dual-use research. https://www.who.int/publications-detail-redirect/9789240056107

[15] Gerrard, J. G. et al. (2003) Photorhabdus species: bioluminescent bacteria as human pathogens? Emerging Infectious Diseases, 9(2), 251–254. doi: 10.3201/eid0902.020220

[16] Weissfeld, A. S. et al. (2005) Photorhabdus asymbiotica, a pathogen emerging on two continents that proves that there is no substitute for a well-trained clinical microbiologist. Journal of Clinical Microbiology, 43(8), 4152–4155. doi: 10.1128/jcm.43.8.4152-4155.2005

[17] Wichmann, N. et al. (2024) Hydrolysis of antimicrobial peptides by extracellular peptidases in wastewater. Environmental Science & Technology, 58, 717–726. doi: 10.1021/acs.est.3c06506

[18] iGEM Foundation. Release Beyond Containment Policy. iGEM Responsibility. https://responsibility.igem.org/safety-policies/release-beyond-containment