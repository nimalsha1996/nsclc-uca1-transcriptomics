# nsclc-uca1-transcriptomics
# Transcriptomic Analysis of lncRNA UCA1 in Non-Small Cell Lung Cancer (NSCLC)

## Abstract
This repository provides a comprehensive analysis of the long non-coding RNA **UCA1** in **non-small cell lung cancer (NSCLC)** using publicly available **TCGA RNA-seq data**.  
The workflow includes data acquisition, preprocessing, normalization, differential expression analysis, and visualization, with the goal of understanding UCA1 expression patterns, clinical correlations, and potential roles in NSCLC progression.

## Background
Long non-coding RNAs (lncRNAs) are critical regulators in cancer biology. **UCA1 (Urothelial Cancer Associated 1)** has been implicated in tumor growth, metastasis, and drug resistance in multiple cancers, including NSCLC.  
This project aims to provide a **reproducible workflow** for analyzing UCA1 expression and its clinical significance in NSCLC patients, offering insights for further functional studies or biomarker development.

## Repository Structure
| Folder / File       | Description |
|--------------------|-------------|
| `data/`            | Scripts to download TCGA data or small metadata files (raw RNA-seq data not included due to size) |
| `notebooks/`       | Jupyter notebooks for exploratory data analysis |
| `scripts/`         | Reproducible scripts for preprocessing, differential expression, and visualization |
| `results/`         | Processed tables, differential expression results, and intermediate outputs |
| `figures/`         | High-quality plots (boxplots, heatmaps, survival curves) |
| `environment.yml`  | Conda environment file to ensure reproducibility |
| `LICENSE`          | License information (MIT License) |
| `README.md`        | This file |
| `CITATION.md`      | Instructions for citing this repository |

## Methods Overview
1. **Data Acquisition**  
   - TCGA LUAD (Lung Adenocarcinoma) RNA-seq counts and clinical metadata were obtained from the GDC portal.
2. **Preprocessing**  
   - Filtering low-expression genes  
   - Aligning samples between count matrix and clinical metadata
3. **Normalization & Quality Control**  
   - Log2 transformation, CPM normalization, or DESeq2 normalization  
   - PCA and sample clustering for QC
4. **Differential Expression Analysis**  
   - Compare high vs. low UCA1 expression groups  
   - Statistical tests with multiple testing correction (FDR)
5. **Visualization**  
   - Boxplots, heatmaps, correlation plots, survival curves
6. **Interpretation**  
   - Integrate expression results with clinical features  
   - Identify potential biological implications

