# Awesome Virtual Cell & Whole-Cell Modeling Papers

A curated collection of important papers, methods, and GitHub repositories for virtual cell and whole-cell modeling.

## Table of Contents

- [Physics-Based Modeling](#physics-based-modeling)
- [AI/Data-Driven Modeling](#aidata-driven-modeling)
- [Software Ecosystem](#software-ecosystem)
- [Others](#other-papers)

<img src="./figures/budding_yeaset_digital_twin_shrink.png" alt="digital-twin" width="600">
---

## Physics-Based Modeling

<img src="./figures/wcm_phsics.png" alt="physicswcm" width="300">

### Zan Luthey-Schulten Lab (University of Illinois at Urbana-Champaign)
This is a review like paper:

**paper:** Cole JA, Luthey-Schulten Z. Whole Cell Modeling: From Single Cells to Colonies. Isr J Chem. 2014 Aug;54(8-9):1219-1229. doi: 10.1002/ijch.201300147. Epub 2014 Jul 31. PMID: 26989262; PMCID: PMC4792290.

#### 1.4D-minimal cell in 105 min
**Paper:** Thornburg et al. (2025) "Bringing the Genetically Minimal Cell to Life on a Computer in 4D." bioRxiv.

**Method:** Hybrid 4D spatiotemporal modeling combining Lattice Microbes (stochastic reaction-diffusion), LAMMPS (Brownian dynamics for chromosome), and ODEs (metabolism). Simulates complete cell cycle of JCVI-syn3A with spatial heterogeneity.

**GitHub:** [4DWCM](https://github.com/Luthey-Schulten-Lab/Minimal_Cell_4DWCM)

#### 2.Static one

**Paper:** Thornburg et al. (2022) "Fundamental behaviors emerge from simulations of a living minimal cell." Cell.

**Github:**: [MinCell](https://github.com/Luthey-Schulten-Lab/Minimal_Cell)

---

### Markus Covert Lab (Stanford University)

**Paper:** Ahn-Horst, T.A., Mille, L.S., Sun, G. et al. An expanded whole-cell model of E. coli links cellular physiology with mechanisms of growth rate control. npj Syst Biol Appl 8, 30 (2022). https://doi.org/10.1038/s41540-022-00242-9

**paper:** Sun G, Ahn-Horst TA, Covert MW.2021.The E. coli Whole-Cell Modeling Project. 9:eESP-0001-2020.https://doi.org/10.1128/ecosalplus.ESP-0001-2020

**paper:** Macklin, D. N. et al. Simultaneous cross-evaluation of heterogeneous E. coli datasets via mechanistic simulation. Science 369, eaav3751 (2020).


**GitHub:** [WCM_ecoli](https://github.com/CovertLab/WholeCellEcoliRelease)


---

### FBA amd FBA related models

#### 1.Yeast GEM 9:
**paper**: Zhang C, Sánchez BJ, Li F, Eiden CWQ, Scott WT, Liebal UW, Blank LM, Mengers HG, Anton M, Rangel AT, Mendoza SN, Zhang L, Nielsen J, Lu H, Kerkhoven EJ. Yeast9: a consensus genome-scale metabolic model for S. cerevisiae curated by the community. Mol Syst Biol. 2024 Oct;20(10):1134-1150. doi: 10.1038/s44320-024-00060-7. Epub 2024 Aug 12. PMID: 39134886; PMCID: PMC11450192.

**Github**: [Yeast-GEM](https://github.com/SysBioChalmers/yeast-GEM)

### 2.ETFL

This is a version of FBA model that have thermo-constraint and various conservations. This have both yeast and ecoli model here. 

**paper:** Salvy, P., Hatzimanikatis, V. The ETFL formulation allows multi-omics integration in thermodynamics-compliant metabolism and expression models. Nat Commun 11, 30 (2020) doi:10.1038/s41467-019-13818-7

**paper:** Oftadeh, O. & Hatzimanikatis, V. Genome-scale models of metabolism and expression predict the metabolic burden of recombinant protein expression. Metabolic Engineering 84, 109–116 (2024). doi: 10.1016/j.ymben.2024.06.005

**paper:** Oftadeh, O., Salvy, P., Masid, M. et al. A genome-scale metabolic model of Saccharomyces cerevisiae that integrates expression constraints and reaction thermodynamics. Nat Commun 12, 4790 (2021). https://doi.org/10.1038/s41467-021-25158-6

**Github:** [ETFL](https://github.com/EPFL-LCSB/etfl.git)

**Github:** [ecoli-ETFL](https://github.com/EPFL-LCSB/ecetfl/)

**Github:** [yeast-ETFL](https://github.com/EPFL-LCSB/yetfl)

---

## AI/Data-Driven Modeling

<img src="./figures/wcm_AI.png" alt="AI_wcm" width="300">

### AI Virtual Cell (CZI Biohub / Arc Institute)

**intiative paper:** Bunne, C. et al. How to build the virtual cell with artificial intelligence: Priorities and opportunities. Cell 187, 7045–7063 (2024).

**challege paper:** Roohani, Y. H. et al. Virtual Cell Challenge: Toward a Turing test for the virtual cell. Cell 188, 3370–3374 (2025).

#### STATE: Model by Arc Institute  (June 2025)

**Paper:** Adduri, A. K. et al. Predicting cellular responses to perturbation across diverse contexts with State. 2025.06.26.661135 Preprint at https://doi.org/10.1101/2025.06.26.661135 (2025).

**news report:** [Arc Institute’s first virtual cell model: State](https://arcinstitute.org/news/virtual-cell-model-state )


**Method:** Centralized open-source hub with NVIDIA GPU infrastructure hosting models (CodonFM, MONAI), datasets, and benchmarks.

**GitHub:** [STATE](https://github.com/ArcInstitute/state)


---

## Software Ecosystem

### **1. Integrated & Multiscale Modeling Platforms**
These platforms are designed to bridge different scales (molecular to cellular) or integrate various modeling approaches (deterministic, stochastic, spatial) into a unified environment.

| Platform | Key Developer / PI | Methodology & Key Features | Links |
| :--- | :--- | :--- | :--- |
| **Virtual Cell (VCell)** | **Leslie Loew** (UConn Health) | **Unified Environment:** Integrates reaction-diffusion, spatial modeling, rule-based modeling (BioNetGen), and particle-based simulation (SpringSaLaD) in one interface. | [Website](https://vcell.org/) |
| **Vivarium** | **Eran Agmon** (UConn) | **Integrative Framework:** Python-based engine using "Process Bigraphs" to composite diverse models across scales and languages into a single simulation. | [GitHub](https://github.com/vivarium-collective/vivarium-core) |
| **Morpheus** | **Jörn Starruß** (TU Dresden) | **Hybrid Cell-Based:** User-friendly GUI for multiscale modeling. Combines Cellular Potts Models (CPM) for mechanics with ODE/PDE systems for biochemistry. | [Website](https://morpheus.gitlab.io) |

### **2. Multicellular & Tissue Simulation (Agent-Based)**
These tools focus on the behavior of cell populations, tissue mechanics, and the microenvironment, often using Agent-Based Modeling (ABM) or the Cellular Potts Model (CPM/GGH).

| Platform | Key Developer / PI | Methodology & Key Features | Links |
| :--- | :--- | :--- | :--- |
| **PhysiCell** | **Paul Macklin** (Indiana Univ) | **Tissue-Scale ABM:** Optimized for 3D multicellular systems, focusing on cell mechanics, diffusion fields, and tumor microenvironments. | [Website](http://physicell.org) |
| **CompuCell3D** | **Maciej Swat** | **Cellular Potts Model:** Couples cell mechanics and shape changes with reaction-diffusion processes. Supports Python scripting for complex tissue logic. | [Website](https://compucell3d.org) |
| **Chaste** | **Gary Mirams** (Nottingham) | **High-Performance C++:** A modular library specialized for cardiac electrophysiology, soft tissue mechanics, and cancer modeling. | [Website](https://chaste.github.io) |

### **3. Intracellular Network & Pathway Simulators**
These tools specialize in modeling the biochemical logic, signaling pathways, and reaction kinetics within a cell, using ODEs or rule-based definitions.

| Platform | Key Developer / PI | Methodology & Key Features | Links |
| :--- | :--- | :--- | :--- |
| **COPASI** | **Stefan Hoops** (Virginia Tech) | **Biochemical Kinetics:** Simulates networks using ODEs/SDEs. Robust tools for parameter estimation, sensitivity analysis, and time-course analysis. | [Website](http://copasi.org) |
| **BioNetGen** | **James Faeder** (Pitt) | **Rule-Based Modeling:** Uses BNGL to model signal transduction, handling the combinatorial complexity of protein-protein interactions. | [Website](https://bionetgen.org) |
| **PySB** | **Carlos Lopez** (Altos Labs) | **Python Framework:** A programming environment for biological models. Interoperable with BioNetGen and Kappa for composable modeling. | [Website](https://pysb.org) |
| **CellNOpt** | **C. Terfve** | **Logic Modeling:** Trains protein signaling networks to data using logic, fuzzy logic, or differential logic formalisms. | [Website](https://saezlab.github.io/CellNOptR) |

### **4. Stochastic & Particle-Based Simulators**
These tools model biology at the highest resolution, tracking individual molecules or particles to capture spatial stochasticity and diffusion in 3D.

| Platform | Key Developer / PI | Methodology & Key Features | Links |
| :--- | :--- | :--- | :--- |
| **Lattice Microbes** | **Zan Luthey-Schulten** (UIUC) | **Stochastic Reaction-Diffusion:** Simulates biochemical networks in realistic 3D cellular geometries using lattice-based methods on GPUs. | [GitHub](https://github.com/Luthey-Schulten-Lab/Lattice_Microbes) |
| **Smoldyn** | **Steve Andrews** (Fred Hutch) | **Particle-Based:** Simulates molecular diffusion, surface interactions, and excluded volume with high spatial precision. | [Website](http://www.smoldyn.org) |
| **MCell** | **T. Bartol / T. Sejnowski** (Salk) | **Monte Carlo:** 3D reaction-diffusion simulator. Highly integrated with Blender for complex geometry construction. | [Website](https://mcell.org) |
| **ReaDDy** | **Frank Noé** (FU Berlin) | **Interacting Particles:** Software for particle-based reaction dynamics that accounts for crowding and molecular potentials. | [Website](https://readdy.github.io) |

### **5. AI: Generative Models & Omics Analysis**
These AI models use Deep Learning (VAEs, Transformers, GNNs) to integrate multi-omics data, denoise datasets, and infer cell states.

| Model | Key Reference | Methodology & Key Features | Links |
| :--- | :--- | :--- | :--- |
| **scVI / totalVI** | **Gayoso et al.** | **Deep Generative (VAE):** Handles batch integration and joint probabilistic modeling of RNA and protein single-cell data. | [GitHub](https://github.com/scverse/scvi-tools) |
| **GeneFormer** | **Theodoris et al.** | **Foundation Model:** Large-scale transformer pretrained on gene expression. Enables transfer learning for cell-type and gene-function inference. | [GitHub](https://github.com/jkobject/geneformer) |
| **GLUE** | **Cao et al.** | **Multi-Omics Graph:** Uses regulatory network priors to project heterogeneous single-cell omics into a shared embedding space. | [GitHub](https://github.com/gao-lab/GLUE) |
| **GraphST** | **Long et al.** | **Spatial GNN:** Graph neural network that couples expression data with spatial proximity for cell-type identification. | [GitHub](https://github.com/JinmiaoChenLab/GraphST) |

### **6. AI: Perturbation & Drug Response Prediction**
These models specifically target the "Virtual Cell" goal of predicting how a cell reacts to drugs or genetic edits.

| Model | Key Reference | Methodology & Key Features | Links |
| :--- | :--- | :--- | :--- |
| **GEARS** | **Roohani et al.** | **Knowledge Graph AI:** Predicts transcriptional outcomes of novel multi-gene perturbations using knowledge graphs. | [GitHub](https://github.com/snap-stanford/GEARS) |
| **DrugCell** | **Kuenzi / Ideker** |  **Interpretable AI:** Predicts drug response by unifying transcriptomes with drug molecular graphs and biological target networks. | [GitHub](https://github.com/idekerlab/DrugCell) |


> References: Ma, C., Zhang, H., Rao, Y. et al. AI-driven virtual cell models in preclinical research: technical pathways, validation mechanisms, and clinical translation potential. npj Digit. Med. (2025). https://doi.org/10.1038/s41746-025-02198-6



---

## Other papers

---

## Contributing

Contributions welcome! Please add papers, methods, and repositories following the existing format.

## License

MIT licnese. See [LICENSE](LICENSE) file for details.

