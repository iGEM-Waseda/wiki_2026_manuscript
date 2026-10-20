# Progressive Safety Assessment Framework (PSAF)

## 1. Why We Developed PSAF

When you run an iGEM project, safety is not only about the experiments inside the laboratory. Besides handling the organisms and genes safely, you need to think about what would happen if they left containment unintentionally, what effects the intended future use would have, and what happens during manufacture, storage, transport and disposal [^1][^2][^3]. Risks also do not arise only from accidents and unintended exposure (Biosafety). They can arise when the materials or information handled in the research are accessed inappropriately and used for a purpose other than the intended one (Biosecurity) [^1].

In iGEM, every team must submit a Safety Form, and teams are expected to address biosafety and biosecurity across the whole project, not only for the organisms and parts they use [^4]. When you actually sit down to do this, however, it is hard to see "what to look for as a risk, and how" and "how to connect the research stage to future real-world implementation in a single assessment".

We therefore built the Progressive Safety Assessment Framework (PSAF), which assesses the biosafety and biosecurity risks of a synthetic biology project through one consistent procedure, from research to future real-world implementation, on the basis of risk assessment frameworks that are already widely used internationally. PSAF gathers what those frameworks ask you to check into five STEPs and a worksheet that an iGEM team can actually work with. It is designed not only for the safety assessment of SUNRISE, the Waseda-Tokyo 2026 project, but also for use by other iGEM teams, and the [worksheet (PDF)](https://static.igem.wiki/teams/6144/wiki/safety/psaf-worksheet.pdf) we use for the assessment is public. Please use it.

For general safety management in the laboratory, see [General Laboratory Safety](https://2026.igem.wiki/waseda-tokyo/safety-and-security/#general-safety-1.-general-laboratory-safety-introduction); for the results of the safety assessment of SUNRISE, see [Project Safety](LINK_TO_PROJECT_SAFETY).

## 2. Overview of PSAF

PSAF consists of the following five STEPs. STEP 1 to STEP 3 search systematically for the risks involved in running the project, and STEP 4 and STEP 5 assess those risks and decide what to do about them.

:::c
**Table. 11.2.1.** The five STEPs of PSAF
:::
| STEP | What it does |
|---|---|
| STEP 1 — Project Definition | Set out the function, components and conditions of use of the project |
| STEP 2 — Hazard Identification | Identify who or what could be harmed, and how |
| STEP 3 — Risk Scenario Identification | Find the situations in which that harm occurs, from both the biosafety and the biosecurity side |
| STEP 4 — Risk Assessment | Decide the risk level from the consequence and the likelihood |
| STEP 5 — Risk Control | Plan measures that bring the risk down |

Whenever the design or the intended use of what you are developing changes, or you obtain new or unexpected experimental results, go back to STEP 1 and assess again. Rethinking the risks each time, as the project moves on, is what "Progressive" means in PSAF.

## 3. How PSAF Relates to Existing Frameworks

PSAF is built on two risk assessment procedures that are widely used and not specific to one country or region. In iGEM, teams are asked to consider not only the experiments in the laboratory but also how the project would be used in society [^4]. To assess both, we combined the WHO Laboratory Biosafety Manual, 4th edition (LBM4) [^1], which covers the risks that come with laboratory work (including release outside the laboratory and transport), with Cartagena Protocol Annex III [^2], which covers the effects of deliberately using genetically modified organisms in the environment outside the laboratory. Both set out a common procedure: identify the harmful properties, evaluate the likelihood and the consequence, judge whether the risk is acceptable, and apply control measures. PSAF takes these as its basis and rearranges them into five STEPs.

:::c
**Table. 11.2.2.** How each PSAF STEP maps onto the existing frameworks
:::
| PSAF | WHO LBM4 [^1] | Cartagena Protocol Annex III [^2] |
|---|---|---|
| STEP 1 | Gather information (Step 1) | Characterization of the recipient organism, vector, insert, intended use and receiving environment (paragraph 9) |
| STEP 2 | Hazard identification, within gathering information (Step 1) | Identification of characteristics that may cause adverse effects (paragraph 8(a)) |
| STEP 3 | How exposure and release occur, within risk evaluation (Step 2) | Consideration of the level and kind of exposure (paragraph 8(b)) |
| STEP 4 | Risk evaluation and determination of the acceptable risk (Step 2) | Evaluation of the likelihood and the consequences, and estimation of the overall risk (paragraphs 8(b)–(d)) |
| STEP 5 | Develop a risk control strategy (Step 3); select and implement risk control measures (Step 4); review risks and risk control measures (Step 5) | Judgement on the acceptability of the risk and how to manage it (paragraph 8(e)); handling uncertainty (paragraph 8(f)) |

In PSAF we added biosecurity at the implementation stage to the perspectives these two frameworks cover [^3][^4], and arranged the whole as a single table of four combinations of stage (research, implementation) and biosafety or biosecurity. This lets a team check, through one procedure, the biosafety and biosecurity risks that an iGEM project has to consider, from laboratory experiments to future real-world implementation.

## 4. How to Use PSAF

### STEP 1 — Project Definition: Set out what the project is

To judge what could become a harmful effect, first set out the function, the components and the conditions of use of the project [^2].

:::c
**Table. 11.2.3.** What to write in STEP 1
:::
| Item | What to write | Example |
|---|---|---|
| Engineered Function | The intended function and the mechanism that produces it (including how the parts behave once combined) | Fluoresces when it detects a target substance in urine (intended as a home test kit) |
| Biological Components | Chassis, genes, proteins and vectors, with their origin and known properties | An *E. coli* K-12 derivative (generally of low pathogenicity); a plasmid carrying the detection circuit and an antibiotic-resistance marker |
| Conditions of use | The experiments at the research stage and the way it would be used at the implementation stage (who uses it, where, how, and how it is disposed of). Write the current experiments and the future assumption separately | Research stage: culture and fluorescence measurement in the laboratory. Implementation stage: a user tests urine at home and throws the kit away as waste |

### STEP 2 — Hazard Identification: Identify who or what could be harmed, and how

To search for harms systematically, arrange them in a table of who or what is harmed (rows) against how the harm arises (columns) [^2]. In each cell, leave the route aside and write in the form "property or behaviour of the organism or part → possible harm". A cell is not limited to one entry. Write out every harm you can think of, and give each one a Hazard ID (H01…). For each harm, state the conditions under which it arises (who is exposed, by what route, in what amount) as far as you can explain them from published data or from your own results; the examples below are written in that way.

:::c
**Table. 11.2.4.** The STEP 2 table
:::
| Who or what | Expected harm<br/>From known properties (toxicity, pathogenicity, allergenicity and so on) and from the function working as designed | Unexpected harm<br/>From behaviour that departs from the design: mutation, loss of function, unforeseen interactions, horizontal gene transfer and so on |
|---|---|---|
| **People** (researchers, users, patients, people nearby) | e.g. Antibiotic-resistance marker in the live cells → if the strain causes an infection (for example through a wound), treatment options are limited (H01) | e.g. Loss of function in the detection circuit → delayed care after a false negative (H02)<br/>Incorrect fluorescence after a mutation → an unnecessary visit after a false positive (H03) |
| **Animals** (livestock, pets, wildlife, insects) | (Left empty in this example: no harm was identified under the conditions of use in Table 11.2.3) | e.g. Colonization of the gut by the strain → a change in the gut microbiota (H04) |
| **Plants** (crops, wild plants) | (Left empty in this example: no harm was identified under the conditions of use in Table 11.2.3) | e.g. Colonization of the rhizosphere by the strain → a change in the rhizosphere microbial community (H05) |
| **Environment** (microbial communities, water, soil, ecosystems) | e.g. The ability of the strain to multiply → competition with native microorganisms (H06) | e.g. Horizontal transfer of the resistance gene → resistance in environmental bacteria (H07) |

Where a component has a known harmful property such as toxicity or pathogenicity, that property is inherent and always present, so it belongs under "expected" [^5]. Write out a harm even if you think it unlikely, as long as you cannot rule it out. If you cannot yet explain the conditions under which a harm would arise, do not drop it silently: record it and mark it "more information needed" in STEP 4. Leave a cell empty only after you have considered it and found no harm.

### STEP 3 — Risk Scenario Identification: Find the situations in which harm occurs

For each harm identified in STEP 2, think about when and how it would arise, from both the research stage and the implementation stage and from both the biosafety and the biosecurity side [^3]. Where several routes are conceivable for one harm, write each route out as a separate situation and give each one a Risk ID (R01…).

:::c
**Table. 11.2.5.** The four areas in STEP 3
:::
| | Biosafety (unintended exposure or release) | Biosecurity (loss, theft, unauthorized access, misuse) |
|---|---|---|
| **Research stage** | **A**: Accidents and exposure during experiments, storage and disposal<br/>e.g. Spilling culture medium on the bench (R01)<br/>Pouring waste down the sink before inactivation (R02) | **B**: Loss, theft or unauthorized access to research materials and information<br/>e.g. The storage unit has no lock and strains can be taken out without a record (R03) |
| **Implementation stage** | **C**: Undesirable effects during manufacture, transport, use and disposal (including side effects during treatment)<br/>e.g. A user leaves the kit in a hot car (R04)<br/>A used kit goes into household waste as it is (R05) | **D**: Diversion or misuse of the product, the technology or the information<br/>e.g. Cells are taken out of the kit and used for another purpose (R06) |

Write each situation as one sentence: what happens, and by what route the harm arises. For H02, for example, write "a user leaves the kit in a hot car, the detection circuit stops working, and the user believes the false negative and delays seeking care" (R04). As in STEP 2, write out a situation even if you think it unlikely, as long as you cannot rule it out. For B and D, write which materials or information are involved, under what controls they are held, and how hard it would be to turn them into harm. Do not write the method of misuse itself.

### STEP 4 — Risk Assessment: Decide the risk level

To decide which risks to address first, take each situation from STEP 3 and assess the consequence of the harm and the likelihood that the harm arises through that situation; the two together give the risk level [^1]. In STEP 4, assess the risk as it stands with the control measures that are already in place at the time of assessment.

In PSAF we worked from the LBM4 approach of evaluating risk from the consequence and the likelihood [^1], and wrote the guides below so that assessments do not drift between assessors. For the consequence, we drew on the severity grading of CTCAE [^6] for people, and on the four levels of 2002/623/EC [^5] for the populations and ecosystems of animals, plants and the environment (we merged Low and Negligible, neither of which implies a significant change, into Negligible). Those four levels describe populations and ecosystems, so a serious harm to a single animal could be rated low simply because the population is hardly affected. For animals we therefore added a separate guide for harm to an individual animal, which is PSAF's own and is modelled on the grading used for people. For animals, assess both the individual and the population or ecosystem, and take the higher level. For the likelihood, we drew on the factors that LBM4 lists as raising the likelihood: the nature of the procedure, the stability of the material, the competency of personnel and the condition of the facilities [^1]. The likelihood is that of the harm identified in STEP 2 actually arising through the route you wrote in STEP 3, not merely that of exposure to the material. For the biosecurity situations (B and D), the intent of a person who would misuse the material is hard to judge, so we judge from the evidence of the state of the controls over materials and information, which the WHO Laboratory biosecurity guidance [^7] emphasizes, and from how hard it would be to turn them into harm.

:::c
**Table. 11.2.6.** Guide to the consequence
:::
| Level | People [^6] | Animals: harm to an individual (PSAF's own guide) | Populations and ecosystems: animals, plants, environment [^5] |
|---|---|---|---|
| **Severe** | Hospitalization is required, self-care is lost, life is at risk, or death follows (CTCAE Grade 3–5 as a guide). Or it spreads from person to person and a major public health impact is expected | An individual animal (for example livestock or a pet) dies unintentionally or is severely disabled, even if the effect on the population is small | The population of a species or the functioning of the ecosystem changes greatly and does not readily return |
| **Moderate** | Minor medical intervention is required and part of daily activity is limited (Grade 2 as a guide) | Veterinary treatment is required and the animal's normal activity or production is partly limited | Populations change substantially, but no species is lost and recovery is possible |
| **Negligible** | There are no symptoms, or they are mild, and no treatment is required (Grade 1 as a guide) | There are no symptoms, or they are mild, and no treatment is required | There is no meaningful change in populations or in the functioning of the ecosystem |

For animals, assess both columns and take the higher level.

Assess the likelihood that the harm identified in STEP 2 arises through the route written in STEP 3.

:::c
**Table. 11.2.7.** Guide to the likelihood
:::
| Level | Biosafety (A and C) | Biosecurity (B and D) |
|---|---|---|
| **Likely** | Under the conditions of work and use you assume, the route readily occurs and leads to the harm, and no effective measure or condition that would stop the harm can be confirmed | Under the misuse you assume, the harm could readily follow: the materials or information can be reached by people who could misuse them, and no effective control, or barrier to turning them into harm, can be confirmed |
| **Possible** | The route could occur and lead to the harm, but it is held in check by measures already in place or by the conditions the harm requires | The assumed misuse could lead to the harm, but it is held in check by the controls in place or by what it takes to turn the material or information into harm; if those were breached, harm could follow |
| **Unlikely** | You can explain concretely, from the properties of the material, the conditions of use and the effect of the measures, why the route is unlikely to occur or unlikely to lead to the harm | You can show, from the state of the controls and from how hard it would be to turn the material or information into harm, that the assumed misuse is unlikely to lead to the harm, even if the material were obtained |

Record the evidence for each assessment: experimental data, published work, the measures already in place, and so on. Where the evidence is not enough, write "more information needed". Cartagena Protocol Annex III states that a lack of knowledge is not to be taken as evidence that a risk is absent or acceptable, and that uncertainty is to be addressed by gathering further information or by control measures [^2]. In PSAF, therefore, we provisionally choose the level that makes the risk higher until we have gathered the information and assessed again. If, for instance, there are no data on how far a condition worsens when a false negative delays care, and you cannot decide between Moderate and Severe, mark it "more information needed" and provisionally choose Severe.

From these two assessments, the LBM4 risk assessment matrix (Table 11.2.8) gives the risk level.

:::c
**Table. 11.2.8.** Risk assessment matrix (LBM4 Table 2.5 [^1])
:::
| Consequence ＼ Likelihood | Unlikely | Possible | Likely |
|---|:---:|:---:|:---:|
| **Severe** | Medium | High | Very high |
| **Moderate** | Low | Medium | High |
| **Negligible** | Very low | Low | Medium |

LBM4 asks you to judge risks as acceptable, controllable or unacceptable, but leaves it to each organization to decide which levels count as acceptable [^1]. Use the categories in Table 11.2.9 as a reference and settle them with the biosafety officer at your institution before you begin the assessment.

:::c
**Table. 11.2.9.** Risk levels and decision categories (PSAF defaults)
:::
| Risk level | Category | What to do |
|---|---|---|
| Very high・High | Unacceptable | Bring it down to Medium or below with control measures. If it cannot be brought down, change the design or do not carry out that work or that use |
| Medium | Controllable | This band also contains Severe × Unlikely, so put measures in place and proceed once the biosafety officer at your institution has confirmed them |
| Low・Very low | Acceptable | Proceed under the current controls |

### STEP 5 — Risk Control: Plan measures that bring the risk down

For every risk assessed as Medium or above, plan additional control measures and assess the residual risk again with the same matrix. Where the effect of a measure has not yet been confirmed, mark the result "predicted" and treat it as provisional until the effect can be confirmed [^1][^2].

:::c
**Table. 11.2.10.** What to write in STEP 5
:::
| Item | What to write | Example (care delayed after a false negative) |
|---|---|---|
| Measure | What you will do, and whether it is already in place or planned | Add a control that reads "invalid" when the cells are not working (planned) |
| Evidence and verification | Why the measure should work, and how its effect will be checked | If the cells degrade, the control does not fluoresce either, so the user notices the false negative. Check with deliberately degraded kits that the control does not fluoresce |
| Residual risk | The level reassessed with the same matrix. Mark it "predicted" where the effect is unconfirmed | Predicted: Severe × Unlikely ＝ Medium (not final until the effect of the control, and the chance of the control itself failing, have been checked) |

Choose measures from the five main strategies for risk reduction that LBM4 sets out. Where elimination and reduction are not possible, use isolation, and combine strategies where necessary [^1].

:::c
**Table. 11.2.11.** Strategies for risk reduction (LBM4 Table 2.6 [^1]) and examples in synthetic biology
:::
| Strategy | What it means | Example |
|---|---|---|
| Elimination | Eliminate the hazard | Switch to a reagent-only detection method that uses no live cells |
| Reduction and substitution | Reduce the risk (use less, or substitute something safer) | Replace the antibiotic-resistance marker with an auxotrophic marker |
| Isolation | Isolate the hazard | Seal the kit and build in a mechanism that kills the cells after use |
| Protection | Protect personnel and the environment | Culture in a biological safety cabinet; wear gloves and a lab coat |
| Compliance | Administrative controls and management of the biosafety programme | Write an SOP for inactivating waste and train people on it; lock the storage unit and record what is taken out |

If the risk is still High or above after the measures, add further measures or replace them with more effective ones [^1]. If it still does not come down, change the design and return to STEP 1.

## 5. Scope and Limitations

PSAF does not determine that a project is "safe". It is a framework for making clear what you have checked and how far you have brought the risk down.

:::c
**Table. 11.2.12.** What PSAF can and cannot do
:::
| Item | What PSAF can do | What PSAF alone cannot do |
|---|---|---|
| Risk Identification | Systematically identify hazards and risk scenarios from both the biosafety and the biosecurity side | Prove that no unknown hazard exists |
| Risk Assessment | Decide a risk level with an established matrix and state the evidence | Reach a final judgement on safety without experimental data or expert assessment |
| Implementation | Set out in advance what has to be considered for manufacture, use and disposal | Guarantee or approve the safety of administration, environmental release or industrial use |
| Regulation | Identify where legal regulation, ethical review or expert assessment is needed | Judge compliance with the law, or stand in for review by a regulatory authority |

Assessing the implementation stage does not mean that administration to a subject or release into the environment actually takes place. iGEM does not permit the release or use of genetically modified organisms outside the laboratory, and a Check In is required before any product of synthetic biology is taken outside the laboratory [^8]. The guides to consequence and likelihood (including the guide to harm to an individual animal) and the decision categories are ones that PSAF itself sets, and assessments may differ between assessors. We will look into this by having other teams use PSAF as well.

## 6. PSAF Worksheet — Try It on Your Project

<div style="display: flex; justify-content: center; margin: 24px auto;">
 <iframe src="https://static.igem.wiki/teams/6144/wiki/safety/psaf-worksheet.pdf" width="80%" height="800px"></iframe>
</div>

It brings together the entry fields for STEP 1 to STEP 5 with the guides to the levels and the risk assessment matrix. Print it, or fill it in with the annotation tools of a PDF reader. Please try it on your own team's project. If you do use it, we would be grateful if you cited the PSAF of iGEM Waseda-Tokyo 2026 as the source.

### Example: PSAF applied to SUNRISE

Below is the worksheet of the Waseda-Tokyo 2026 project, SUNRISE, filled in with PSAF.

<div style="display: flex; justify-content: center; margin: 24px auto;">
 <iframe src="https://static.igem.wiki/teams/6144/wiki/safety/psaf-worksheet-waseda-tokyo-2026.pdf" width="80%" height="800px"></iframe>
</div>

[^1]: World Health Organization. (2020) Laboratory Biosafety Manual, 4th edition. Geneva: WHO. https://www.who.int/publications/i/item/9789240011311
[^2]: Secretariat of the Convention on Biological Diversity. (2000) Cartagena Protocol on Biosafety to the Convention on Biological Diversity, Annex III: Risk Assessment. Montreal. https://www.cbd.int/doc/legal/cartagena-protocol-en.pdf
[^3]: World Health Organization. (2022) Global guidance framework for the responsible use of the life sciences. Geneva: WHO. https://www.who.int/publications/i/item/9789240056107
[^4]: iGEM Foundation. (2026) Judging: Medals; Special Awards (Safety and Security Award). iGEM Competition 2026. https://competition.igem.org/judging/awards/medals , https://competition.igem.org/judging/awards/special
[^5]: European Commission. (2002) Commission Decision 2002/623/EC establishing guidance notes supplementing Annex II to Directive 2001/18/EC on the deliberate release into the environment of genetically modified organisms. Official Journal of the European Communities L 200, 22-33. https://eur-lex.europa.eu/legal-content/EN/TXT/?uri=CELEX:32002D0623
[^6]: National Cancer Institute. (2025) Common Terminology Criteria for Adverse Events (CTCAE), Version 6.0. https://dctd.cancer.gov/research/ctep-trials/for-sites/adverse-events/ctcae-v6.pdf
[^7]: World Health Organization. (2024) Laboratory biosecurity guidance. Geneva: WHO. https://www.who.int/publications/i/item/9789240095113
[^8]: iGEM Foundation. Release Beyond Containment Policy. iGEM Responsibility. https://responsibility.igem.org/safety-policies/release-beyond-containment
