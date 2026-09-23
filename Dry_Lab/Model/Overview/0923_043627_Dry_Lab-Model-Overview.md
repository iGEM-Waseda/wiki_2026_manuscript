# Overview

The SUNRISE System is designed to resensitize drug-resistant bacteria to existing antibiotics in a target-specific and safe manner by directly degrading antibiotic resistance proteins. SUNRISE consists of a TPD Module, which degrades resistance proteins, and a CPI Module, which delivers the TPD Module into target bacteria. For a full account of the system, see our Description and Design pages.

In our Model, we first established and documented a set of design workflows for TPD and CPI, and used in silico analysis to decide which designs to validate in the Wet Lab. The experimental data obtained from the Wet Lab were then fed back into the Model, allowing us to evaluate the properties, behavior, and safety of each module quantitatively and from multiple perspectives through mathematical modeling and in silico analysis.

We then integrated the TPD and CPI models built through this iteration between Wet Lab and Model, and examined the conditions under which the SUNRISE System — combining delivery of the TPD Module with degradation of its target — can actually restore antibiotic susceptibility. We also modeled the pharmacokinetics of local administration as a prospective route of implementation, and analyzed safety aspects including off-target effects and the toxicity of the constituent molecules. Together, these results demonstrate the feasibility of the SUNRISE System and the conditions required for its future implementation from a range of angles.

In addition, we documented the design workflows and analytical methods of each Model in a reusable form. Future iGEM teams can therefore apply not only the SUNRISE System as a whole, but also the TPD or CPI Module on its own, or even individual Models, to projects of their own.

## TPD

Here we examined how the TPD Module is designed, how efficiently it can degrade its target protein, and whether that degradation is sufficient to restore antibiotic susceptibility.

In ①, we used Wet Lab data relating the expression level of the antibiotic resistance protein to the MIC in order to model the relationship between the amount of resistance protein and the amount of antibiotic required, thereby clarifying how much degradation the TPD Module must achieve.

In ②, we extended the technology for directly degrading target proteins inside bacteria and proposed and documented a TPD design workflow applicable to a wide range of target proteins. By making the TPD Module extensible to diverse targets and presenting it as a design platform that can be applied to many different projects, we aimed to contribute to the iGEM community.

Here we evaluated, by molecular dynamics (MD) simulation, whether the Adaptor we designed binds stably to its target protein and can therefore function as part of a TPD Module.

In ③, we examined how extensively the TPD Module can degrade antibiotic resistance proteins. This Model uses constants obtained directly from our Wet Lab results, making it a more realistic representation of the system.

In ④, we analyzed regions conserved among resistance factors as well as potential off-targets, and assessed how broad a range of resistance factors the TPD Module can target while retaining its target specificity.

Taken together, these analyses allowed us to design the TPD Module through modeling, quantify its behavior using Wet Lab results, and ultimately evaluate the conditions under which the TPD Module can restore antibiotic susceptibility.

## CPI

Here we examined the design and performance of the CPI Module, which binds specifically to target bacteria and delivers a TPD payload into the cell.

In ①, we used structure prediction and interaction analysis to design the CPI tail that binds to the target bacterium, and selected from the Model the constructs to be built and validated in the Wet Lab.

In ②, we extended this approach into a design workflow for CPIs directed against a variety of *E. coli* strains, and compiled a library summarizing which CPI can be used against which strain. Together, ① and ② establish a foundation for designing CPIs against a wide range of target bacteria; by presenting a design workflow that can be applied to many different projects, we aimed to contribute to the iGEM community.

In ③, CPIs have so far been shown mainly to inject into eukaryotic cells, so we examined geometrically whether injection into *E. coli* is in fact possible and with what efficiency.

In ④, we examined how much TPD cargo can be loaded into a CPI. Combining ③ and ④ allowed us to assess whether a CPI carrying a TPD payload can still inject into bacteria, and thus whether the central idea of loading the TPD Module into a CPI and delivering it to drug-resistant bacteria is feasible.

In ⑤, we examined whether the CPI binds in a target-specific manner and evaluated the possibility of off-target binding to non-target bacteria, thereby assessing the target specificity and safety of the CPI Module.

Through these analyses, we designed the CPI Module in the Model and quantified binding, loading, and injection using Wet Lab results, clarifying the conditions under which TPD delivery by the CPI Module can be achieved.

## SUNRISE

Here we integrated the Models built for the TPD and CPI Modules and examined whether the SUNRISE System as a whole can actually work.

In ①, we connected the model of TPD delivery by the CPI Module to the model of degradation by the TPD Module, and evaluated the following as a single continuous model:

1. delivery by the CPI Module  
2. intracellular TPD level  
3. degradation of the antibiotic resistance protein  
4. restoration of antibiotic susceptibility

This model is built on the values and relationships obtained from the Wet Lab experiments and in silico analyses performed for the TPD and CPI Modules. It therefore allowed us to examine not only whether each Module works on its own, but also whether the amount of TPD that the CPI Module can realistically deliver is enough to degrade the antibiotic resistance protein down to the level required for antibiotic susceptibility to be restored.

In ②, we assumed local administration as a prospective route of implementation for SUNRISE and built a pharmacokinetic model accounting for distribution, elimination, and clearance by the immune system.

In ③, we examined the safety of the SUNRISE System under the assumption of administration to the human body, from multiple perspectives including peptide toxicity and off-target interactions. Through ② and ③, we assessed the feasibility and safety of the SUNRISE System with a view to its eventual real-world implementation.

In this way, we fed our designs from the Model back into the Wet Lab, and the measured data from the Wet Lab back into the Model. By integrating the models built through this iteration into SUNRISE as a whole, we evaluated the feasibility, implementation conditions, and safety of the system.