## **New Parts**

We registered several parts for the BIND-PETase Module. They will serve as a basis for future iGEMers who make new whole-cell biocatalysts and innovative efforts.   
   
[**BBa_K5436124**](https://parts.igem.org/Part:BBa_K5436124) **“Optimized RBS+BIND-bearPETase”**    
   
This part contributes to the construction of whole-cell biocatalysts “BIND-bearPETase” using the BIND-System, which enhances PET degradation efficiency while stabilizing and enabling the reuse of enzymes. It can also lower enzyme purification costs and maintain protein activity.  For more detailed experimental results, refer to [BBa_K5436124](https://parts.igem.org/Part:BBa_K5436124),  [Engineering Success](https://2024.igem.wiki/waseda-tokyo/engineering/) and [Results.](https://2024.igem.wiki/waseda-tokyo/results/)   


:::c   
**Fig. 5.1.** BIND-PETase Module graphical abstract    
:::   
While BIND-System is initially designed for PET degradation, it can be applied to any enzymes. By combining it with the three parts below, any enzyme can be incorporated into the BIND-System, expanding its applicability.  
   
[**BBa_K5436005**](https://parts.igem.org/Part:BBa_K5436005) **“Optimized RBS for BIND-System"**  
[**BBa_K5436006**](https://parts.igem.org/Part:BBa_K5436006) **“csgA-taa"**  
[**BBa_K5436100**](https://parts.igem.org/Part:BBa_K5436100) **“BIND-System Module”**  

:::c   
**Fig. 5.2.** Advantages of [BBa_K5436100](https://parts.igem.org/Part:BBa_K5436100) “BIND-System Module”  
:::

## **Development of In Silico Evolution Pipeline** 

We developed the In Silico Evolution Pipeline to enhance protein function and achieved partial success with BIND-PETase(ID3) ([BBa_K5436103](https://parts.igem.org/Part:BBa_K5436103)). This experience is significant for considering protein evolution using machine learning models and simulation tools, and it is documented in the [Model-Simulation](https://2024.igem.wiki/waseda-tokyo/model/?section=simulation#in-silico-evolution-pipeline) and [GitLab](https://gitlab.igem.org/2024/software-tools/waseda-tokyo). This will greatly benefit future iGEMers aiming to improve proteins using machine learning.



:::c   
**Fig5.3** In Silico Evolution Pipeline   
:::   
Typically, mutation introduction and screening are performed in a Wet Lab; however, the PCR kits for random mutagenesis are expensive[^1], making it difficult for iGEM teams to implement them. We hope to continue using this pipeline to evolve various proteins, with the code published on [GitLab](https://gitlab.igem.org/2024/software-tools/waseda-tokyo) being utilized by many teams.

## **Documentation of Groundbreaking Mathematical Models**

Among the various models we developed for the social implementation of PET TWINS, there are some that have never been built before and can be utilized by future iGEMers for various purposes. 

Those formulas are well documented in [Model](https://2024.igem.wiki/waseda-tokyo/model/) for future iGEMers.

####  **PET Degradation Model**



:::c   
**Fig5.4** The scheme for mathematical modeling of PET polymer degradation by BIND-PETase  
::: 

This model simulates how BIND-PETase breaks down PET polymer chains. It was specifically designed for the BIND-PETase project, **built from scratch**, and produced the intended results.

This model has the potential to be applied by future iGEMers to model the breakdown of polymers other than PET or biological mechanisms that involve annealing to polymer chains for degradation.

#### **3D Diffuision Model**

We need to consider mass transfer in liquid as we aim for the industrialization of PETase, and we have **newly constructed and demonstrated a diffusion model of liquid in three-dimensional space**.

Based on previous research under the state of two-dimensions and their referred research, we conducted the CIP method for three-dimensions.


:::c   
**Fig5.5** Animation of the altering concentration around the origin  
::: 

This model **allows for the three-dimensional diffusion of any object in a liquid to be modeled for future iGEMers**. As long as the size of the particle is known, it is useful for validating the diffusion of very small electrons as well as relatively larger cells, such as yeast.

## **Leakiness of pSoxS observed and modeled** 

Our results showed that maintaining the redox state of the SoxR protein and the chemical called pyocyanin is challenging, which are essential factors of the pSoxS promoter, in the ideal redox state. The challenges are outlined as follows.

* It is not possible to reduce all of the existing pyocyanin.   
* SoxR expression in E.coli may not be exclusively in its reduced form   
* The equipment utilized lacked the ability to completely reduce pyocyanin in LB medium  
* More anaerobic conditions required to control the pSoxS promoter. 

For more details, refer to [Engineering Success](https://2024.igem.wiki/waseda-tokyo/engineering/#ecb-module) or [Results](https://2024.igem.wiki/waseda-tokyo/results/#2-ecb-overview).

 
:::c   
Fig. 5.6.  Electric fermentation of *E. coli* in the equipment.   
:::   
To understand the leakiness in more detail, we made simulations of the reaction using mathematical modeling, with the conditions used in the lab. (Refer to [Model-Part.1](https://2024.igem.wiki/waseda-tokyo/model/?section=model-1#part1.-gene-circuits-model))   
As shown in Fig. 5.7, the quantity of both the oxidized and reduced SoxR continued increasing (Reaction time = 100 seconds), thus raising difficulties in implementing this module.    

:::c   
**Fig. 5.7.** Simulation of the redox state of Pyocyanin and SoxR protein   
:::   
We believe that exploring the use of the pSoxS promoter contributes not only to bioremediation, but also to foster advancements by improving gene regulation technologies.    
 

## **Documentation of Outreaching activity with Microplastics**

 
:::c   
**Fig. 5.8.** Outreaching activity with Microplastics    
:::   
The workshop, where we observed microplastics actually collected from a nearby sea, was the first activity we conducted as part of our Human Practice in iGEM Community. The methods used in this activity have been summarized in the following PDF.   
   
<div style="display: flex; justify-content: center; margin: 24px auto;">     
 <iframe src="https://static.igem.wiki/teams/5436/contirbution/unilab-experiment-guide-ver3.pdf" width="80%" height="500px"></iframe>     
</div>    

**Supplementary Material.** Experiment guidebook for the general public.  
Future iGEMers who aim to address plastic issues, including microplastics, can enhance their dialogue with the general public by referencing our methods.   
What we learned through this outreach activity is documented in [IHP-Section. 1](https://2024.igem.wiki/waseda-tokyo/human-practices/#what-we-did-in-section-1.). By collecting samples from Tokyo Bay and observing them under microscopes, this experience reaffirmed the urgency of addressing the issue. 

## **First attempt to collaborate with a VTuber for outreach in the iGEM community.**

We planned a collaborative livestream with [Mr. Rai Takatoh, a life science VTuber](https://www.youtube.com/@takatoh_life). This initiative set a new precedent as the first collaboration between an iGEM team and a VTuber   

:::c   
**Fig. 5.9.** Live streaming event with Vtuber, [Mr. Rai Takatoh](https://www.youtube.com/@takatoh_life)   
:::   
Live streaming event exemplifies effective science communication and human practice, providing a model for future iGEMers to engage with VTubers in promoting synthetic biology.    
VTubers, particularly [Mr. Rai Takatoh](https://www.youtube.com/@takatoh_life), are influential in YouTube culture, utilizing virtual characters for interactive broadcasts that engage audiences. We, Waseda-Tokyo team collaborated with Rai Takatoh in a livestream focused on the plastic waste problem, facilitating valuable discussions with viewers in the comment section. For detailed insights from the event, see the [IHP-Section.4](https://2024.igem.wiki/waseda-tokyo/human-practices/#section-4.-re-examination-of-where-pet-twins-can-be-implemented-in-society) section. 

## **Documentation of Protocols** 

We documented protocols of our experiment for future iGEMers (see [Experiments](https://2024.igem.wiki/waseda-tokyo/experiments/) for details!). 

[^1]: Takara Bio Inc. Diversify PCR Random Mutagenesis Kit for sequence mutations. https://www.takarabio.com/products/cloning/mutagenesis-kits/random-mutagenesis-kit?catalog=630703.   
   
