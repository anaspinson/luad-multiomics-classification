# Figures

This directory contains selected visualizations generated throughout the LUAD multi-omics classification workflow.

The figures illustrate key stages of the analysis pipeline, from exploratory data analysis and multi-omics integration to machine learning model performance and biological interpretation.

---

# Featured Figures

## 1. Exploratory Data Analysis

### Principal Component Analysis (PCA)

![PCA](pca_subtypes.jpg)

This PCA visualization was generated during the exploratory analysis stage of the RNA-seq dataset.

Key observations:

* Primary tumor samples separate clearly from normal tissue samples.
* Molecular subtypes show distinct clustering patterns.
* Tumor stage exhibits substantially weaker separation than subtype.

These observations provided early evidence that subtype classification would likely be more successful than stage classification and guided subsequent feature selection and modeling decisions.

**Analysis stage:** Data exploration and quality assessment.

---

## 2. Multi-Omics Sample Integration

### RNA-seq and DNA Methylation Sample Intersection

![Sample Intersection](sample_intersection.jpg)

A critical step in multi-omics integration is ensuring that samples are available across all data modalities.

This figure shows:

* The overlap between RNA-seq and methylation datasets.
* The final set of matched primary tumor samples used for downstream analyses.
* The reduction of the original datasets into a harmonized multi-omics cohort.

This integration step ensured that transcriptomic and epigenomic measurements originated from the same biological samples.

**Analysis stage:** Data preprocessing and integration.

---

## 3. Machine Learning Performance

### Random Forest Multi-Class Classification Results

![RF Multi-class Performance](multiclass_RF_confusion_matrix.jpg)

The Random Forest classifier achieved strong performance when predicting LUAD molecular subtypes using integrated transcriptomic and methylation features.

Highlights:

* Multi-class accuracy of approximately 89%.
* High sensitivity and specificity across classes.
* Stable performance confirmed through bootstrap validation.

This figure summarizes the predictive capability of the final multi-omics classification model.

**Analysis stage:** Model testing and evaluation.

---

## 4. Biological Interpretation

### Top Predictive Genes

![Top Overlapping Genes](top_overlapping_genes.jpg)

This figure shows the highest-ranking genes identified through the combined importance scores of Random Forest and Support Vector Machine models.

Notable markers include:

* CEP55
* EXO1
* CCNB1
* CABYR
* CDCA5

These genes were subsequently investigated through pathway enrichment analysis to better understand the biological mechanisms associated with LUAD subtype differentiation.

**Analysis stage:** Biological annotation and interpretation.

---

# Figure Categories

The complete collection of figures documents:

* Data exploration and quality control
* Sample filtering and integration
* Differential expression analysis
* Differential methylation analysis
* Feature selection
* Machine learning model evaluation
* Biological interpretation and pathway enrichment

Together, these visualizations provide a reproducible record of the full end-to-end multi-omics analysis workflow.
