

# 1 Introduction

# 2 BIP Overview

　We have found BIND-bearPETase (BBa_K5436124) from the various BIND-PETases listed in Tazable. 9.2.1 by performing multiple assays in the flow shown in Fig. 9.2.1. A summary of the results is shown in Table. 9.2.1.   
For the various mutant BIND-PETases designed at the beginning, Curli Fiber formation by CsgA was evaluated by performing the 9.4 Congo Red Assay and the activity of the PETase was evaluated by performing the 9.5 *p*NPB Assay.   
Those that showed Curli Fiber formation and PETase activity were further subjected to 9.6 Storage Stability Assay and 9.7 Reusability Assay. Those that showed excellent activity and reusability in these assays were further validated for PET degradation activity in the 9.8 PET Powder Degradation Assay and 9.9 PET Pellet Degradation Assay. Through these validations, we determined that “BIND-bearPETase (BBa_K5436124 ),” which we submitted as New Composite Parts, has excellent activity as a PETase, post-storage activity, and reusability.   
The results of each assay are shown in 9.4 Congo Red Assay\~9.9 PET degration Assay, and the flowchart to determine “BIND-bearPETase(BBa_K5436124)” from each mutant is shown in 9.5. The flow of determining “BIND-bearPETase (BBa_K5436124)” from each mutant is shown in Section 9.9 Discussion. 

