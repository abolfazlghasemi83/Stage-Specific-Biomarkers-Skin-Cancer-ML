<a id="readme-top"></a>

<div align="center">

# Stage-Specific Biomarkers Skin Cancer ML

**Machine Learning Framework for Stage-Specific Transcriptomic Biomarker Discovery in Skin Cancer**

<p align="center">

<a href="https://github.com/abolfazlghasemi83/Stage-Specific-Biomarkers-Skin-Cancer-ML/tree/main/Stage_Specific_Biomarker_Pipeline">
<img src="https://img.shields.io/badge/Pipeline-Documentation-blue?style=for-the-badge&logo=github" />
</a>

<a href="https://github.com/abolfazlghasemi83/Stage-Specific-Biomarkers-Skin-Cancer-ML/releases/latest">
<img src="https://img.shields.io/badge/Dataset-Release-success?style=for-the-badge&logo=github" />
</a>

<a href="https://github.com/abolfazlghasemi83/Stage-Specific-Biomarkers-Skin-Cancer-ML/tree/main/Supplementary-Tables">
<img src="https://img.shields.io/badge/Supplementary-Materials-orange?style=for-the-badge&logo=github" />
</a>

</p>

This repository accompanies the study **Stage-Specific Transcriptomic Biomarker Discovery in Skin Cancer Using Machine Learning and Statistical Approaches**.

<p align="center">

<a href="#overview">Overview</a> •
<a href="#associated-publication">Publication</a> •
<a href="#quick-facts">Quick Facts</a> •
<a href="#repository-structure">Repository Structure</a> •
<a href="#dataset-availability">Dataset</a> •
<a href="#pipeline-documentation">Pipeline</a> •
<a href="#supplementary-material">Supplementary</a> •
<a href="#repository-outputs">Results</a> •
<a href="#citation">Citation</a> •
<a href="#license">License</a> •
<a href="#contact">Contact</a>

</p>

---

## Overview

This repository provides the complete computational workflow for identifying transcriptomic biomarkers associated with skin cancer progression using TCGA-SKCM gene expression data.

The repository includes:

- Complete machine learning workflow
- Pipeline documentation
- Pseudocode
- Analysis outputs
- Supplementary tables
- GitHub Release dataset
- Figures used in the manuscript

The analysis was performed on **413 clinically annotated TCGA-SKCM samples** containing expression measurements for **16,049 genes**, followed by preprocessing, dimensionality reduction, feature ranking, and comparative evaluation of **35 machine learning and statistical algorithms** across multiple stage transitions.

The strongest supervised performance was observed for **Stage III vs Stage IV**, while recurrent high-priority biomarkers included **OR2A10, HIST1H3B, FAM213B, SSFA1, ADAM19, CAMTA1, CETP, and SLC25A18**.

---

## Associated Publication

**Stage-Specific Transcriptomic Biomarker Discovery in Skin Cancer Using Machine Learning and Statistical Approaches**

**Abolfazl Ghasemi, Mohammad-Reza Shahbazi, Siamak Salimy\*, Amir-Mohammad Asgari, Omid Taheri**

**1.** Department of Computer Engineering, National University of Skills (NUS), Tehran, Iran

**Corresponding author:** Siamak Salimy  
**Email:** [siamak.salimy@email.com](mailto:siamak.salimy@email.com)

**Additional contact:** [abolfazlghasemi55@gmail.com](mailto:abolfazlghasemi55@gmail.com)

**Manuscript status:** Under review

---

## Quick Facts

| Item | Value |
|------|-------|
| Dataset | TCGA-SKCM |
| Samples | 413 |
| Genes | 16,049 |
| Algorithms | 35 |
| Task | Stage‑specific biomarker identification |
| Primary outputs | Accuracy, precision, normalized importance, top biomarkers |
| Dataset distribution | GitHub Releases |

---
---

## Repository Structure

The repository is organized into dedicated modules for the dataset, computational workflow, supplementary materials, and project documentation. This structure separates data resources from methodological documentation and supporting files, improving reproducibility and ease of navigation.


## Repository Structure

