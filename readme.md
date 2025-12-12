# Awesome Virtual Cell & Whole-Cell Modeling Papers

A curated collection of important papers, methods, and GitHub repositories for virtual cell and whole-cell modeling.

## Table of Contents

- [Physics-Based Modeling](#physics-based-modeling)
- [AI/Data-Driven Modeling](#aidata-driven-modeling)
- [Software Ecosystem](#software-ecosystem)
- [Others](#other-papers)

![digital-twin](./figures/budding_yeaset_digital_twin_shrink.png)
---

## Physics-Based Modeling

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

### AI Virtual Cell (CZI Biohub / Arc Institute)

**intiative paper:** Bunne, C. et al. How to build the virtual cell with artificial intelligence: Priorities and opportunities. Cell 187, 7045–7063 (2024).

**challege paper:** Roohani, Y. H. et al. Virtual Cell Challenge: Toward a Turing test for the virtual cell. Cell 188, 3370–3374 (2025).

#### STATE: Model by Arc Institute  (June 2025)

**Paper:** Adduri, A. K. et al. Predicting cellular responses to perturbation across diverse contexts with State. 2025.06.26.661135 Preprint at https://doi.org/10.1101/2025.06.26.661135 (2025).

**news reprot:** [Arc Institute’s first virtual cell model: State](https://arcinstitute.org/news/virtual-cell-model-state )


**Method:** Centralized open-source hub with NVIDIA GPU infrastructure hosting models (CodonFM, MONAI), datasets, and benchmarks.

**GitHub:** [STATE](https://github.com/ArcInstitute/state)

---

## Software Ecosystem
### Lattice Microbes - University of Illinois at Urbana-Champaign

**PI:** Zan Luthey-Schulten

**Method:** Stochastic reaction-diffusion simulator for modeling biochemical networks in 3D cellular environments. Uses lattice-based methods to simulate molecular interactions and spatial dynamics within cells.

**GitHub:** [Lattice Microbes](https://github.com/Luthey-Schulten-Lab/Lattice_Microbes)

**Document:**: 

[UserGuide](https://luthey-schulten-chemistry.github.io/LM2.5_doc/)

[Detailed Guide](https://forxhunter.github.io/Lattice_Microbes_DevelopDoc/)

### Virtual Cell (VCell) - UConn Health

**PI:** Leslie Loew

**Method:** Reaction-diffusion and spatial modeling platform. Integrates rule-based modeling (BioNetGen), moving boundary problems, and mesoscale simulations using particle-based methods (SpringSaLaD).

**Website:** https://vcell.org/

**GitHub:** [Virtual Cell](https://github.com/virtualcell/vcell)

---

### Vivarium - University of Connecticut

**PI:** Eran Agmon

**Paper:** Agmon E, Spangler RK, Skalnik CJ, Poole W, Peirce SM, Morrison JH, Covert MW. "Vivarium: an interface and engine for integrative multiscale modeling in computational biology." Bioinformatics. 2022.

**Method:** Python-based compositional systems biology framework using "Process Bigraphs" for integrating models across scales and languages.

**GitHub:** [Vivarium](https://github.com/vivarium-collective/vivarium-core)

---



---

## Other papers

---

## Contributing

Contributions welcome! Please add papers, methods, and repositories following the existing format.

## License

See [LICENSE](LICENSE) file for details.