![Experiment flow. png](https://static.igem.wiki/teams/5436/results/bipflow.png. =500x)

:::c  
**Fig. 9.2.1.** Experiment flow  
:::

:::c  
**Table. 9.2.1.** BIND-PETase varinats and an overview of their characteristics and results   
:::

| BIND-PETase variant | description | Curli Fiber Formation(9.4 Cogo Red Assay) | PETaseactivity(9.5 *p*NPB Assay) | Activity while Stored(9.7 Storage Activity Assay) | Acivity while Reused(9.7 Reusability Assay) | PET Degradation Activity |
| :---- | :---- | :---- | :---- | :---- | :---- | :---- |
| WT | Wild type sequence from *I. Sakaiensis*  | ✓  | ✓ | 4℃：increase RT：decrease | a little decrease |  |
| *E. coli* optimized | WT codon optimized for *E. coli* | ✓  | ✓  | 4℃：no significant change RT：decrease | a little decrease |  |
| 5 mut.  | 5 amino acid substitution sequence of *E. coli* optimized | ✓ (weak) | × | - | - |  |
| dura | 10 mutants of WT, with superior activity and heat tolerance | ✓  | ✓ | 4℃：increase RT：increase | increase |  |
| ID1 | ESM_PETase  | × | × | - | - |  |
| ID2 | ESM_PETase_affinity_screenig  | × | × | - | - |  |
| ID3 | ESM_PETaseaffinity_REU_screening  | ✓ (weak) | ✓ | - | - |  |
| ID4 | DuraPETase_EvoProGrad_EMS2_evocouplings_affinity_screening  | × | × | - | - |  |
| ID5 | DepoPETase_EvoProGrad_EMS2_evocouplings_affinity_screening  | × | × | - | - |  |
| ID6 | LCC_mut_IsPETase_M1M3  | × | × | - | - |  |
| ID7 | LCC_mut_IsPETase_M3  | No validation due to failed plasmid construction  |  |  |  |  |
| ID8 | LCC_mut_IsPETase_M1M2M3  | No validation due to failed plasmid construction  |  |  |  |  |
| ID22 | DepoPETase-M4_DuraPETase-M10  | ✓ | ✓ | 4℃：increase then decrease RT：increase then decrease | decrease |  |
| ID23 | DepoPETase-M2-3_DuraPETase-M10  | ✓ | ✓ | 4℃：increase RT：increase | increase |  |
| ID24 | DepoPETase-M2_DuraPETase-M10  | ✓ | ✓ | 4℃：increase RT：increase | increase |  |
| ID25 | DepoPETase-M3_DuraPETase-M10  | ✓ | ✓ | No verification due to time constraints  |  |  |
| ID26 | DepoPETase-M2-2_DuraPETase-M10  | ✓ | ✓ | No verification due to time constraints  |  |  |
| ID27 | DepoPETase-M2-1_DuraPETase-M10  | ✓ | ✓ | No verification due to time constraints  |  |  |

# 3 Confirmation of expression of BIND-PETase(WT), BIND-bearPETase

For BIND-PETase (WT), we performed SDS-PAGE and Western Blotting to evaluate whether our RBS was working properly. We also performed BIND-bearPAGE and Western Blotting. We also confirmed the expression of BIND-bearPETase in the New Composite Parts registry. For other mutants of BIND-PETase, we substituted the expression verification of BIND-PETase with the functional verification of BIND-PETase. 

## 3.1 Confirmation of expression of BIND-PETase(WT)

BIND-PETase (WT) was introduced into *E. coli* BL21 (DE3) and we tried to confirm the IPTG-induced expression by SDS-PAGE. *E. coli* were crushed and SDS-PAGE was performed, and the results are shown in Fig. 9.3.1A. A very large number of bands were identified with and without IPTG; there was no clear difference in the bands of BIND-PETase(WT) with a molecular weight of approximately 45 kDa; the BIND-PETase(WT ) band of *E. coli* BL21(DE3). It is possible that the BIND-PETase(WT) band overlapped with the endogenous protein, making it difficult to detect. Therefore, we conclude that it is difficult to confirm the expression of BIND-PETase by SDS-PAGE.  

![SDS-PAGE results for BIND-PETase (WT, E. coli optimized, 5 mut.). png](https://static.igem.wiki/teams/5436/results/results-sdspage.png =500x)

:::c  
**Fig. 9.3.1A.** SDS-PAGE results for BIND-PETase (WT, E. coli optimized, 5 mut.)   
:::  
:::c  
Two colonies each of BIND-PETase (WT, E. coli optimized, 5mut) were cultured with and without IPTG+ induction for each colony. The E. coli were crushed, proteins were extracted, and the proteins were phased. The samples were treated with HFIP treatment, which depolymerizes CsgA. BIND-PETase (*E. coli* optimized, 5mut), which was being validated at the same time, was also treated in the same way and then phased.     
:::

Therefore, Western Blotting, which can specifically detect proteins, was performed.   
The reason why no difference was detected in the bands corresponding to IPTG+/- BIND-PETase by SDS-PAGE was considered to be a problem with HFIP treatment in sample preparation prior to SDS-PAGE. So,  sonication treatment, which is more commonly used as a cell disruption method, was also performed. The results of Western Blotting are shown in Fig. 9.3.1B. Western Blotting was not performed with BIND-PETase (*E. coli* optimized, 5mut). 

![Western Blotting results for BIND-PETase(WT).png(https://static.igem.wiki/teams/5436/results/results-wb-wt.png =500x)  
:::c  
**Fig. 9.3.1B.** Western Blotting results for BIND-PETase(WT)  
:::  
:::c  
Three colonies of BIND-PETase (WT) were cultured with and without IPTG+ induction for each colony. E. coli were disrupted by HFIP or sonication, proteins were extracted, and the proteins were phased. *E. coli* BL21(DE3) were disrupted by sonication, proteins were extracted, and phased. his-tag antibody was used to detect BIND-PETase(WT).   
:::

From Fig. 9.3.1B, a band was detected around 45 kDa in the IPTG-induced sample, confirming the expression of BIND-PETase. The reason why it was difficult to confirm the expression of BIND-PETase (WT) by SDS-PAGE is that its expression level is low and it is likely to be hidden by the endogenous protein of *E. coli* BL21(DE3). This low expression of BIND-PETase may be due to the fact that BIND-PETase is a protein that is displayed on the membrane. [^1]

 

## 3.2 Confirmation of expression of BIND-bearPETase

Western blotting was also performed for BIND-bearPETase, which has a his-tag at the end of the PETase, so it was detected with a his-tag antibody in the same way as BIND-PETase (WT). The results are shown in Fig. 9.3.2. 

![Western Blotting results for BIND-bearPETase.png](https://static.igem.wiki/teams/5436/results/results-id24.png =500x)  
:::c  
**Fig. 9.3.2.** Western Blotting results for BIND-bearPETase  
:::  
:::c  
Three colonies of BIND-bearPETase were cultured and IPTG induced. *E. coli* BL21(DE3) were disrupted by sonication, proteins were extracted, and phased. his-tag antibody was used to detect BIND-bearPETase.   
:::

# 4 Congo Red Assay

　BIND-PETase requires the formation of Curli Fiber by CsgA, that PETase is displayed on the membrane surface. We evaluated this by using Congo Red, which stains Curli Fiber. If the pellet formed after the addition of Congo Red is red and the supernatant is light in color, it can be confirmed that Curli Fiber has formed normally. The results of absorbance measurement are shown in Fig. 9.4.1, and detailed results for each mutant are shown in Table. 9.4.1.   
　Of the 16 BIND-PETase variants tested in the experiment. The formation of Curli Fiber was confirmed in 12 of them. In particular, a lot of Curli Fiber was formed in BIND-PETase (WT, ID22, 25).   
　The difference in the ability of each mutant to form Curli Fiber may be due to the different expression levels of CsgA in each mutant and the different structure of PETase, which may affect the tendency of CsgA polymerization.   
   
 

 ![Intensity of Curli Fiber Formation For Each Variant]  
(https://static.igem.wiki/teams/5436/experiments/results/congo-red-assay/cr-assay-graph.png =500x)

:::c  
**Fig. 9.4.1.** Intensity of Curli Fiber Formation in each mutant   
:::

 The horizontal axis represents the mutant type, and the vertical axis represents the level of Curli Fiber formation. IPTG(+/-) samples stained with Congo Red were pelletized and the absorbance (wavelength 490 nm) indicated by Congo Red in the supernatant was measured. Curli Fiber formation was evaluated by comparing the difference in absorbance between IPTG(-) and IPTG(+) samples. The absorbance was corrected by the value of OD. The higher the value, the greater the amount of Congo Red bound to the Curli Fiber, indicating the formation of more Curli Fiber.   
   
 :::c  
**Table. 9.4.1.**  Result and analysis of the formation of Curli Fiber in each mutant  
:::

| Sample name  | formation of Curli Fiber  | Figure  (left: IPTG+, right:IPTG-)  | Analysis   |
| :---- | :---- | :---- | :---- |
| WT  | ✓  | [click this link](https://static.igem.wiki/teams/5436/experiments/results/congo-red-assay/cr-wt.png)  | The IPTG(+) pellet was stained red, and the result of the supernatant indicates that Curli Fiber has formed. |
| E. coli optimized  | ✓      | [click this link](https://static.igem.wiki/teams/5436/experiments/results/congo-red-assay/cr-e-coli-optomized.png)  | The IPTG(+) pellet was stained red, and the result of the supernatant indicates that Curli Fiber has formed.  |
| 5 mut.  | ✓(weak)      |  [click this link](https://static.igem.wiki/teams/5436/experiments/results/congo-red-assay/cr-5mut.png)  | The IPTG(+) pellet was a little stained red, and the result of the supernatant indicates that a little Curli Fiber has formed.  |
| dura  | ✓(*)      |  [click this link](https://static.igem.wiki/teams/5436/experiments/results/congo-red-assay/cr-dura.png)  | *The supernatant of the IPTG+ pellet is clear and colorless. This indicates the formation of a very large number of Curli Fiber. On the other hand, it is likely that the IPTG- sample also formed Curli Fiber for some reasons. Therefore, although the absorbance value of the supernatant is low, it is likely that more Curli Fiber has formed.   |
| ID 1  | ×  |  [click this link](https://static.igem.wiki/teams/5436/experiments/results/congo-red-assay/cr-id1.png)  | Both IPTG(+) and IPTG(-) sample pellets were not stained, and the absorbance results show that little or no number of Curli Fiber was formed. |
| ID 2  | ×  |  [click this link](https://static.igem.wiki/teams/5436/experiments/results/congo-red-assay/cr-id2.png)  | Both IPTG(+) and IPTG(-) sample pellets were not stained, and the absorbance results show that little or no number of Curli Fiber was formed.  |
| ID 3  | ✓(weak)  |  [click this link](https://static.igem.wiki/teams/5436/experiments/results/congo-red-assay/cr-id3.png)  |  IPTG(+) pellets are slightly more stained than IPTG(-) pellets. The absorbance results indicate that a small amount of Curli Fiber was formed.  |
| ID 4  | ×    |  [click this link](https://static.igem.wiki/teams/5436/experiments/results/congo-red-assay/cr-id4.png)  | Both IPTG(+) and IPTG(-) sample pellets were not stained, and the absorbance results show that little or no number of Curli Fiber was formed.    |
| ID 5  | ×    |  [click this link](https://static.igem.wiki/teams/5436/experiments/results/congo-red-assay/cr-id5.png)  | Both IPTG(+) and IPTG(-) sample pellets were not stained, and the absorbance results show that little or no number of Curli Fiber was formed. |
| ID 6  | ×    |  [click this link](https://static.igem.wiki/teams/5436/experiments/results/congo-red-assay/cr-id6.png)  | Both IPTG(+) and IPTG(-) sample pellets were not stained, and the absorbance results show that little or no number of Curli Fiber was formed.  |
| ID 22  | ✓  |  [click this link](https://static.igem.wiki/teams/5436/experiments/results/congo-red-assay/cr-id22.png)  | IPTG(+) pellets were stained dark red and the supernatant was nearly colorless. The absorbance results also indicate that a lot of  Curli Fiber was formed.   |
| ID 23  | ✓    |  [click this link](https://static.igem.wiki/teams/5436/experiments/results/congo-red-assay/cr-id23.png)  | IPTG(+) pellets were stained dark red and the supernatant was nearly colorless. The absorbance results also indicate that a lot of  Curli Fiber was formed.     |
| ID 24  | ✓  |  [click this link](https://static.igem.wiki/teams/5436/experiments/results/congo-red-assay/cr-id24.png)  | IPTG(+) pellets were stained dark red and the supernatant was nearly colorless. The absorbance results also indicate that a lot of  Curli Fiber was formed.     |
| ID 25  | ✓  |  [click this link](https://static.igem.wiki/teams/5436/experiments/results/congo-red-assay/cr-id25.png)  | IPTG(+) pellets were stained dark red and the supernatant was nearly colorless. The absorbance results also indicate that a lot of  Curli Fiber was formed.   |
| ID 26  | ✓  |   [click this link](https://static.igem.wiki/teams/5436/experiments/results/congo-red-assay/cr-id26.png)  | IPTG(+) pellets were stained dark red and the supernatant was nearly colorless. The absorbance results also indicate that a lot of  Curli Fiber was formed.  |
| ID 27  | ✓  |  [click this link](https://static.igem.wiki/teams/5436/experiments/results/congo-red-assay/cr-id27.png)  | IPTG(+) pellets were stained dark red and the supernatant was nearly colorless. The absorbance results also indicate that a lot of  Curli Fiber was formed.   |

 

# 5 *p*NPB Assay

In the pNPB assay, the activity of PETase was evaluated by observing the degradation activity of BIND-PETase towards pNPB. When pNPB is hydrolyzed by PETase, butyric acid and the fluorescent yellow pNP are produced. Since pNP exhibits an absorption peak at 405 nm, this was measured. The results of the absorbance measurements are shown in Fig. 9.5.1, and detailed results for each variant are provided in Table. 9.4.1.  
Among the 16 types of BIND-PETase tested in the experiment, PETase activity was confirmed in 11 of them. Particularly high activity was observed in BIND-PETase variants (ID23\~27). DuraPETase, which has been shown in previous studies to have higher activity than PETase (WT), also demonstrated similarly high activity in the form of BIND-duraPETase. Moreover, the PETase variants we designed (ID23\~27) exhibited higher activity than duraPETase in the pNPB assay, indicating that the activity of PETase was improved. Among them, BIND-PETase (ID23, 27) exhibited more than double the activity of BIND-PETase (WT).  
On the other hand, the variants that did not show activity either have inherently low PETase activity, or the fusion with CsgA may have structurally hindered the binding of the substrate to the PETase enzyme.

![]  
(https://static.igem.wiki/teams/5436/experiments/results/pnpb-assay/pnpb-assay-figure.png =500x)  
:::c  
**Fig. 9.5.1** Degradation Activity of *p*NPB for Each Variant   
:::  
The horizontal axis represents the types of variants, and the vertical axis represents pNPB degradation activity. The IPTG (+/-) samples were reacted with pNPB, and after the pNPB assay, the absorbance at 405 nm (indicative of pNP production) was measured, and the difference between IPTG (+) and IPTG (-) was calculated. The absorbance values were corrected with OD, and higher values indicate higher PETase activity towards pNPB.

:::c  
**Table. 9.5.1.** The results and analysis of Reusability assay in each mutant  
:::

| Variant | PETase Activity | Image (Left: IPTG+, Right: IPTG-)  | Discussion |
| :---- | :---- | :---- | :---- |
| WT  | ✓  |  [click this link](https://static.igem.wiki/teams/5436/experiments/results/pnpb-assay/pnpb-assay-wt.png ) | IPTG(+) samples turned yellow due to pNP production. Absorbance results also confirmed hydrolytic activity.  |
| E. coli optimized  | ✓  |  [click this link](https://static.igem.wiki/teams/5436/experiments/results/pnpb-assay/pnpb-assay-e-coli-optimized.png ) | IPTG(+) samples turned yellow due to pNP production. Absorbance results confirmed hydrolytic activity, though lower than WT.     |
| 5mut.  | ×  | [click this link](https://static.igem.wiki/teams/5436/experiments/results/pnpb-assay/pnpb-assay-5mut.png) | Both IPTG (+/-) samples remained clear, indicating no pNP production. Absorbance results confirmed the absence of hydrolytic activity.  |
| dura  | ✓  | [click this link](https://static.igem.wiki/teams/5436/experiments/results/pnpb-assay/pnpb-assay-dura.png ) | IPTG(+) samples turned yellow due to pNP production. Absorbance results confirmed hydrolytic activity, which was higher than WT.   |
| ID1  | ×  | [click this link](https://static.igem.wiki/teams/5436/experiments/results/pnpb-assay/pnpb-assay-id1.png ) | Both IPTG (+/-) samples remained clear, indicating no pNP production. Absorbance results confirmed the absence of hydrolytic activity.   |
| ID2  | ×    | [click this link](https://static.igem.wiki/teams/5436/experiments/results/pnpb-assay/pnpb-assay-id2.png) | The IPTG(+) sample appeared slightly yellow, but since IPTG(-) also showed similar coloration, it is unlikely that the hydrolysis of pNP by BIND-PETase (ID2) occurred. |
| ID3  | ✓(weak)    | [click this link](https://static.igem.wiki/teams/5436/experiments/results/pnpb-assay/pnpb-assay-id3.png ) | Both IPTG (+/-) samples remained clear with no significant difference, but a small amount of pNP was detected by absorbance. ID3 has weak activity.    |
| ID4  | ×    | [click this link](https://static.igem.wiki/teams/5436/experiments/results/pnpb-assay/pnpb-assay-id4.png ) | Both IPTG (+/-) samples remained clear, indicating no pNP production. Absorbance results confirmed the absence of hydrolytic activity.    |
| ID5  | ×    | [click this link](https://static.igem.wiki/teams/5436/experiments/results/pnpb-assay/pnpb-assay-id5.png ) | Both IPTG (+/-) samples remained clear, indicating no pNP production. Absorbance results confirmed the absence of hydrolytic activity.      |
| ID6  | ✓    | [click this link](https://static.igem.wiki/teams/5436/experiments/results/pnpb-assay/pnpb-assay-id6.png ) | Both IPTG (+/-) samples remained clear, but absorbance confirmed a small amount of pNP production. ID6 has weak activity, lower than ID3.  |
| ID22  | ✓    | [click this link](https://static.igem.wiki/teams/5436/experiments/results/pnpb-assay/pnpb-assay-id22.png) | IPTG(+) samples turned yellow due to pNP production. Absorbance results confirmed hydrolytic activity, which was lower than WT and similar to the E. coli optimized version.   |
| ID23  | ✓    | [click this link](https://static.igem.wiki/teams/5436/experiments/results/pnpb-assay/pnpb-assay-id23.png ) | IPTG(+) samples turned yellow due to pNP production. Absorbance results confirmed hydrolytic activity, which was the second highest among the tested variants.   |
| ID24  | ✓    | [click this link](https://static.igem.wiki/teams/5436/experiments/results/pnpb-assay/pnpb-assay-id24.png )  | IPTG(+) samples turned yellow due to pNP production. Absorbance results confirmed hydrolytic activity, which was the third highest among the tested variants.     |
| ID25  | ✓    | [click this link](https://static.igem.wiki/teams/5436/experiments/results/pnpb-assay/pnpb-assay-id25.png ) | IPTG(+) samples turned yellow due to pNP production. Absorbance results confirmed hydrolytic activity, which was higher than WT and duraPETase. |
| ID26  | ✓    | [click this link](https://static.igem.wiki/teams/5436/experiments/results/pnpb-assay/pnpb-assay-id26.png ) | IPTG(+) samples turned yellow due to pNP production. Absorbance results confirmed hydrolytic activity, which was higher than WT and duraPETase.   |
| ID27  | ✓    | [click this link](https://static.igem.wiki/teams/5436/experiments/results/pnpb-assay/pnpb-assay-id27.png ) | IPTG(+) samples turned yellow due to pNP production. Absorbance results confirmed hydrolytic activity, which was the highest among the tested variants.     |

Two additional validations were conducted on BIND-PETase (WT, E. coli optimized, ID 22\~24), which had demonstrated sufficient basic functionality as BIND-PETase through the Congo Red Assay in Section 9.4 and the pNPB Assay in Section 9.5. These validations were the 9.6 Storage Stability Assay, which investigated the activity after storage, and the 9.7 Reusability Assay, which examined the reusability of BIND-PETase.  
BIND-PETase (ID3) was excluded due to the low activity of PETase. Additionally, while BIND-PETase (ID25\~27) had also demonstrated sufficient basic functionality, further validation could not be performed due to time constraints.  
On the other hand, in cases where neither Curli fiber formation nor PETase activity was confirmed in BIND-PETase, it is possible that either the expression of CsgA and PETase did not occur, or even if expressed, the fusion of CsgA and PETase structurally hindered polymerization or activity of one another.

# 6 Storage Activity Assay

In this assay, the activity of BIND-PETase was evaluated on the 5th and 11th days after storage at either 4°C or room temperature. The activity fluctuate depending on the storage temperature and type of PETase, and detailed results are shown in Table. 9.6.1.  
The highest increase in activity during the storage period was observed in BIND-PETase (ID23) at 4°C and in BIND-PETase (ID24) at room temperature. Compared to BIND-PETase (WT, E. coli optimized), BIND-duraPETase and its designed variants (ID23, 24) exhibited a greater increase in activity over time.  
Conversely, PETase (WT, E. coli optimized) showed little to no increase in activity, or even a decrease, indicating lower stability. These results suggest that BIND-duraPETase improved upon BIND-PETase (WT, E. coli optimized) in terms of storage stability. Furthermore, BIND-PETase (ID23, 24) may have further improved upon BIND-duraPETase.  
The changes in activity after storage could be attributed to factors such as a decrease in stability, denaturation, or degradation of BIND-PETase. Alternatively, the increase in activity may be due to the continued expression or folding of BIND-PETase over time. The overall post-storage activity likely reflects a combination of these factors.

:::c  
**Table. 9.6.1.** Results and Discussion of the Storage Stability Assay for Each BIND-PETase Variant  
:::

| Variant | Activity | Discussion |
| :---- | :---- | :---- |
| WT  | 4°C: Increase Room temp: Decrease  [click this link](https://static.igem.wiki/teams/5436/experiments/results/storage-activity-assay/storage-activity-assay-wt.png )   | At 4°C, activity increased to 120% on day 5 and 136% on day 11. At room temperature, it decreased to 81% on day 5 and 55% on day 11, indicating instability at room temperature.  |
| E. coli optimized  | 4°C: No significant change Room temp: Decrease  [click this link](https://static.igem.wiki/teams/5436/experiments/results/storage-activity-assay/storage-activity-assay-e-coli-optimized.png ) | At 4°C, no significant changes were observed, indicating relative stability.   |
| dura  | 4°C: Increase Room temp: Increase  [click this link](https://static.igem.wiki/teams/5436/experiments/results/storage-activity-assay/storage-activity-assay-dura.png ) | At 4°C, activity increased to 183% on day 5 and 237% on day 11. At room temperature, activity increased to 224% on day 5 and 327% on day 11, suggesting stable expression and folding under both conditions. |
| ID 22  | 4°C: Increase, then decrease Room temp: Increase, then decrease  [click this link](https://static.igem.wiki/teams/5436/experiments/results/storage-activity-assay/storage-activity-assay-id22.png ) | At 4°C, activity increased to 177% on day 5 but dropped to 63% on day 11. At room temperature, it increased to 172% on day 5 but decreased to 108% by day 11.  |
| ID 23  | 4°C: Increase Room temp: Increase [click this link](https://static.igem.wiki/teams/5436/experiments/results/storage-activity-assay/storage-activity-assay-id23.png )  | At 4°C, activity increased to 294% on day 5 and 310% on day 11. At room temperature, it increased to 126% on day 5 and 394% on day 11. |
| ID 24  | 4°C: Increase Room temp: Increase   [click this link](https://static.igem.wiki/teams/5436/experiments/results/storage-activity-assay/storage-activity-assay-id24.png ) | At 4°C, activity increased to 198% on day 5 and 313% on day 11. At room temperature, it increased to 379% on day 5 and maintained at 391% by day 11.  |

# 7 Reusability Assay  

 　In this Assay, the activity of BIND-PETase was evaluated by the pNPB assay when it was used 3 times in a row (cycles 1\~3). The increase or decrease in activity depended on the type of mutant, and the details of each mutant are shown in Table. 9.7.1.    
Activity of BIND-PETase (WT, E. coli optimized, ID22) showed a slight decrease while reuse. On the other hand, activity of BIND-duraPETase and BIND-PETase (ID23 and ID24) showed an increase while reuse. This suggests that BIND-duraPETase and BIND-PETase (ID23, 24) are superior to BIND-PETase (WT, E. coli optimized) in terms of reusability of BIND-PETase.   
The following factors may contribute to the change in activity while reuse. The decrease in activity may be due to the destabilization of the structure because of usage in the reaction.   
Also, the structural change because of the environment after the reaction or collection by centrifugation may be another factor. On the other hand, the increase in activity may be due to the reaction of BIND-PETase with pNPB, or the promotion of folding of BIND-PETase.   
In addition, as a problem of experimental manipulation, it is possible that pNP, a degradation product of pNPB, was mixed into the cycle. However, the effect on the cycle should be small because it should be diluted enough when reused. Yet, there were some results that suggested that pNPs were not removed enough from the samples of some mutants. For more accurate measurement, it is important to increase the times of washing  BIND-PETase pellets and remove pNPs as much as possible. 

:::c  
**Table. 9.7.1**. The results and analysis of Reusability assay in each mutant  
:::

| Sample name  | Activity of BIND-PETase while reuse | Analysis  |
| :---- | :---- | :---- |
| WT  | a little decrease   [click this link](https://static.igem.wiki/teams/5436/experiments/results/reusability-assay/reusability-wt.png)  | Activity was 83% in Cycle 2 and 88% in Cycle 3. Activity decreased slightly while reusing, but not significantly decreased. This BIND-PETase is considered to be relatively stable and reusable.  |
| E. coli optimized  | a little decrease   [click this link](https://static.igem.wiki/teams/5436/experiments/results/reusability-assay/reusability-e-coli-optimized.png)   | Activity was 70% in Cycle 2 and 86% in Cycle 3. Activity decreased slightly while reusing, but not significantly decreased. This BIND-PETase is considered to be relatively stable and reusable.  |
| dura  | increase   [click this link](https://static.igem.wiki/teams/5436/experiments/results/reusability-assay/reusability-dura.png)   | The activity was 91% in cycle2 and 274% in cycle3. The variation between samples in cycle1 and cycle2 was small and this suggests that activity of BIND-PETase didn’t decrease by reusing. On the other hand, the activity increased significantly between cycle2 and cycle3, and the variation among the samples was wide. So, it is possible that the activity of BIND-PETase in cycle3 was estimated to be higher due to the contamination of pNPs generated in the previous cycles, but at least the activity was not lost.   |
| ID22  | decrease   [click this link](https://static.igem.wiki/teams/5436/experiments/results/reusability-assay/reusability-id22.png)   | Activity decreased to 59% in cycle 2 and 52% in cycle 3. It is thought that the activity decreases with reuse. The more it is used, the lower the activity.  |
| ID23  | increase   [click this link](https://static.igem.wiki/teams/5436/experiments/results/reusability-assay/reusability-id23.png)   | The activity was 193% in cycle2 and 144% in cycle 3. Although there is a possibility of pNP contamination because there is large variation between sample in cycle2 and sample in cycle3.  |
| ID24  | increase   [click this link](https://static.igem.wiki/teams/5436/experiments/results/reusability-assay/reusability-id24.png)     | The activity was 168% in cycle2 and 128% in cycle3. As with ID23, there is a possibility of pNP contamination because there is large variation among samples. However, an increase in activity was observed. |

   
 

# 8 PET Pellet Degradation Assay

# 9 PET Powder Degradation Assay

# 10 Discussion

# 

 [^1]:Yunpu J. et al. (2022), Hydrophobic cell surface display system of PETase as a sustainable biocatalyst for PET degradation, Microbiotechnology,Vol.13, 