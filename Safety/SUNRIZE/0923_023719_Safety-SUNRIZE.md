# **Progressive Safety Assessment Framework**

## **1. Why We Developed PSAF**

When conducting an iGEM project, safety cannot be considered only in terms of experiments performed inside the laboratory. It is necessary to consider not only whether the organisms and genes used in the project can be handled safely, but also what could happen if they unintentionally leave containment, what effects could arise when the technology is used for its intended future application, and how safety can be maintained throughout manufacturing, storage, transport, and disposal.

In addition, Risks arising from a project are not limited to those caused by accidental release or exposure. Risks may also arise when Materials used or produced during research, designed Functions, or publicly available Information are inappropriately Accessed and used for purposes other than those originally intended. Therefore, project safety must consider both Biosafety Risks arising from accidents or unintended exposure and Biosecurity Risks arising from inappropriate Access or use.

In iGEM, all teams are required to submit a Safety Form and to address biosafety and biosecurity not only for the organisms and parts they use but throughout the entire project [^5]. However, when teams actually attempt to assess project safety, it can be difficult to determine what should be identified as a Risk and how risks should be assessed consistently from the experimental stage through future implementation. Existing guidelines also differ in their objectives and scope, making it difficult to organize the safety of an entire iGEM project using a single guideline.

Therefore, we organized the common concepts found in existing international guidelines and developed the **Progressive Safety Assessment Framework (PSAF)** as a **Framework for consistently assessing Biosafety and Biosecurity Risks in iGEM synthetic biology projects, from laboratory research through future implementation**. PSAF is not a Framework designed only for Waseda-Tokyo2026's project, SUNRISE. By examining project stages and project components using the same procedure, **other iGEM teams can also systematically explore project-specific Risks and assess their safety.**

&nbsp;

## **2. Design of PSAF**

PSAF was not created from scratch as an independent checklist. Instead, we organized existing concepts presented by WHO, ISO, the Cartagena Protocol, and OECD, and integrated the Risk Assessment principles described in these documents into a format that can be applied to iGEM synthetic biology projects from the research stage through future implementation. The guidelines used as references are summarized below.

:::c

**Table 1. Guidelines and Frameworks Referenced in the Design of PSAF**

:::

| Guideline / Framework | Original Scope and Key Concepts | Concepts Incorporated into PSAF |
| ----- | ----- | ----- |
| WHO Laboratory Biosafety Manual, 4th edition [^1] | Focuses on biosafety in laboratories handling biological agents. It adopts an evidence- and risk-based approach in which risk assessment is performed before experimental work begins and appropriate risk control measures are selected according to each activity and situation. | This concept forms the basis of PSAF Stage 1 — Contained Research Safety. Rather than assessing laboratory activities using uniform rules alone, PSAF examines the actual Hazard and Exposure and determines the necessary Controls. The principle of evidence-based Safety Assessment was also incorporated into Evidence & Uncertainty within the Five Assessment Elements. |
| ISO 35001:2019 — Biorisk management for laboratories and other related organisations [^2] | Applies to laboratories and related organizations handling hazardous biological materials and describes a continuous management process for identifying, assessing, controlling, and monitoring biorisk. It addresses not only experimental Work but also storage, transport, disposal, and other activities, managing biorisk from both biosafety and biosecurity perspectives. | This concept was reflected in the overall PSAF process of continuously performing Risk Identification → Assessment → Control → Review rather than ending the process once a Risk has been identified. It was also incorporated into the design of Stage 4, which extends assessment beyond research procedures to storage, transport, and disposal, as well as into the consideration of Risks related to Access to and management of Materials. |
| Cartagena Protocol on Biosafety, Annex III — Risk Assessment [^3] | Provides a risk assessment methodology for evaluating the potential adverse effects of Living Modified Organisms (LMOs) on the receiving environment and human health. It sequentially considers identification of potential adverse effects, likelihood considering exposure, consequence, risk management, and uncertainty. It also considers information such as the recipient organism, vector, insert, introduced modification, intended use, and receiving environment. | This was a major reference for structuring the evaluation of Risk Scenarios in PSAF. In particular, the concept of assessing not only the properties of a Hazard but also the Exposure Scenario and Consequence was incorporated into the Five Assessment Elements. The approach of exploring Risks from multiple information sources, such as organisms, vectors, introduced functions, and intended use, was also used in designing the Three Hazard Sources. |
| OECD Safe(r)-by-Design / Safe and Sustainable by Design [^4] | Developed primarily in the context of innovation involving nanomaterials and advanced materials, this approach emphasizes reducing risk and uncertainty from the early stages of innovation rather than assessing Safety only after development has been completed. It also considers the entire product life cycle, from R\&D through production, use, recycling, and disposal. | This concept was incorporated into the Four Safety Stages, which progressively expand the scope of Safety Assessment beyond the laboratory to future Intended Use and the life cycle. It also informed the iterative use of PSAF, in which problems identified through Safety Assessment are fed back into the next Design cycle. |

