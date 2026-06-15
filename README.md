# LUAD Multi-Omics Classification

## Executive Summary

Lung adenocarcinoma (LUAD) is the most common subtype of lung cancer and exhibits substantial molecular heterogeneity. Accurate subtype identification is important for prognosis and treatment decisions but traditionally relies on extensive pathological assessment.

This project investigates whether lung cancer molecular subtypes can be predicted using integrated transcriptomic (RNA-seq) and epigenomic (DNA methylation) data from The Cancer Genome Atlas (TCGA).

Using a biologically driven feature selection strategy, differential expression and differential methylation analyses were combined to identify genes showing both transcriptional and epigenetic alterations. These features were then used to train Random Forest and Support Vector Machine classifiers capable of distinguishing LUAD molecular subtypes.

The resulting models achieved high predictive performance on independent test data, demonstrating the potential of multi-omics integration and machine learning for cancer subtype classification.

---

## Project Highlights

- Integrated RNA-seq, DNA methylation and clinical data
- Processed and matched samples from multiple TCGA sources
- Differential Expression Analysis (DESeq2)
- Differential Methylation Analysis (limma)
- Multi-omics feature engineering
- Random Forest and Support Vector Machine models
- Cross-validation and bootstrap validation
- Biological interpretation through pathway enrichment analysis

---

## Data Sources

- TCGA LUAD
- recount3
- TCGAbiolinks
- curatedTCGAData

---

## Workflow

```text
RNA-seq Data
       +
DNA Methylation Data
       +
Clinical Labels
          │
          ▼
Data Cleaning & Quality Control
          │
          ▼
Sample Matching Across Omics Layers
          │
          ▼
Differential Expression Analysis
(DESeq2)
          │
          ▼
Differential Methylation Analysis
(limma)
          │
          ▼
Feature Selection
(DEGs ∩ DMPs)
          │
          ▼
Multi-Omics Integration
          │
          ▼
Machine Learning Models
(Random Forest + SVM)
          │
          ▼
Model Evaluation
          │
          ▼
Biological Annotation
```

---

## Repository Structure

```text
01_data_preprocessing_and_integration.Rmd
    Data acquisition, preprocessing, filtering and integration

02_feature_selection_and_model_training.Rmd
    Differential analyses, feature engineering and model training

03_model_evaluation.Rmd
    Test data evaluation and performance metrics

04_biological_annotation.Rmd
    Pathway enrichment and biological interpretation
```

---

## Results

| Model | Classification Task | Accuracy |
|---------|---------|---------|
| Random Forest | PP vs PI | 93.1% |
| Random Forest | TRU vs PI | 90.3% |
| Random Forest | TRU vs PP | 93.5% |
| Random Forest | Multi-class | 89.2% |
| SVM | Multi-class | 84.2% |

---

## Technologies

### Programming

- R

### Bioinformatics

- DESeq2
- limma
- Bioconductor

### Machine Learning

- Random Forest
- Support Vector Machines

### Data Science

- Feature Engineering
- Cross Validation
- Bootstrap Validation
- Data Visualization

---

## Academic Context

This project was developed as part of the Data Science in the Life Sciences course at Freie Universität Berlin and extended into a complete multi-omics machine learning workflow for lung adenocarcinoma subtype classification.

---

## Full Report

See:

`docs/Final_Project_Report.pdf`
