# Transcriptomic Analysis of lncRNA UCA1 in Non-Small Cell Lung Cancer Using Public RNA-seq Data

## Overview
This repository presents a transcriptomic workflow for investigating the expression profile of the long non-coding RNA **UCA1 (Urothelial Cancer Associated 1)** in **non-small cell lung cancer (NSCLC)** using publicly available **RNA-seq** data derived from **The Cancer Genome Atlas (TCGA)**. The project was developed to explore UCA1-associated expression patterns in lung adenocarcinoma-oriented transcriptomic datasets and to demonstrate a reproducible computational framework for preprocessing, exploratory analysis, statistical interrogation, and visualization of cancer transcriptome data.

Long non-coding RNAs are increasingly recognized as important regulators of tumor biology, with reported roles in proliferation, invasion, immune modulation, epithelial–mesenchymal transition, and therapeutic resistance. Among these, **UCA1** has attracted substantial research interest because of its dysregulated expression across multiple cancer types and its proposed contribution to tumor progression. This project focuses on the computational assessment of UCA1 expression within NSCLC-related RNA-seq data, with emphasis on transparent workflow design, reproducibility, and interpretation-ready outputs.

## Project Objective
The primary objective of this project is to evaluate the transcriptomic behavior of **UCA1** in **NSCLC** using public RNA-seq count data and to generate a structured analytical pipeline that can be shared, reused, and extended by other researchers.

Specific aims include:

- importing and organizing public RNA-seq count data for downstream analysis
- performing initial quality inspection and data cleaning
- applying appropriate preprocessing and normalization steps
- examining expression patterns relevant to **UCA1**
- generating descriptive statistics and exploratory visualizations
- producing analysis outputs that support interpretation, reporting, and future hypothesis generation
- establishing a reproducible GitHub-based project structure suitable for academic and portfolio use

## Scientific Background
Non-small cell lung cancer accounts for the majority of lung cancer diagnoses worldwide and remains a major cause of cancer-associated morbidity and mortality. The molecular heterogeneity of NSCLC has driven the use of transcriptomic approaches to better understand regulatory pathways, identify biomarkers, and refine disease stratification.

Long non-coding RNAs, typically defined as transcripts longer than 200 nucleotides with limited protein-coding potential, have emerged as important components of gene regulatory networks in cancer. **UCA1** is one such lncRNA that has been implicated in oncogenic signaling, altered metabolism, proliferation, migration, and drug resistance in diverse malignancies. Investigating UCA1 in publicly accessible NSCLC transcriptomic datasets may therefore provide insight into its expression context and potential biological relevance.

This repository does not claim to establish definitive causal conclusions regarding UCA1 function. Rather, it provides a reproducible computational framework for expression-focused exploration using publicly available RNA-seq data.

## Dataset Source
This project uses publicly available transcriptomic data derived from **The Cancer Genome Atlas (TCGA)**. The analysis was conducted using a count matrix prepared from **TCGA lung adenocarcinoma (TCGA-LUAD)** RNA-seq data for downstream computational analysis.

**Local input file expected by the workflow:**
`data/tcga_luad_count.csv`

Because public RNA-seq count matrices can be large, the raw input data file is **not uploaded to this GitHub repository**. Users who wish to reproduce the analysis should prepare or download the appropriate dataset independently and place the file in a local `data/` directory.

### Data availability note
To run this project locally:

1. create a folder named `data/` in the root project directory
2. place the file `tcga_luad_count.csv` inside that folder
3. ensure the notebook paths match your local folder structure

## Analytical Workflow

The workflow implemented in this repository follows a standard transcriptomic analysis logic adapted for an exploratory expression study.

### 1. Data import
RNA-seq count data are imported into Python for inspection and analysis. This includes loading the prepared count matrix, checking file integrity, and confirming sample and gene dimensions.

### 2. Data inspection and cleaning
The imported dataset is examined for formatting consistency, missing values, duplicated entries, and structural issues that may affect downstream analysis. Gene identifiers and expression columns are reviewed to ensure compatibility with subsequent processing steps.