Based on these concepts, we designed PSAF as a Three-Layer Structure.

First, the **Four Safety Stages**, which organize the stages of a project at which Risks may arise. Second, the **Three Hazard Sources**, which are used to explore where Risks may originate within each Stage. Third, the **Five Assessment Elements**, which are used to evaluate each identified Risk Scenario using the same criteria. PSAF explores and evaluates Risks arising from unintended exposure, release, inappropriate Access, unintended use, and related situations within the same Framework.

### **2.1 Four Safety Stages**

Existing guidelines assess Safety in different contexts, including laboratory biosafety, environmental exposure, intended use, and the product life cycle.

In PSAF, these contexts were organized into four Stages corresponding to the progression of an iGEM project from research toward future implementation.

:::c

**Table 2. Four Safety Stages of PSAF**

:::

| Stage | Safety Being Assessed | Central Question |
| ----- | ----- | ----- |
| Stage 1 — Contained Research Safety | Safety within a controlled research environment | Can this project be conducted safely within the laboratory? |
| Stage 2 — Unintended Exposure Safety | Unintended exposure outside containment | What could happen if research materials or products unintentionally leave containment? |
| Stage 3 — Intended-Use Safety | Safety when used for the intended application | What effects could occur to humans, organisms, or the environment during Intended Use? |
| Stage 4 — Life-cycle & Deployment Safety | Safety from manufacturing through disposal | Can safety be maintained throughout manufacturing, storage, transport, use, and disposal? |

Through these four Stages, Safety Assessment does not end within the laboratory. Instead, the scope of assessment progressively expands as the project advances.

### **2.2 Three Hazard Sources**

Defining the Stages alone does not determine which Risks should be evaluated.

Therefore, rather than listing Risks simply as they come to mind, PSAF systematically explores Risks from the same three perspectives at every Stage.

:::c

**Table 3. Three Hazard Sources Used for Risk Exploration**

:::

| Hazard Source | What to Examine | Examples |
| ----- | ----- | ----- |
| Biological Components | What does the project use or produce? | chassis, recombinant DNA, proteins, vectors, and other biological materials |
| Engineered Function | What has the system been artificially designed to do? | expression, degradation, transport, recognition, killing, signal production, etc. |
| Process / Use | How is it produced, handled, used, shared, stored, and disposed of? | cultivation, purification, administration, storage, transport, information sharing, disposal, etc. |

These three categories are PSAF-specific classifications that reorganize factors considered in existing guidelines—such as organisms, genetic modifications, introduced functions, handling, intended use, receiving environments, and life cycles—into a format that is easier to use for Risk Exploration in iGEM projects. This classification is based on the Cartagena Protocol, which considers factors such as the recipient organism, vector, insert, resulting characteristics, intended use, and receiving environment during risk assessment.

By examining the Three Hazard Sources, the Risks that actually require assessment can be identified.

### **2.3 Five Assessment Elements**

After Risks have been identified through Risk Exploration, each Risk is evaluated using five common elements.

:::c

**Table 4. Five Assessment Elements Used for Risk Assessment**

:::

| Assessment Element | What Is Assessed |
| ----- | ----- |
| Hazardous Property | Which property of the Component, Function, or Process could cause a harmful effect? |
| Exposure / Access Scenario | Who or what could be exposed to the Hazard, through what route or under what conditions, or who could intentionally Access the Material, Function, or Information? |
| Consequence | What effects could occur if the exposure, Access, or unintended use takes place? |
| Control | How can Exposure, inappropriate Access, or the resulting Consequence be reduced? |
| Evidence & Uncertainty | What experiments, models, literature, or expert knowledge support the assessment, and what remains unknown? |

This assessment method is based on concepts from the Cartagena Protocol, which considers Hazard identification, likelihood accounting for exposure, consequence, risk management, and uncertainty, as well as ISO 35001, which describes the identification, assessment, control, and monitoring of risk.

