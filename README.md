# SUGARFuseNet — GBMT-SLID Repository

**SUGARFuseNet: Diffusion-Driven Domain Adaptation and Bimodal Bitemporal Fusion for Global Landslide Segmentation**  
Repository for the GBMT-SLID dataset, the Diffusion-driven Data Enhancement Strategy (DES), and the SUGARFuseNet segmentation model used in the associated paper.

---

## Overview

This repository contains data preprocessing pipelines, diffusion-based data enhancement (conditioned translator + DDIM augmentation), model implementations, training/validation code, and inference utilities for global bimodal-bitemporal landslide segmentation. The work introduces the GBMT-SLID dataset (29 global regions; Sentinel-2 pre/post + Copernicus DEM) and the SUGARFuseNet architecture which fuses optical and topographic information across two time steps.

Key highlights
- GBMT-SLID — a globally distributed bimodal-bitemporal landslide dataset (pre/post Sentinel-2 + Copernicus DEM).
- DES — Condition Diffusion Model Translator (cDMT) for domain harmonization + DDIM augmentation to handle imbalance and regional variance.
- SUGARFuseNet — dual-branch encoder with Shared Gated Paired Attention (SGPA), Bimodal Bitemporal Information Fusion Module (BBIFM), Feature Aggregation (FA), and Unified Upsampling (UFUM).

### Performance (summary from experiments)
On GBMT-SLID, SUGARFuseNet achieves:
- Recall: **94.6%**  
- F1-score: **80.5%**  
- IoU: **67.5%**

Generalization on five unseen ROIs (DRC, Uganda, Myanmar, Philippines, Colombia):
- Mean F1: **55.85%**  
- Mean IoU: **38.98%**

Ablations confirm the value of topography and each bespoke module (SGPA, BBIFM, UFUM), and indicate DES yields substantial improvements over traditional augmentation (F1 uplift ≈ **26.94%**).

---

## Repository layout