### 3. Preprocessing and normalization
Depending on the structure of the count matrix, preprocessing may include filtering low-information entries, transforming count values where appropriate, and preparing the dataset for descriptive and comparative exploration. Normalization-related steps are applied to improve interpretability and reduce technical bias in visualization and summary analyses.

### 4. UCA1-focused transcriptomic exploration
A key component of the workflow is the extraction and analysis of expression information relevant to **UCA1**. This stage is designed to assess expression levels, summarize patterns across samples, and position UCA1 within the broader expression context of the NSCLC dataset.

### 5. Descriptive statistics
Basic statistical summaries are generated to characterize the data distribution and support interpretation of observed expression behavior. These outputs may include measures of central tendency, variability, and distribution-aware summaries relevant to transcriptomic data.

### 6. Visualization
Figures are generated to support interpretation and communication of results. Depending on the notebook implementation, these may include:

- UCA1 expression plots
- sample-level distribution plots
- heatmaps
- principal component analysis (PCA) visualizations
- other exploratory graphical summaries

### 7. Output generation
Analysis results, summary files, and figures are saved into dedicated output directories to maintain clean project organization and facilitate downstream reporting.

## Tools and Computational Environment

This project was developed in **Python** and organized for use in **Jupyter Notebook** and **Visual Studio Code (VS Code)**.

### Core tools and libraries
- **Python**
- **pandas** for data handling and tabular manipulation
- **numpy** for numerical operations
- **matplotlib** for plotting
- **seaborn** for statistical visualization
- **scipy** for scientific and statistical functions where applicable

### Recommended environment
- Python 3.10 or later
- Jupyter Notebook or VS Code with Jupyter extension
- Git for version control
- GitHub for repository hosting and sharing

## Expected Outputs

This project is designed to generate interpretation-oriented outputs that may include:

- cleaned or reformatted expression tables
- processed transcriptomic summaries
- UCA1-specific expression results
- exploratory statistical summaries
- publication-style visualizations
- saved intermediate or final result files for downstream use

The exact outputs depend on the notebook version and analytical depth implemented in the repository.

## Reproducibility and Good Research Practice

This repository is structured to support transparent and reproducible computational research practices. Key reproducibility features include:

- organized project folder structure
- clear separation of notebooks, figures, and results
- version control through Git and GitHub
- documentation of expected input file structure
- exclusion of oversized raw data files from the repository
- readable workflow presentation suitable for academic review

To further strengthen reproducibility, future versions may include:

- a `requirements.txt` file
- environment specification using `conda` or `venv`
- metadata documentation for sample annotation
- notebook-to-script conversion for automated execution

## Limitations

Several important limitations should be considered when interpreting this repository:

- the repository is based on publicly available bulk RNA-seq data and may not capture all biological heterogeneity
- conclusions are dependent on the quality and preprocessing of the input count matrix
- transcript-level findings alone do not establish functional causality
- additional validation, including experimental and clinical correlation analyses, would be required for translational interpretation
- dataset upload is omitted from the repository because of file size and GitHub storage constraints

## Future Directions

This workflow can be extended in several ways, including:

- differential expression analysis between biological groups
- integration of clinical metadata
- survival analysis associated with UCA1 expression
- pathway enrichment analysis
- co-expression network construction
- comparison across NSCLC subtypes
- validation using independent datasets or GEO cohorts

## Citation and Acknowledgment

This work is based upon data generated by **The Cancer Genome Atlas (TCGA) Research Network**.

### Suggested acknowledgment
> The results shown here are based upon data generated by The Cancer Genome Atlas (TCGA) Research Network.

This project also makes use of widely adopted open-source Python libraries, including **pandas**, **numpy**, **matplotlib**, **seaborn**, and **scipy**, for data processing, statistical analysis, and visualization.

When using TCGA-derived data in formal academic work, users should cite the relevant TCGA publications, the associated data portal or access framework, and any additional tools used in their own analysis pipeline.

## License

This project is distributed under the terms of the **MIT License**. See the `LICENSE` file for details.

## Author

**Nimalsha Hansani**

This repository was created as part of an academic and research-oriented bioinformatics project focused on transcriptomic analysis of lncRNA UCA1 in NSCLC using public RNA-seq data.