Importantly, Risk should not be judged solely on the basis of the existence of a Hazard. A more specific Safety Assessment requires examining whether there is an actual Scenario in which exposure to the Hazard could occur, whether Material, Function, or Information could be Accessed, and what Consequences could arise as a result.

&nbsp;

## **3. How to Use PSAF**

PSAF can be used from the project design stage as a worksheet for identifying gaps in Safety and connecting those gaps to additional experiments, modeling, literature review, and consultation with experts. An example of how PSAF was applied to Waseda-Tokyo2026's SUNRISE project can be found here.

### **3.1 Step 1 — Explore Risks from the Three Hazard Sources**

First, clearly define the project as it exists at that point in time. For each Stage, define the Biological Components being used, the Engineered Function being introduced, and the Intended Use ultimately envisioned for the project.

Stage 1 addresses the experiments that are actually being conducted or planned at the present time. Stage 2 considers what could happen if those materials leave containment. Stage 3 defines the future conditions under which the technology is intended to be used. Stage 4 assumes that the technology is actually manufactured and operated and considers the entire life cycle. In each Stage, if Risks could also arise from inappropriate Access to or unintended use of Material, Function, or Information, these possibilities should be considered within the same Stage. If these definitions are unclear, the subsequent Safety Assessment will also remain unclear. When the Project Design changes, the assessment should be revisited starting from these definitions.

Risks can then be systematically explored by completing the following Risk Exploration Sheet.

:::c

**Table 5. PSAF Risk Exploration Sheet**

:::

| Stage | Biological Components | Engineered Function | Process / Use | Identified Risk Scenarios |
| ----- | ----- | ----- | ----- | ----- |
| Stage 1 — Contained Research |  |  |  |  |
| Stage 2 — Unintended Exposure |  |  |  |  |
| Stage 3 — Intended Use |  |  |  |  |
| Stage 4 — Life-cycle & Deployment |  |  |  |  |

First, complete the three Hazard Source columns from left to right. Then, identify factors that could realistically lead to harmful outcomes and record them as Risk Scenarios in the rightmost column. Through this process, Risks can be systematically explored from the components of the project rather than simply listed as they come to mind, while incorporating both Biosafety and Biosecurity.

### **3.2 Step 2 — Assess Each Risk Scenario**

Each identified Risk Scenario is then examined individually using the Five Assessment Elements.

For example, rather than treating the Component “genetically modified *E. coli*” itself as the Risk and ending the assessment there, the evaluator should sequentially determine which properties of the recombinant *E. coli* constitute a Hazardous Property, through what routes it could reach humans or the environment, what Consequences could occur, which Controls could reduce those consequences, and how much Evidence is available.

Similarly, Biosecurity Risks involving inappropriate Access to Materials or Information should be assessed using the same elements: what constitutes the Hazardous Property, who could Access it and how, what Consequences could result from that Access or use, and what Controls would be required.

When multiple Risk Scenarios are identified, the same assessment is repeated for each Risk Scenario. The results are ultimately organized into a Matrix consisting of the Five Assessment Elements × Four Safety Stages.

:::c

**Table 6. PSAF 5 × 4 Safety Matrix**

:::

| Safety Stage | Hazardous Property | Exposure / Access Scenario | Consequence | Control | Evidence & Uncertainty |
| ----- | ----- | ----- | ----- | ----- | ----- |
| Stage 1 — Contained Research Safety |  |  |  |  |  |
| Stage 2 — Unintended Exposure Safety |  |  |  |  |  |
| Stage 3 — Intended-Use Safety |  |  |  |  |  |
| Stage 4 — Life-cycle & Deployment Safety |  |  |  |  |  |

If multiple Risk Scenarios are identified within a single Stage, additional rows can be added as needed within that Stage. This Matrix allows users to visually identify not only which Stages have undergone Safety Assessment, but also Risks for which no Control exists, Risks for which Evidence is insufficient, and Risks associated with substantial uncertainty.

### **3.3 Step 3 — Use the Gaps to Improve the Project**

In PSAF, the presence of an empty field is not itself considered a failure.

For example, if “no experimental data” is entered under Evidence & Uncertainty, this indicates that an additional Wet Lab experiment is needed. If the Exposure Scenario is unknown, modeling, literature review, or Consultation with experts may be required. If inappropriate Access cannot be adequately prevented, the management of Materials or the way Information is shared may need to be reconsidered. If a serious Risk is identified for which no appropriate Control can be established, the Design itself may need to be changed.

