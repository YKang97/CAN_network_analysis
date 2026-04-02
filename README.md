# Cross-Condition Network Analysis

## Overview

This repository contains the analysis code for the paper:

> **Your Paper Title Here**
> Author 1, Author 2, ... (Year). *Journal Name*. https://doi.org/PAPER_DOI

The code implements a correlation-based network analysis comparing two
experimental conditions (CWL vs. BWL) using sign-flip permutation
inference on global, node-level, and edge-level network metrics.

## Method Summary

| Step | Description |
|------|-------------|
| Network construction | Spearman correlation matrix, edges thresholded at p < .05 |
| Node metric | Weighted strength |
| Global metrics | Density, efficiency, clustering, modularity, path length |
| Inference | 10,000 sign-flip permutations (paired design) |
| Correction | Benjamini–Hochberg FDR |

## Key Results

### Figure 1 — Condition-Specific Networks

| (A) CWL Network | (B) BWL Network |
|:----------------:|:----------------:|
| ![CWL Network](output/figures/Fig1a_CWL_network.png) | ![BWL Network](output/figures/Fig1b_BWL_network.png) |

### Figure 1c — Difference Network (BWL − CWL)

![Difference Network](output/figures/Fig1c_difference_network.png)

### Figure 1d — Node Strength Change

![Strength Change Bar](output/figures/Fig1d_strength_change_bar.png)

### Figure 2 — Dissociation: Univariate vs Network Significance

![Dissociation](output/figures/Fig2_dissociation.png)

### Figure 3 — Forest Plot (Node Strength with 95% Permutation CI)

![Forest Plot](output/figures/Fig3_forest_plot.png)

### Figure 4 — Intra- vs Inter-subsystem Edge Changes

![Subsystem Edges](output/figures/Fig4_subsystem_edges.png)

### Figure 5 — Strength Rank Changes (Bump Chart)

![Bump Chart](output/figures/Fig5_bump_chart.png)

## Repository Structure