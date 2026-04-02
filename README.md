# Cross-Condition Network Analysis

[![Python 3.8+](https://img.shields.io/badge/python-3.8%2B-blue.svg)](https://www.python.org/)
[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE.txt)

## Overview

This repository contains the data and analysis code for the paper:

> **Your Paper Title Here**
> Author 1, Author 2 (2026). *Journal Name*.（← 换成期刊名）

We implement a **correlation-based network analysis** comparing two experimental conditions (CWL vs. BWL) using sign-flip permutation inference on global, node-level, and edge-level network metrics. The entire analysis is fully reproducible from raw data to final figures in a single Jupyter notebook.

## Method Summary

| Step | Description |
|------|-------------|
| Network construction | Spearman correlation matrix; edges thresholded at *p* < .05 |
| Node metric | Weighted strength |
| Global metrics | Density, global efficiency, clustering coefficient, modularity, characteristic path length |
| Inference | 10 000 sign-flip permutations (paired design) |
| Multiple-comparison correction | Benjamini–Hochberg FDR |

## Key Results

### Figure 1 — Condition-Specific Networks

| (A) CWL Network | (B) BWL Network |
|:----------------:|:----------------:|
| ![CWL](output/figures/Fig1a_CWL_network.png) | ![BWL](output/figures/Fig1b_BWL_network.png) |

### Figure 1c — Difference Network (BWL − CWL)

![Difference Network](output/figures/Fig1c_difference_network.png)

### Figure 1d — Node Strength Change

![Strength Change](output/figures/Fig1d_strength_change_bar.png)

### Figure 2 — Dissociation: Univariate vs. Network Significance

![Dissociation](output/figures/Fig2_dissociation.png)

### Figure 3 — Forest Plot (Node Strength ± 95 % Permutation CI)

![Forest Plot](output/figures/Fig3_forest_plot.png)

### Figure 4 — Intra- vs. Inter-subsystem Edge Changes

![Subsystem Edges](output/figures/Fig4_subsystem_edges.png)

### Figure 5 — Strength Rank Changes (Bump Chart)

![Bump Chart](output/figures/Fig5_bump_chart.png)

## Repository Structure