| Directory | Description |
|-----------|-------------|
| **[`Data/`](https://github.com/abolfazlghasemi83/Stage-Specific-Biomarkers-Skin-Cancer-ML/tree/main/Data)** | Dataset description, metadata, download instructions, and links to the GitHub Release containing the complete TCGA-SKCM expression dataset. |
| **[`Stage_Specific_Biomarker_Pipeline/`](https://github.com/abolfazlghasemi83/Stage-Specific-Biomarkers-Skin-Cancer-ML/tree/main/Stage_Specific_Biomarker_Pipeline)** | Documentation of the complete computational workflow, including installation instructions, software requirements, preprocessing pipeline, pseudocode, execution workflow, and pipeline figures. |
| **[`Supplementary-Tables/`](https://github.com/abolfazlghasemi83/Stage-Specific-Biomarkers-Skin-Cancer-ML/tree/main/Supplementary-Tables)** | Supplementary tables, complete model outputs, publication figures, biomarker summaries, and additional supporting materials associated with the manuscript. |
| **[`LICENSE`](https://github.com/abolfazlghasemi83/Stage-Specific-Biomarkers-Skin-Cancer-ML/blob/main/LICENSE)** | License governing the use and distribution of the repository. |


---

## Dataset Availability

The original TCGA-SKCM expression dataset is distributed through the repository's **GitHub Releases** because the Excel file exceeds GitHub's recommended repository size.

| Item | Description |
|------|-------------|
| Dataset | `skcm_tcga.xlsx` |
| Source | TCGA Skin Cutaneous Melanoma (TCGA-SKCM) |
| Samples | 413 |
| Genes | 16,049 |
| Distribution | GitHub Release Asset |

Download the complete dataset from the latest release:

👉 [**Latest Release**](https://github.com/abolfazlghasemi83/Stage-Specific-Biomarkers-Skin-Cancer-ML/releases/latest)

The dataset contains the normalized gene-expression matrix used throughout the complete machine learning workflow.

---

## Pipeline Documentation

The complete computational workflow is documented in:

👉 [**`Stage_Specific_Biomarker_Pipeline/README.md`**](./Stage_Specific_Biomarker_Pipeline/)

The documentation includes:

- Installation guide
- Required software
- Python packages
- IBM SPSS Modeler workflow
- Complete pseudocode
- Data preprocessing
- PCA / Factor Analysis
- Feature selection
- Machine learning workflow
- Biomarker extraction
- Result generation
- Output structure

Pipeline figures are stored in:

👉 [**`Stage_Specific_Biomarker_Pipeline/Pictures/`**](./Stage_Specific_Biomarker_Pipeline/Pictures/)

### Study Workflow

```text
TCGA-SKCM Gene Expression Dataset
                │
                ▼
       Clinical Data Integration
                │
                ▼
        Data Preprocessing
        • Quality Control
        • Missing Value Handling
        • Normalization
                │
                ▼
     Dimensionality Reduction
      (PCA / Factor Analysis)
                │
                ▼
      Feature Selection & Ranking
                │
                ▼
  35 Machine Learning & Statistical Models
                │
                ▼
 Feature Importance Estimation
                │
                ▼
 Top Biomarker Identification
                │
                ▼
 Comparative Model Evaluation
 (Accuracy, Precision, Importance)
                │
                ▼
 Stage-Specific Biomarker Discovery
```
---

## Repository Outputs

| Output | Description |
|--------|-------------|
| **Accuracy** | Model accuracy for every stage transition |
| **Precision** | Weighted precision values |
| **Top 20 Biomarkers** | Highest-ranked genes for every algorithm |
| **Feature Importance** | Normalized importance scores |
| **Stage Results** | Individual stage transition analyses |
| **Excel Reports** | Structured output tables |
| **Supplementary Tables** | Manuscript supplementary files |

### Main Findings

The strongest supervised classification performance was observed for:

- **Stage III → Stage IV** (Accuracy = 0.862, Precision = 0.760)

Frequently identified biomarkers include:

- **OR2A10**
- **HIST1H3B**
- **FAM213B**
- **SSFA1**
- **ADAM19**
- **CAMTA1**
- **CETP**
- **SLC25A18**

Functional enrichment analysis associated these biomarkers with:

- Extracellular matrix organization
- Epigenetic regulation
- Lipid metabolism
- Calcium signaling
- Hippo signaling
- Protein‑protein interaction networks

---

## Supplementary Material

Additional analyses are available in:

👉 [**`Supplementary-Tables/README.md`**](./Supplementary-Tables/README.md)

The supplementary folder contains:

- Supplementary Table S1 (complete enrichment statistics)
- Model outputs
- Biomarker summaries
- Supporting charts
- Manuscript supplementary documents

### Figures

All manuscript figures are available in:

👉 [**`Stage_Specific_Biomarker_Pipeline/Pictures/`**](./Stage_Specific_Biomarker_Pipeline/Pictures/)

including:

- Graphical Abstract
- Pipeline Overview
- KEGG Pathway Figures
- Enrichment Plots
- PPI Network
- Workflow Diagrams

---

## Reproducibility

This repository contains all documentation required to reproduce the complete computational workflow.

The only external component distributed separately is the original expression dataset, which is available through the [GitHub Release page](https://github.com/abolfazlghasemi83/Stage-Specific-Biomarkers-Skin-Cancer-ML/releases/latest).

---

## Citation

If this repository contributes to your research, please cite:

> Ghasemi A., Shahbazi M.R., Salimy S., Asgari A.M., Taheri O.  
> *Stage-Specific Transcriptomic Biomarker Discovery in Skin Cancer Using Machine Learning and Statistical Approaches*  
> **Status:** Under review

---

## License

This project is released under the terms of the [MIT License](./LICENSE).

---

## Contact

**Siamak Salimy** (Corresponding Author)  
Email: [siamak.salimy@email.com](mailto:siamak.salimy@email.com)

**Additional contact:**  
Abolfazl Ghasemi  
Email: [abolfazlghasemi55@gmail.com](mailto:abolfazlghasemi55@gmail.com)

---
## Contents

| File | Description |
|------|-------------|
| **Supplementary Table S1.xlsx** | Seven-sheet supplementary workbook presenting comprehensive functional enrichment analyses for the identified stage-specific biomarkers, including **GO Biological Process, KEGG Pathway, Reactome Pathway, WikiPathways, DisGeNET Disease Associations, HuBMAP Tissue Mapping, and DrugAtlas** analyses. |
| **Models-Output.xlsx** | Consolidated machine learning outputs, including model performance metrics and feature importance results. |
| **Article Pictures.pdf** | Figures prepared for the manuscript, including workflow diagrams, pathway analyses, enrichment plots, and related visualizations. |

---

## Purpose

The supplementary files provide additional information that complements the main manuscript, including:

- Complete model outputs
- Supplementary biomarker rankings
- Performance summaries
- Supporting figures
- Additional analyses not included in the main text

---

## Related Resources

- ⚙️ **Pipeline Documentation**  
  https://github.com/abolfazlghasemi83/Stage-Specific-Biomarkers-Skin-Cancer-ML/tree/main/Stage_Specific_Biomarker_Pipeline

- 📦 **Dataset Release**  
  https://github.com/abolfazlghasemi83/Stage-Specific-Biomarkers-Skin-Cancer-ML/releases/latest

---

<p align="center">
This directory contains the supplementary material supporting the manuscript.
</p>
