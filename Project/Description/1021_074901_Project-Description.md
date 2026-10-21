# Introduction

Antimicrobial resistance (AMR) occurs when microorganisms such as bacteria acquire resistance to antimicrobial agents, making these drugs less effective. It is an increasingly serious global public health challenge [^1]. We became acutely aware of this problem when a family member of one of our team members developed an infection caused by antimicrobial-resistant bacteria. Although susceptibility testing was performed for 18 antimicrobial agents, the bacteria were susceptible to only five. Some of these remaining options also raised concerns about severe side effects, making treatment particularly challenging. This experience showed us that AMR is not merely a future threat: it is already depriving patients of treatment options and causing considerable anxiety for patients and their families. In response, Waseda-Tokyo 2026 set out to develop Safety-enhanced UNconventional Resensitization through Injection and Selective Elimination (SUNRISE), a novel synthetic biology-based therapeutic approach that integrates two modules, with the aim of bringing a new “dawn” to the uncertain fight against AMR.

Our project combined [*in silico* design and evaluation](https://2026.igem.wiki/waseda-tokyo/model/) of the modules that make up SUNRISE with [Wet Lab](https://2026.igem.wiki/waseda-tokyo/results/) experiments to test their feasibility. We then incorporated experimental measurements from the Wet Lab into [Mathematical Modeling](https://2026.igem.wiki/waseda-tokyo/model/) to evaluate the effectiveness and feasibility of the integrated SUNRISE system. With eventual administration in mind, we also assessed [safety](https://2026.igem.wiki/waseda-tokyo/safety-and-security/), including toxicity and specificity, and examined in vivo dynamics, administration strategies, manufacturing methods, and market potential to explore the prospects for [clinical implementation](https://2026.igem.wiki/waseda-tokyo/human-practices/). Throughout the project, we continuously incorporated stakeholder feedback through [Human Practices](https://2026.igem.wiki/waseda-tokyo/human-practices/) to refine SUNRISE—from identifying challenges in AMR treatment and developing our project concept to exploring clinical implementation.

![](https://static.igem.wiki/teams/6144/wiki/description/description.avif =500x) 

:::c

Fig. 1.1. Overview of the SUNRISE Project Workflow

:::

# Problem — Limitations of Current Resensitization Strategies

We first visited the AMR Clinical Reference Center at the Japan Institute for Health Security (JIHS), which provides specialist support for AMR control, to discuss the current state of AMR. When antimicrobial agents are used, susceptible bacteria are eliminated, while resistant bacteria survive and are free to multiply. In addition to acquiring new resistance through mutation, bacteria can exchange resistance genes across strains through horizontal gene transfer, including plasmid-mediated transfer [^2]. Resistance therefore not only emerges but also spreads within bacterial populations, allowing bacteria resistant to previously effective drugs to become more widespread. Bacterial AMR was estimated to have directly caused approximately 1.14 million deaths worldwide in 2021, and this annual figure is projected to rise to approximately 1.91 million by 2050 [^1]. We learned that although infection prevention and appropriate antimicrobial use are essential, these measures alone cannot adequately address the ongoing burden of drug-resistant infections. Alongside new antimicrobial agents, new treatment strategies are needed for patients whose infections no longer respond to existing drugs [^3].

![](https://static.igem.wiki/teams/6144/wiki/description/image-720.avif =700x) 

:::c

Fig. 1.2. Global Burden and Future Projections of Antimicrobial Resistance

:::  
Our discussion also highlighted a fundamental dilemma: antimicrobial agents are indispensable to modern medicine, yet their use can promote the emergence and spread of resistant bacteria. This underscored the value of preserving existing drugs as treatment options, rather than relying on new drugs alone. This led us to explore “resensitization” — restoring bacterial susceptibility to previously ineffective antimicrobial agents. To learn how this approach is being pursued in drug development, we visited Meiji Seika Pharma, which is tackling AMR by restoring the effectiveness of existing antimicrobial agents. One approach to resensitization is to inhibit resistance-conferring proteins, including those that degrade or inactivate antimicrobial agents or modify the drugs’ targets [^2]. The company is pursuing this approach by developing inhibitors of β-lactamases, resistance proteins that degrade β-lactam antibiotics [^4]. These inhibitors must bind in a way that impairs protein function, for example by targeting active sites or substrate-binding sites [^5].

![](https://static.igem.wiki/teams/6144/wiki/description/fig1-3-1-1024.avif =500x) 

:::c

Fig. 1.3. Mechanisms of Antibiotic Resistance and Resensitization by Inhibitors

:::  
However, discussions with representatives from Meiji Seika Pharma revealed that inhibitor-based resensitization also faces challenges. Resistance proteins comprise diverse types and variants [^2]. Even among proteins that confer resistance to the same antimicrobial agent, mutations can produce differences in active-site structure, making it difficult for a single inhibitor to cover a broad range of targets [^5]. When an inhibitor is effective against only a limited set of resistance proteins, additional inhibitors are needed for those it cannot address. Yet developing new antimicrobial agents is costly, while their use is restricted to patients who need them to limit the emergence of resistance. Inhibitors targeting specific resistance proteins have an even narrower eligible patient population, making it difficult to recover development costs [^6]. We recognized both technical and economic challenges in continually developing inhibitors for diverse resistance proteins.

Inspired by this interview, we considered whether we could target a broader range of surface regions on resistance proteins—not just functional sites such as active sites and substrate-binding sites—to overcome these limitations of inhibitors. We focused on the possibility of targeting surface structures shared by multiple resistance proteins, allowing a single molecule to recognize multiple targets and potentially achieve resensitization. Binding to a region not directly involved in function may not sufficiently inhibit a resistance protein, but using that interaction to remove the protein from the cell could eliminate its activity.

We therefore chose to degrade resistance proteins themselves rather than directly inhibit their function through binding.

![](https://static.igem.wiki/teams/6144/wiki/description/fig1-4-1-1024.avif =500x) 

:::c

Fig. 1.4. From Inhibition to Degradation of Resistance Proteins

:::

# Our Solution

## Targeted Protein Degradation Module

To eliminate resistance proteins inside bacterial cells, we developed the [Targeted Protein Degradation (TPD) Module](https://2026.igem.wiki/waseda-tokyo/design/).

Our TPD Module builds on CLIPPERs, a previously reported approach that selectively degrades target proteins expressed in bacterial cells by recruiting them to the endogenous bacterial protease complex ClpXP [^7]. The module uses an Adaptor composed of three components joined into a single polypeptide: a Binder that binds to the target resistance protein, an Anchor that recognizes ClpXP, and a Linker connecting the two. Together, these components recruit the resistance protein to ClpXP for selective degradation [^7].

In this approach, binding of the Binder does not itself need to inhibit the target protein’s function [^7]. Potential binding sites are therefore not restricted to active sites or substrate-binding sites but can include a wider range of surface regions. This is a key advantage of TPD: regions that are difficult to exploit for functional inhibition with conventional inhibitors can still serve as candidate binding sites for inducing protein degradation.

![](https://static.igem.wiki/teams/6144/wiki/description/fig1-1.avif =500x) 

:::c

Fig. 1.5. Schematic Overview of the TPD Module

:::  
We first tested whether degrading a resistance protein could restore antimicrobial susceptibility in the [Wet Lab](https://2026.igem.wiki/waseda-tokyo/results/). We directly fused the Anchor, a degradation-inducing tag, to the kanamycin resistance enzyme APH(3')-IIa in order to promote its intracellular degradation. This restored susceptibility to kanamycin, demonstrating that degradation of a resistance protein can enable antimicrobial resensitization.

![](https://static.igem.wiki/teams/6144/wiki/description/description-tpd.avif =700x)

:::c

Fig. 1.6. Experimental Validation of Resensitization Through Protein Degradation

:::  
To move beyond the limitations of inhibitors, we also developed an [*in silico* design pipeline](https://2026.igem.wiki/waseda-tokyo/model/) aimed at targeting multiple resistance proteins and their variants with a single Adaptor. First, we align the three-dimensional structures of multiple resistance proteins using FoldMason to identify conserved surface structures [^8]. Next, we use BindCraft to design Binders for these regions [^9] and construct structural models of complete Adaptors by combining each Binder with a Linker and an Anchor. We then use simulations to evaluate the predicted binding of the designed Adaptors to multiple resistance proteins.

This pipeline allows us to design and evaluate Adaptor candidates *in silico* against regions shared by multiple resistance proteins before testing numerous protein–Binder combinations individually in the Wet Lab. Using this approach, we designed Adaptor candidates predicted to bind both ArmA and RmtB, two distinct proteins that confer resistance to aminoglycoside antibiotics [^10].

In addition to targeting surface structures shared by multiple resistance proteins, we also anticipate the need to address new variants that existing Adaptors may not adequately recognize. The TPD Adaptor has a modular architecture consisting of a Binder, a Linker, and an Anchor. If such variants emerge, we can use our pipeline to redesign the Binder while retaining the Linker and Anchor, enabling us to explore Adaptor candidates for the new targets.

![](https://static.igem.wiki/teams/6144/wiki/description/1.avif =700x)

:::c

Fig. 1.7. In Silico Design Pipeline for Multi-Target Adaptors

:::

## Cargo Protein Injection Module

Even if TPD can degrade resistance proteins, therapeutic application requires the Adaptor to be delivered into the target bacterial cells.

Through discussions with Dr. Kiga at the National Institute of Infectious Diseases, JIHS, who researches treatments for drug-resistant bacteria, we learned that introducing nucleic acids encoding the Adaptor into bacteria raises safety considerations, including the persistence and unintended spread of genetic information. To keep genetic information out of the treatment entirely, we developed the [Cargo Protein Injection (CPI) Module](https://2026.igem.wiki/waseda-tokyo/design/) to deliver the Adaptor itself directly as a protein, rather than introducing nucleic acids that encode it.

The CPI Module is based on the Photorhabdus virulence cassette (PVC), a protein injection system. PVC is composed of proteins and has been shown to deliver its loaded protein cargo, rather than nucleic acids, directly into eukaryotic cells [^11]. Its tail fibers recognize target cells, and modifying these fibers allows the target to be changed [^11]. In wild-type PVC, Pdp1 is a naturally loaded cargo protein whose N-terminal region serves as a loading signal required for incorporation into the injector. Fusing this signal to the N terminus of a protein of interest has been reported to enable the loading and delivery of various proteins [^11]. We aim to use this mechanism in CPI to recognize target bacteria and inject the Adaptor directly into their cells.

![](https://static.igem.wiki/teams/6144/wiki/description/10-19cpi.avif =500x) 

:::c

Fig. 1.8. Schematic Overview of the CPI Module

:::  
In the Dry Lab, we first developed an *in silico* design pipeline to modify tail fibers for bacterial targeting and to predict and evaluate their three-dimensional structures. In the Wet Lab, we then constructed a modified Injector designed in the Dry Lab that incorporates the T7 phage tail fiber protein gp17, which recognizes *Escherichia coli* BL21(DE3) [^12]. We also confirmed that proteins fused to the Pdp1-derived loading signal required for cargo loading could retain their function inside cells.

![](https://static.igem.wiki/teams/6144/wiki/description/fig-1-9.avif =700x)

:::c

Fig. 1.9. Design and Construction of the Modified Injector

:::  
However, clinically relevant bacteria are not limited to a single type. Through discussions with Professor Tsuneda of the Department of Life Science and Medical Bioscience at Waseda University, we learned that bacterial surface structures can vary between strains of the same species, making it difficult for a single modified tail fiber to recognize diverse clinical strains [^13].

Our Dry Lab work expanded the range of candidate bacterial targets. We simulated interactions between candidate receptor-binding proteins (RBPs), including tail fibers, and the surface structures of clinically encountered *E. coli* strains. Using these analyses, we constructed a [Targeting Library](https://2026.igem.wiki/waseda-tokyo/model/) to support the selection of suitable RBPs for each bacterial target. This library allows us to explore and select candidate RBPs according to the surface structures of different bacteria. Through this approach, we aim to develop a CPI Module that is not limited to a single bacterial type.

![](https://static.igem.wiki/teams/6144/wiki/description/fig10-table-library.avif =500x)

:::c

Fig. 1.10. Targeting Library for Selecting Receptor Binding Proteins

:::

## SUNRISE — The Integrated System

[SUNRISE](https://2026.igem.wiki/waseda-tokyo/design/) is our therapeutic platform for AMR, integrating the TPD and CPI Modules.

In the proposed system, the CPI Injector recognizes the target bacterium and delivers the TPD Adaptor into the cell. The Adaptor then recruits the resistance protein for ClpXP-mediated degradation. By reducing the amount of resistance protein, we aim to restore susceptibility to existing antimicrobial agents.

SUNRISE is designed to allow the resistance protein selected for degradation to be changed by modifying the TPD Adaptor, while the bacterial delivery target can be changed by modifying the CPI tail fiber. This ability to design the two modules independently is a defining feature of SUNRISE’s approach to addressing diverse forms of AMR.

![](https://static.igem.wiki/teams/6144/wiki/description/10-19.avif =500x)

:::c

Fig. 1.11. Proposed Mechanism of the Integrated SUNRISE System

:::  
However, even if CPI and TPD each function individually, the integrated SUNRISE system may not necessarily function as a therapy. For example, even when the Adaptor can degrade the resistance protein, an insufficient amount of Adaptor delivered into bacterial cells may prevent adequate restoration of antimicrobial susceptibility.

To test whether the two modules work as one system, we developed an [Integrated Mathematical Model](https://2026.igem.wiki/waseda-tokyo/model/) that links the SUNRISE dose to the amount of Adaptor delivered into bacterial cells, the subsequent reduction in intracellular resistance protein levels, the resulting change in antimicrobial susceptibility, and ultimately the inhibition of bacterial growth in the presence of an antimicrobial agent. Beyond evaluating the feasibility of SUNRISE as a whole, this model can identify factors that limit its performance by examining the capabilities of each module. Before experimentally integrating the modules, we can use the model to identify which aspects of module performance—such as delivery efficiency or protein degradation efficiency—are insufficient and quantify the improvements needed for SUNRISE to function. The model predicted that SUNRISE-mediated resensitization could be achieved under conditions based on the experimental data.

The Integrated Mathematical Model thus enables us to predict the feasibility of the complete SUNRISE system computationally. By identifying the components that require improvement and the performance targets needed for resensitization, it also provides concrete guidance for future development.

Fig. 1.12. Integrated Mathematical Model of SUNRISE

# Safety by Design

We incorporated [safety](https://2026.igem.wiki/waseda-tokyo/safety-and-security/) considerations into SUNRISE from the design stage, with eventual administration in the body and clinical implementation in mind.

SUNRISE is designed to be administered as an all-protein system centered on the TPD Adaptor and the CPI Injector. The Injector itself consists of proteins and can deliver protein cargo directly [^11]. This design would allow SUNRISE to reduce resistance protein activity without introducing new genetic information into target bacteria during treatment. SUNRISE itself also cannot self-replicate. These features are intended to reduce risks associated with introducing genetic information and with self-replication.

With in vivo administration in mind, we evaluated the potential toxicity of SUNRISE’s protein components *in silico* to assess possible risks. Achieving both broad target coverage and high specificity is also important for SUNRISE. For the TPD Adaptor, we assessed binding to regions shared by multiple resistance proteins while simulating interactions with non-target intracellular bacterial proteins to evaluate the potential for off-target interactions. For the CPI Injector, we compared interactions with target bacteria and human cells to assess the potential for binding to non-target cells following administration in the body.

By adopting an all-protein system that does not introduce nucleic acids and using Dry Lab analyses to assess toxicity and specificity from an early stage, we have integrated safety assessment into SUNRISE’s development. These efforts support the design of a system intended to combine effectiveness with safety.

# Implementation

For SUNRISE to be used clinically, it must be delivered in sufficient amounts to the site of infection in the body and be safe to administer.

Discussions with Dr. Kiga at the National Institute of Infectious Diseases, JIHS, led us to consider local administration directly to infection sites, such as the urinary tract, lungs, and skin, as a promising delivery strategy for SUNRISE. Using local administration to the urinary tract as a model case, we developed a mathematical model that accounts for immune effects, clearance from the infection site, and the acquisition of resistance. We used the model to simulate SUNRISE’s dynamics and therapeutic effects. We also varied the SUNRISE dose and dosing interval, as well as the dose of the co-administered antimicrobial agent, to explore the conditions required for a therapeutic effect.

Building on these results, we examined a concrete scenario for the [clinical implementation](https://2026.igem.wiki/waseda-tokyo/human-practices/) of SUNRISE using an Adaptor designed in the Dry Lab. This Adaptor was predicted to bind a structural region shared by ArmA and RmtB. We selected difficult-to-treat urinary tract infections caused by drug-resistant *E. coli* harboring ArmA or RmtB as our model indication.

For this model indication, we prepared a Target Product Profile (TPP), a planning document that defines a product’s intended characteristics and use during drug development [^14]. We comprehensively considered the target patient population, route of administration, dosage, efficacy, and safety, as well as manufacturing, storage, supply, and market potential.

The TPP developed for this case can serve as an example for planning the clinical implementation of future SUNRISE applications targeting other resistance proteins, drug-resistant bacteria, and diseases. The same process can be used to systematically assess performance requirements, administration conditions, safety, manufacturing, and market potential, supporting more efficient development.

![](https://static.igem.wiki/teams/6144/wiki/description/hp1.avif =500x)

:::c  
Fig. 1.13. Toward Clinical Implementation of SUNRISE  
:::

# Conclusion

Waseda-Tokyo 2026 proposes SUNRISE, a therapeutic platform for AMR that combines TPD-mediated degradation of resistance proteins with CPI-mediated delivery of the Adaptor directly into target bacteria as a protein.

In the Dry Lab, we identified structures shared by multiple resistance proteins and use them to guide Adaptor design. We also design and select tail fibers according to the target bacterium. Through these efforts, we aim to build a platform in which the resistance protein targeted for degradation and the bacterium targeted for delivery can be changed independently. 

We assessed the feasibility of the complete SUNRISE system by combining Wet Lab proof-of-concept experiments with the Integrated Mathematical Model. With eventual administration in the body in mind, we also evaluated safety considerations, including toxicity and specificity, from the design stage.

We will further develop SUNRISE into a modular and programmable therapeutic platform that can be redesigned by modifying the Adaptor and tail fiber to address the diversity and continued evolution of AMR, rather than a treatment limited to a particular resistance protein or bacterium.

SUNRISE will bring a new “dawn” to the fight against AMR.

![](https://static.igem.wiki/teams/6144/wiki/description/fig16-1024.avif =700x)

:::c

Fig. 1.14. SUNRISE: A Modular Platform for Antimicrobial Resensitization

:::

[^1]: GBD 2021 Antimicrobial Resistance Collaborators. (2024). Global burden of bacterial antimicrobial resistance 1990–2021: a systematic analysis with forecasts to 2050. *The Lancet*, 404(10459), 1199–1226. [https://doi.org/10.1016/S0140-6736(24)01867-1](https://doi.org/10.1016/S0140-6736(24)01867-1)

[^2]: Davies, J., & Davies, D. (2010). Origins and evolution of antibiotic resistance. *Microbiology and Molecular Biology Reviews*, 74(3), 417–433. [https://doi.org/10.1128/MMBR.00016-10](https://doi.org/10.1128/MMBR.00016-10)

[^3]: World Health Organization. (2024). WHO releases report on state of development of antibacterials. [https://www.who.int/news/item/14-06-2024-who-releases-report-on-state-of-development-of-antibacterials](https://www.who.int/news/item/14-06-2024-who-releases-report-on-state-of-development-of-antibacterials)

[^4]: Meiji Seika Pharma Co., Ltd. (2025). Submission of New Drug Application for the Novel β-Lactamase Inhibitor, Nacubactam in Japan. [https://www.meiji.com/global/news/2025/pdf/251226_01.pdf](https://www.meiji.com/global/news/2025/pdf/251226_01.pdf)

[^5]: Tehrani, K. H. M. E., & Martin, N. I. (2018). β-Lactam/β-lactamase inhibitor combinations: an update. *MedChemComm*, 9(9), 1439–1456. [https://doi.org/10.1039/C8MD00342D](https://doi.org/10.1039/C8MD00342D)

[^6]: World Health Organization. (2020). Update from WHO and Pew Charitable Trusts: urgent action needed to accelerate antibiotic development. [https://www.who.int/news/item/07-07-2020-update-from-who-and-pew-charitable-trusts-urgent-action-needed-to-accelerate-antibiotic-development](https://www.who.int/news/item/07-07-2020-update-from-who-and-pew-charitable-trusts-urgent-action-needed-to-accelerate-antibiotic-development)

[^7]: Izert-Nowakowska, M. A., Klimecka, M. M., Antosiewicz, A., et al. (2025). Targeted protein degradation in Escherichia coli using CLIPPERs. *EMBO Reports*, 26(16), 3994–4016. [https://doi.org/10.1038/s44319-025-00510-9](https://doi.org/10.1038/s44319-025-00510-9)

[^8]: Gilchrist, C. L. M., Mirdita, M., & Steinegger, M. (2026). Multiple protein structure alignment at scale with FoldMason. *Science*, 391(6784), 485–488. [https://doi.org/10.1126/science.ads6733](https://doi.org/10.1126/science.ads6733)

[^9]: Pacesa, M., Nickel, L., Schellhaas, C., et al. (2025). One-shot design of functional protein binders with BindCraft. *Nature*, 646(8084), 483–492. [https://doi.org/10.1038/s41586-025-09429-6](https://doi.org/10.1038/s41586-025-09429-6)

[^10]: Wachino, J.-I., Doi, Y., & Arakawa, Y. (2020). Aminoglycoside resistance: Updates with a focus on acquired 16S ribosomal RNA methyltransferases. *Infectious Disease Clinics of North America*, 34(4), 887–902. [https://doi.org/10.1016/j.idc.2020.06.002](https://doi.org/10.1016/j.idc.2020.06.002)

[^11]: Kreitz, J., Friedrich, M. J., Guru, A., et al. (2023). Programmable protein delivery with a bacterial contractile injection system. *Nature*, 616(7956), 357–364. [https://doi.org/10.1038/s41586-023-05870-7](https://doi.org/10.1038/s41586-023-05870-7)

[^12]: Garcia-Doval, C., & van Raaij, M. J. (2012). Structure of the receptor-binding carboxy-terminal domain of bacteriophage T7 tail fibers. *Proceedings of the National Academy of Sciences*, 109(24), 9390–9395. [https://doi.org/10.1073/pnas.1119719109](https://doi.org/10.1073/pnas.1119719109)

[^13]: Mourosi, J. T., Awe, A., Guo, W., et al. (2022). Understanding bacteriophage tail fiber interaction with host surface receptor: The key “blueprint” for reprogramming phage host range. *International Journal of Molecular Sciences*, 23(20), 12146. [https://doi.org/10.3390/ijms232012146](https://doi.org/10.3390/ijms232012146)

[^14]: World Health Organization. (n.d.). Target Product Profiles, preferred product characteristics and target regimen profiles. [https://www.who.int/our-work/science-division/research-for-health/optimizing-research-processes/product-profiles](https://www.who.int/our-work/science-division/research-for-health/optimizing-research-processes/product-profiles)