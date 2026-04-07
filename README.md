# Cross-Condition Network Analysis

[![Python 3.8+](https://pfst.cf2.poecdn.net/base/image/615ff68347b1a24604be37f6c9bba422591b71f2fb4927934fa1df6431ae9bb3?pmaid=599817308)](https://www.python.org/)
[![License: MIT](https://pfst.cf2.poecdn.net/base/image/4ba58a42a1fd9162b3759f934f77fea471b851e359255d522e10f301557e22c3?pmaid=599817309)](LICENSE)

## Overview

This repository contains the data and analysis code for the paper:

> **Blue-Enriched White Light and Within-Subsystem Integration in Preschool Children: An Exploratory Network Analysis Dissociating Univariate and Topological Sensitivity**  
> Yankang Jiang<sup> a</sup>, Dingheng Mai<sup> b</sup>, Xiaotong Chen<sup> c</sup>, Junxian Liang<sup> d</sup>, Yupeng Shen<sup> a, *</sup> 
>
> 
> <sub>*<sup>a</sup> Sports Engineering Center, School of Physical Education and Sports Science, South China Normal University, Guangzhou, 510006, China*</sub>  
> <sub>*<sup>b</sup> Department of Biomedical Engineering, Case Western Reserve University, Cleveland, OH, United States*</sub>  
> <sub>*<sup>c</sup> School of Physical Education, Guangzhou Business School, Guangzhou, 511400, China*</sub>  
> <sub>*<sup>d</sup> Center for Cognitive and Brain Sciences, Institute of Collaborative Innovation, University of Macau, Taipa, Macau, China*</sub>


We implement a **correlation-based network analysis** comparing two experimental conditions (CWL vs. BWL) using sign-flip permutation inference on global, node-level, and edge-level network metrics. The entire analysis is fully reproducible from raw data to final figures in a single Jupyter notebook.

## Method Summary

| Step | Description |
|------|-------------|
| Network construction | Spearman correlation matrix; edges thresholded at *p* < .05 |
| Node metric | Weighted strength |
| Global metrics | Density, global efficiency, clustering coefficient, modularity, characteristic path length |
| Inference | 10,000 sign-flip permutations (paired design) |
| Multiple-comparison correction | Benjamini–Hochberg FDR |

## Key Results

## Key Results

### Figure 1 — Condition-Specific Networks & Strength Change

![Figure 1](output/figures/Fig1_combined_2x2.png)

(A) CWL network. (B) BWL network. (C) Difference network (BWL − CWL). (D) Node strength change.

### Figure 2 — Forest Plot & Strength Rank Changes

![Figure 2](output/figures/Fig2_strength_forest_bump.png)

(A) Node strength ± 95% permutation CI. (B) Bump chart of strength rank migration.

## Repository Structure

```
.
├── data/                       # Raw data (not included in repo)
├── output/figures/             # Generated figures
├── CAN_network_analysis.ipynb  # Main analysis notebook
├── requirements.txt            # Python dependencies
├── LICENSE                     # MIT License
└── README.md                   # This file
```

## Installation

```bash
git clone https://github.com/YKang97/CAN_network_analysis.git
cd CAN_network_analysis
pip install -r requirements.txt
```

## How to Reproduce

1. Clone this repository
2. Install dependencies: `pip install -r requirements.txt`
3. Place your data file at `./data/CAN.xlsx`
4. Open `CAN_network_analysis.ipynb` in Jupyter
5. Run all cells sequentially (Cell 1 → Cell 6)

## Data Availability

Raw data are available upon reasonable request from the corresponding author. The data file is not included in this repository to protect participant privacy.

## Citation

If you use this code, please cite:

```bibtex
@article{Kang2026,
  title   = {Your Paper Title},
  author  = {Kang, Y. and ...},
  journal = {Journal Name},
  year    = {2026},
  doi     = {YOUR_DOI_HERE}
}
```

## License

This project is licensed under the MIT License. See [LICENSE](LICENSE.txt).
