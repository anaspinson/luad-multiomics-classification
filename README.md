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
luad-multiomics-classification/
│
├── README.md
│   Project overview, workflow, results and instructions
│
├── ABOUT_THE_PROJECT.md
│   Project background, contributions and lessons learned
│
├── docs/
│   ├── README.md
│   └── Final_Project_Report.pdf
│
├── notebooks/
│   ├── README.md
│   ├── 01_data_preprocessing_and_integration.Rmd
│   ├── 02_feature_selection_and_model_training.Rmd
│   ├── 03_model_testing_and_evaluation.Rmd
│   └── 04_biological_annotation.Rmd
│
├── figures/
│   ├── README.md
│   └── project_figures
│
├── results/
│   ├── README.md
│   └── analysis_outputs
│
└── environment/
    ├── README.md
    └── session_info.txt

```

This shows the complete repository.

---

## Section 2: Analysis Workflow

Then immediately below:

````markdown
## Analysis Workflow

The notebooks are intended to be executed sequentially.

### 01 Data Preprocessing and Integration

- Download TCGA LUAD datasets
- Perform quality control
- Filter samples and genes
- Match RNA-seq and methylation samples
- Create training and testing datasets

### 02 Feature Selection and Model Training

- Differential expression analysis (DESeq2)
- Differential methylation analysis (limma)
- Multi-omics feature selection
- Random Forest training
- Support Vector Machine training

### 03 Model Evaluation

- Evaluate models on independent test data
- Generate confusion matrices
- Calculate performance metrics
- Bootstrap validation

### 04 Biological Annotation

- Pathway enrichment analysis
- Functional annotation
- Gene overlap analysis
- Biological interpretation

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
