# Lung Adenocarcinoma Transcriptomic Analysis using GEO RNA-seq Datasets

## Overview

This repository contains a complete bioinformatics and machine learning workflow for identifying transcriptomic biomarkers associated with Lung Adenocarcinoma (LUAD) using publicly available GEO RNA-seq datasets.

The project integrates differential gene expression analysis, functional enrichment, co-expression network analysis, immune cell deconvolution, protein–protein interaction (PPI) analysis, feature selection, and machine learning classification into a unified reproducible pipeline.

---

## Project Highlights

* Multi-cohort GEO RNA-seq integration
* Differential Expression Analysis using DESeq2
* GO & KEGG Functional Enrichment
* Co-expression Network Analysis using CEMiTool
* PPI Network Construction & Hub Gene Detection
* Immune Cell Infiltration Analysis using CIBERSORT
* LASSO-based Biomarker Selection
* Machine Learning Models:

  * Random Forest (RF)
  * Support Vector Machine (SVM)
  * Gradient Boosting Machine (GBM)
  * Artificial Neural Network (ANN)

---

## Datasets Used

| GEO Accession | Description         | Usage               |
| ------------- | ------------------- | ------------------- |
| GSE229705     | LUAD RNA-seq Counts | Training            |
| GSE140343     | LUAD RNA-seq Counts | Training            |
| GSE40419      | LUAD RNA-seq RPKM   | External Validation |

---

## Workflow

```text
GEO Data Acquisition
        ↓
Preprocessing & Cleaning
        ↓
70/30 Patient-Level Splitting
        ↓
Batch Effect Correction
        ↓
DESeq2 Differential Expression
        ↓
GO / KEGG Enrichment
        ↓
CEMiTool Co-expression Analysis
        ↓
PPI Network Construction
        ↓
Immune Cell Infiltration Analysis
        ↓
LASSO Feature Selection
        ↓
Machine Learning Classification
        ↓
External Validation
```

---

## Key Results

* 16,282 common genes analyzed
* 2,421 significant DEGs identified
* Strong enrichment of:

  * Immune pathways
  * Cell cycle pathways
  * Extracellular matrix remodeling
* Hub genes identified:

  * CD79A
  * MS4A1
  * CXCL13
  * IRF4
  * JCHAIN
* Best external ROC-AUC:

  * ANN = 0.995
* Best balanced external performance:

  * Random Forest

---

## Technologies & Packages

### R Packages

* DESeq2
* clusterProfiler
* enrichplot
* CEMiTool
* limma
* igraph
* IOBR
* ggplot2
* pheatmap

### Python Packages

* scikit-learn
* pandas
* numpy
* matplotlib
* seaborn

---

## Repository Structure

```text
├── assets/
│   ├── images/
│   └── pdf/
├── data/
├── scripts/
├── results/
├── index.html
├── README.md
└── LICENSE
```

---

## Figures Included

* PCA plots
* Volcano plots
* DEG heatmaps
* GO enrichment plots
* KEGG pathway plots
* Co-expression module analysis
* PPI network visualization
* Immune infiltration plots
* ROC curves
* Confusion matrices
* Feature importance plots

---

## Biological Interpretation

This study demonstrates that LUAD transcriptomes exhibit strong immune-related and extracellular matrix remodeling signatures. Co-expression and PPI analyses highlighted immune-associated hub genes involved in B-cell activation and adaptive immune signaling.

Machine learning models trained on integrated transcriptomic data achieved strong classification performance and successfully generalized to an independent external cohort.

---

## Research Significance

This project provides:

* A reproducible LUAD bioinformatics workflow
* Cross-dataset biomarker validation
* Integration of systems biology and machine learning
* Potential diagnostic biomarker candidates
* Insights into LUAD immune microenvironment remodeling

---

## Author

**Rakesh Kumar A**
Bioinformatics Researcher
Bangalore, India

---

## Citation

If you use this project or workflow, please cite the corresponding report and GEO datasets used in this analysis.

---

## License

This project is intended for academic and research purposes.
