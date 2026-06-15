# Notebooks

This directory contains the R Markdown notebooks used throughout the LUAD multi-omics classification workflow.

The notebooks are designed to be executed sequentially, as each stage depends on outputs generated in previous steps.

## Execution Order

### 01_data_preprocessing_and_integration.Rmd

* Download and preprocessing of TCGA LUAD datasets
* RNA-seq and DNA methylation quality control
* Sample matching across omics layers
* Clinical metadata integration
* Stratified train/test splitting

### 02_feature_selection_and_model_training.Rmd

* Differential expression analysis (DESeq2)
* Differential methylation analysis (limma)
* Multi-omics feature selection
* Random Forest and Support Vector Machine model training

### 03_model_evaluation.Rmd

* Independent test set evaluation
* Confusion matrices
* Performance metrics
* Bootstrap validation

### 04_biological_annotation.Rmd

* Functional enrichment analysis
* Pathway annotation
* Gene overlap analysis
* Biological interpretation of predictive features

## Requirements

The analysis was developed in R using Bioconductor and CRAN packages. Refer to the repository root README for software dependencies and project overview.