In this way, PSAF is not used as a checklist for confirming Safety only at the end of a project. Instead, it is a Framework for connecting the results of Safety Assessment to the next Design or Experiment. When the Project Design or Intended Use changes, the same Sheet should be reviewed again and the Risk Exploration and Risk Assessment updated.

&nbsp;

## **4. Scope and Limitations of PSAF**

PSAF is a starting point for systematically organizing the types of Safety Assessment required in an iGEM project. However, the use of PSAF itself does not guarantee the safety of a Project or Product.

The role of PSAF is to identify potential Risks and clarify what additional assessment or expert evaluation is required. Therefore, it is necessary to distinguish between what can be evaluated using PSAF and what cannot be determined using PSAF alone.

:::c

**Table 7. Scope and Limitations of PSAF**

:::

| Item | What PSAF Can Do | What PSAF Alone Cannot Do |
| ----- | ----- | ----- |
| Risk Identification | Systematically identify potential Hazards and Risks, including both Biosafety and Biosecurity, from multiple perspectives such as Biological Components, Engineered Function, and Process / Use. | Demonstrate that no unknown Hazards exist. |
| Risk Assessment | Organize Exposure or Access Scenarios, potential impacts, Controls, and the need for additional assessment for identified Risks. | Make a final determination of actual safety without experimental data or expert evaluation. |
| Access and Misuse | Organize Risks that may arise from inappropriate Access to or unintended use of Material, Function, or Information, and consider necessary management measures or additional assessments. | Predict every possible form of inappropriate use in advance or guarantee that such use will not occur. |
| Implementation | Anticipate future use, manufacturing, storage, transport, disposal, and other activities and organize the safety issues that should be considered in advance. | Guarantee that patient administration, environmental release, industrial use, or other implementation is safe, or authorize such implementation. |
| Regulation | Identify areas in future implementation where legal regulation, ethical review, expert evaluation, or other forms of oversight will be required. | Make a final determination of compliance with laws and regulations in individual countries or regions, or substitute for approval by regulatory authorities. |

It is particularly important to distinguish between compliance with the Safety Policy of the iGEM Competition and Safety Assessment conducted with future real-world implementation in mind. In iGEM, wet-lab projects are generally conducted at the experimental stage, and the use of engineered organisms or synthetic biology products outside the laboratory must comply with the iGEM Safety Policy.

Therefore, considering Intended Use and Deployment in Stage 3 and Stage 4 of PSAF does not mean that the project will actually administer the technology to patients or release it into the environment. Instead, these Stages examine what Risks could arise if the technology were implemented in the future and what safety considerations should already be incorporated at the current Design stage.

In other words, PSAF is not a Framework for determining that **“this Project is safe.”** Rather, it is a Framework for clarifying **“what must be examined from a safety perspective.”** PSAF is also not a fixed Safety Check that is performed once and then completed. When the Project Design, experimental results, Intended Use, Materials used, Information disclosed, or knowledge obtained from experts is updated, the Assessment should be reviewed accordingly. By repeatedly applying PSAF, newly emerging Biosafety and Biosecurity Risks and gaps in assessment can be continuously identified as the Project develops, and these findings can be connected to subsequent Safety Assessment activities, including additional experiments, Design modifications, management of Materials and Information, Consultation with experts, and investigation of regulatory requirements.

[^1]: World Health Organization. *Laboratory Biosafety Manual, 4th edition.* Geneva: World Health Organization; 2020.

[^2]: International Organization for Standardization. *ISO 35001:2019 — Biorisk management for laboratories and other related organisations.* Geneva: ISO; 2019.

[^3]: Secretariat of the Convention on Biological Diversity. *Cartagena Protocol on Biosafety to the Convention on Biological Diversity.* Montreal: Secretariat of the Convention on Biological Diversity; 2000. Annex III: Risk Assessment.

[^4]: OECD. *Sustainability and Safe and Sustainable by Design: Working Descriptions for the Safer Innovation Approach.* OECD Series on the Safety of Manufactured Nanomaterials and other Advanced Materials. Paris: OECD Publishing; 2022. doi:10.1787/a9a80171-en.

[^5]: iGEM Foundation. *Safety & Security.* iGEM Responsibility. Accessed September 21, 2026.

&nbsp;