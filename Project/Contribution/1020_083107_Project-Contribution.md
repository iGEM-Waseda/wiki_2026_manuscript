# Contribution

## Introduction

We believe that the development of the iGEM community and synthetic biology depends on documenting the research findings and experiences gained through trial and error throughout our projects in a way that others can easily understand, and passing them on to future generations. With this in mind, Waseda-Tokyo 2026 aimed to share the knowledge and results gained through the development of SUNRISE in a form that future iGEM teams can apply to their own projects. Through the tools, frameworks, and resources presented on this page, we hope that future iGEMers will be able to reuse and improve upon our work, building on it to develop new research projects and activities.

## Engineering Tools

Waseda-Tokyo 2026 developed SUNRISE, a new therapeutic platform designed to address the global challenge of antimicrobial resistance (AMR). SUNRISE consists of two versatile modules: the TPD Module, which degrades target proteins inside bacteria, and the CPI Module, which delivers proteins into bacterial cells. We therefore organized, documented, and shared our design methods and functional evaluation tools in an accessible format so that future iGEMers can use them both to develop SUNRISE further by integrating the two modules to target diverse resistant bacteria and to create new projects using either module independently.

### TPD Design Pipeline

We developed the TPD Design Pipeline, which provides an integrated workflow for identifying structural regions shared by multiple resistance proteins, designing Adaptors that bind to these regions, and evaluating their safety. When targeting a single resistance protein, users can skip the search for shared structural regions and begin directly with Adaptor design. Furthermore, we believe this pipeline can be applied not only to resistance proteins but also to a wide range of other proteins within E. coli. To enable future iGEMers to design and evaluate Adaptors against their chosen target proteins, we compiled detailed instructions for each step in the guide below. We hope this pipeline will provide a foundation for new research that goes beyond combating AMR by enabling the degradation of specific bacterial proteins and the reduction of their functions. For further details, please refer to [the Model page](https://2026.igem.wiki/waseda-tokyo/model/).

<div style="display: flex; justify-content: center; margin: 24px auto;">  
<iframe src="PDFのリンク" width="80%" height="800px"></iframe>  
</div>

### CPI Retargeting Pipeline and Library

We developed the CPI Retargeting Pipeline to enable CPI Injectors to target diverse antibiotic-resistant bacteria. This pipeline provides an integrated workflow, from identifying Receptor-Binding Proteins (RBPs) corresponding to target bacteria to designing their incorporation into the Injector and evaluating binding and receptor accessibility in silico. Furthermore, to achieve broad coverage of clinically important E. coli strains associated with AMR, we constructed a Targeting Library containing RBP candidates that recognize O-antigens, outer membrane proteins, and other bacterial surface structures. This library not only allows users to select from existing RBP candidates but can also be expanded by identifying and adding new RBPs corresponding to additional target bacteria. To enable future iGEMers to design and evaluate Injectors tailored to their target bacteria, we compiled detailed instructions for each step in the guide below. We hope this pipeline and library will provide a foundation for new research beyond AMR, supporting the delivery of proteins into a wide range of bacterial targets. For further details, please refer to [the Model page](https://2026.igem.wiki/waseda-tokyo/model/).

<div style="display: flex; justify-content: center; margin: 24px auto;">  
<iframe src="PDFのリンク" width="80%" height="800px"></iframe>  
</div>

### SUNRISE Integrated Mathematical Modeling

To evaluate the functionality of the complete SUNRISE system integrating TPD and CPI, we developed an Integrated Mathematical Model that describes the entire process, from Adaptor delivery and resistance protein degradation to the restoration of antibiotic susceptibility and suppression of bacterial growth. This model enables us to predict changes in bacterial populations over time based on the binding affinity between the Adaptor and resistance proteins, the binding affinity between the Injector RBP and the bacterial surface, and the concentrations of SUNRISE and antibiotics. We also provide an interactive simulator that allows users to visually examine changes in bacterial populations over time while adjusting individual parameters. This enables users to identify factors limiting the overall performance of SUNRISE and quantitatively determine which properties need to be improved, and to what extent, before integrating the individual modules. We hope that future iGEMers seeking to improve SUNRISE and further contribute to addressing AMR will use this tool to evaluate system performance and optimize their designs. For further details, please refer to [the Model page](https://2026.igem.wiki/waseda-tokyo/model/).

## Project Development Frameworks & Tools

Advancing an iGEM project requires addressing a wide range of challenges beyond research and development, including exploring pathways toward real-world implementation, improving the project based on stakeholder feedback, and ensuring safety. Through the development of SUNRISE, Waseda-Tokyo 2026 developed frameworks and tools to systematically address these challenges. We then organized, documented, and shared these frameworks and tools in an accessible format to help future iGEMers conduct their own projects safely and effectively.

### DAWN Process — Human Practices Framework

In Human Practices activities, it is important to understand societal needs and challenges through dialogue with stakeholders and incorporate the insights gained into research and development. However, it is not always clear how to translate stakeholder feedback into research decisions and use it for continuous improvement. We therefore developed the DAWN Process, a framework that structures Human Practices around an iterative cycle of four guiding questions. DAWN consists of defining the problem (Define), assessing alternatives (Assess), incorporating insights into research (Weave), and identifying the next challenge (Navigate). By repeating this cycle, teams can connect dialogue with society to research decisions and continuously improve their projects. To help future iGEMers systematically conduct Human Practices in their own projects, we shared the principles of the DAWN Process and practical guidance on how to apply it. We hope this framework will serve as a guide for incorporating diverse stakeholder perspectives into research and developing projects that reflect societal needs. For further details, please refer to [the Human Practices page](https://2026.igem.wiki/waseda-tokyo/human-practices/).

### Target Product Profile (TPP)

Bringing a pharmaceutical product into real-world use requires more than laboratory-based technological development. It is also necessary to define requirements for efficacy, safety, manufacturing, and supply based on the needs of patients and healthcare professionals. We therefore developed a Target Product Profile (TPP) that outlines the development goals necessary for the clinical implementation of SUNRISE, drawing on insights gained through discussions with healthcare professionals, regulatory authorities, companies, and members of the public. This allowed us to clarify the challenges that must be addressed and the performance requirements that must be achieved to move SUNRISE toward clinical application. To help future iGEMers not only advance the clinical development of SUNRISE more efficiently but also apply this approach to other pharmaceutical development projects, we shared our TPP and the considerations that informed its development. We hope these resources will serve as a guide for other iGEM teams seeking to translate their research findings into real-world healthcare applications. For further details, please refer to [the Human Practices page](https://2026.igem.wiki/waseda-tokyo/human-practices/).

<div style="display: flex; justify-content: center; margin: 24px auto;">  
<iframe src="PDFのリンク" width="80%" height="800px"></iframe>  
</div>

### Lab Safety Certification

Before beginning laboratory experiments, it is essential for every team member to understand the laboratory's safety rules and demonstrate their knowledge. However, the equipment, experimental procedures, and safety requirements vary between laboratories, making it necessary to provide safety training tailored to each environment. We therefore developed Lab Safety Certification, a web application that allows teams to create and administer knowledge assessment tests based on their laboratory's safety manuals. By using an external AI service to generate questions from the manuals and having administrators review and register them, teams can create tests tailored to their laboratories. The application also integrates test-taking, automatic grading, review of explanations, and administrator monitoring of members' understanding into a single web-based platform. To help future iGEM teams conduct laboratory-specific safety training efficiently and create an environment in which new members can begin experiments safely, we made the source code and instructions for use publicly available. For further details, please refer to [the Safety and Security page](https://2026.igem.wiki/waseda-tokyo/safety-and-security/) and [the Software page](https://2026.igem.wiki/waseda-tokyo/software/).

### Progressive Safety Assessment Framework (PSAF)

When assessing the safety of an iGEM project, it is necessary to evaluate risks from both biosafety and biosecurity perspectives, considering not only laboratory experiments but also potential future real-world implementation. However, it is not always clear which risks should be identified and evaluated or what procedures should be followed. We therefore developed the Progressive Safety Assessment Framework (PSAF), based on internationally recognized risk assessment frameworks, to systematically evaluate safety from the project design stage through potential future implementation. PSAF organizes the process of identifying risks, assessing them, and developing risk mitigation measures into five steps. It enables teams to examine both biosafety and biosecurity risks during the research and implementation stages and to update their assessments as their projects progress. To help future iGEMers apply PSAF to their own projects, we published a guide detailing the procedures for each step, along with a worksheet for recording assessment results. We hope this framework will help identify potential risks in diverse synthetic biology projects and contribute to safer research and development. For further details, please refer to [the Safety and Security page](https://2026.igem.wiki/waseda-tokyo/safety-and-security/).

<div style="display: flex; justify-content: center; margin: 24px auto;">  
<iframe src="PDFのリンク" width="80%" height="800px"></iframe>  
</div>

## Outreach & Fundraising

For synthetic biology to advance, it is important to create more opportunities for people to become interested in the field, deepen their understanding, and participate in it. iGEM provides an important opportunity for students to engage in synthetic biology research and build connections with society, and we believe that sustaining and expanding these activities can make a significant contribution to the broader adoption of synthetic biology. Waseda-Tokyo 2026 therefore engaged in educational activities to raise awareness of AMR and synthetic biology, as well as fundraising through building relationships with companies to support the continued development of our project. To help future iGEMers conduct similar activities and sustain and develop their own projects, we organized and shared the educational materials we used, along with the fundraising experience and practical knowledge we gained through trial and error.

### AMR Educational Materials

Addressing antimicrobial resistance (AMR) requires not only the development of new therapeutic technologies but also greater public awareness of the seriousness of AMR and the appropriate use of antibiotics. We therefore conducted educational activities on AMR for elementary and junior high school students at UniLab, a hands-on science event organized by Waseda University. During this event, we introduced the seriousness of AMR, the appropriate use of antibiotics, and potential new solutions offered by synthetic biology. We also incorporated yeast observation activities and quizzes to help children learn in an engaging and enjoyable way. To enable future iGEMers to conduct similar educational activities, we made the educational materials used during the event publicly available in English. We hope these materials will support AMR education activities by iGEM teams around the world and contribute to raising awareness and understanding of AMR among a wider audience.

<div style="display: flex; justify-content: center; margin: 24px auto;">  
<iframe src="PDFのリンク" width="80%" height="800px"></iframe>  
</div>

### Fundraising Resources

Participating in iGEM requires substantial funding, including team registration fees and competition participation expenses. However, in Japan, individual charitable giving accounts for only 0.23% of nominal GDP, approximately one-seventh of the proportion in the United States (1.55%)[^1], making it difficult for student teams to fund their activities through donations alone. Waseda-Tokyo 2026 also began fundraising with almost no team funds and little knowledge of how to approach companies for financial support. We therefore explored various methods, including contacting companies with which we had no prior connections by email or phone, participating in synthetic biology-related events, organizing networking events jointly with other teams, and seeking introductions from our academic advisors. We recorded both the processes and outcomes of these efforts.

Through this experience, we learned that corporate support often begins through personal connections and that it is important to present proposals in a format that companies can easily evaluate internally. Based on these experiences, we compiled a fundraising guide covering response rates for different contact methods, the process through which companies consider sponsorship proposals, the differences between donations and sponsorships, conditions to confirm when receiving support, and key points to review when entering into agreements. We made this guide publicly available in both Japanese and English.

Although the guide was developed primarily for iGEM teams in Japan, we believe that similar environments exist in other countries and regions where raising funds through donations is difficult and building relationships with companies is essential for fundraising. We hope this guide will also help iGEM teams operating in such environments identify fundraising approaches suited to their own circumstances.

<div style="display: flex; justify-content: center; margin: 24px auto;">  
<iframe src="PDFのリンク" width="80%" height="800px"></iframe>  
</div>

<div style="display: flex; justify-content: center; margin: 24px auto;">  
<iframe src="PDFのリンク" width="80%" height="800px"></iframe>  
</div>

[^1]: Japan Fundraising Association. (2021). Giving Japan 2021: Infographic (2020 statistics). [https://jfra.jp/pdf/gj2020_infographic.pdf](https://jfra.jp/pdf/gj2020_infographic.pdf?utm_source=chatgpt.com) (Accessed October 20, 2026).

