# VarChAMP ALK Variant Profiling

Exploratory functional characterization of **ALK missense variants** using **VarChAMP Cell Painting profiles**, **JUMP CRISPR perturbation matching**, **Gene Ontology over-representation analysis (ORA)**, **ClinVar**, and **AlphaMissense**.

## Overview

Most human missense variants remain functionally uncharacterized despite rapid advances in DNA sequencing. The **Variant Characterization Across the Mendelian Proteome (VarChAMP)** project was established to address this challenge by systematically measuring the functional consequences of genetic variation using high-throughput cellular phenotyping assays.

This repository contains an exploratory analysis of publicly available VarChAMP Cell Painting profiles. The project began with an investigation of OASIS drug-induced liver injury (DILI) compounds and their relationship to JUMP Cell Painting profiles before shifting toward variant-level functional characterization. Through systematic exploration of the dataset, **ALK** emerged as a particularly informative target exhibiting substantial variant-specific morphological diversity.

The analysis focuses on four ALK missense variants:

* T1151M
* A1234T
* F1174L
* R1275Q

and investigates whether morphology-based profiling can provide functional information complementary to sequence-based pathogenicity prediction.

## Workflow

1. OASIS DILI dataset exploration
2. OASIS–JUMP compound matching
3. Identification of genes exhibiting informative morphological variation
4. Prioritisation of ALK for variant-level investigation
5. Morphological profiling of ALK missense variants
6. Distance-from-wild-type analysis
7. Variant–variant similarity analysis
8. CRISPR perturbation matching using JUMP profiles
9. Gene Ontology (GO) over-representation analysis (ORA)
10. ClinVar annotation lookup
11. AlphaMissense pathogenicity assessment
12. Integrated interpretation of morphology-, CRISPR-, and sequence-based evidence

## Key Findings

* ALK variants produced distinct morphological phenotypes relative to wild-type ALK.

* Morphological impact ranked variants as:

  **T1151M > A1234T > F1174L > R1275Q**

* F1174L and R1275Q displayed strong morphological similarity (r = 0.74), consistent with their known activating roles in neuroblastoma.

* CRISPR perturbation matching identified enrichment of transcriptional regulation, ubiquitination, protein modification, and proteostasis pathways.

* GO ORA revealed coherent biological processes associated with morphology-matched perturbations.

* A1234T lacked ClinVar annotation but exhibited one of the strongest morphological phenotypes observed in the dataset.

* AlphaMissense classified all four variants as pathogenic, including A1234T.

* Morphology-derived rankings differed substantially from AlphaMissense rankings, suggesting that image-based profiling and sequence-based prediction capture complementary aspects of variant biology.

## Repository Contents

* `VarChAMP_ALK_Analysis.ipynb` — complete analysis notebook
* `VarChamp_final_ParulK.pdf` — full report containing methods, results, figures, interpretation, and discussion
* `figures/` — exported visualizations
* `results/` — processed analysis outputs

## Data Sources

* VarChAMP Cell Painting Profiles
* JUMP Cell Painting Consortium
* ClinVar
* AlphaMissense

## Resources

* VarChAMP: https://varchamp.broadinstitute.org
* JUMP Cell Painting: https://jump-cellpainting.broadinstitute.org
* JUMP GitHub: https://github.com/jump-cellpainting
* AlphaMissense: https://github.com/google-deepmind/alphamissense
* ClinVar: https://www.ncbi.nlm.nih.gov/clinvar/

## References

1. Bray MA, Singh S, Han H, Davis CT, Borgeson B, Hartland C, et al. *Cell Painting, a high-content image-based assay for morphological profiling using multiplexed fluorescent dyes*. Nature Protocols. 2016;11(9):1757–1774. doi:10.1038/nprot.2016.105.

2. Caicedo JC, Singh S, Carpenter AE. *Applications in image-based profiling of perturbations*. Current Opinion in Biotechnology. 2016;39:134–142. doi:10.1016/j.copbio.2016.04.003.

3. Lacoste J, Haghighi M, Haider S, Reno C, Lin ZY, Segal D, Qian WW, Xiong X, Teelucksingh T, Miglietta E, Shafqat-Abbasi H, Ryder PV, Senft R, Cimini BA, Murray RR, Nyirakanani C, Hao T, McClain GG, Roth FP, Calderwood MA, Hill DE, Vidal M, Yi SS, Sahni N, Peng J, Gingras AC, Singh S, Carpenter AE, Taipale M. *Pervasive mislocalization of pathogenic coding variants underlying human disorders*. Cell. 2024;187(23):6725–6741.e13. doi:10.1016/j.cell.2024.09.003.
