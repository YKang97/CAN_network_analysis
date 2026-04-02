# Cross-Condition Network Analysis

[![DOI](https://zenodo.org/badge/DOI/YOUR_DOI_HERE.svg)](https://doi.org/YOUR_DOI_HERE)

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

## Repository Structure