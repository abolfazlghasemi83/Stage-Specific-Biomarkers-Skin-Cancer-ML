<a id="readme-top"></a>

<div align="center">

# Stage-Specific Biomarkers Skin Cancer ML

**Machine Learning Framework for Stage-Specific Transcriptomic Biomarker Discovery in Skin Cancer**

<a href="./Stage_Specific_Biomarker_Pipeline/README.md">
<img src="https://img.shields.io/badge/Pipeline%20Documentation-2563EB?style=for-the-badge" alt="Pipeline Documentation">
</a>

<a href="https://github.com/abolfazlghasemi83/Stage-Specific-Biomarkers-Skin-Cancer-ML/releases/latest">
<img src="https://img.shields.io/badge/Dataset%20Release-2EA44F?style=for-the-badge&logo=github&logoColor=white" alt="Dataset Release">
</a>

<a href="./Supplementary-Tables/README.md">
<img src="https://img.shields.io/badge/Supplementary%20Tables-B59B00?style=for-the-badge" alt="Supplementary Tables">
</a>

<a href="./LICENSE">
<img src="https://img.shields.io/badge/License-MIT-181717?style=for-the-badge&logo=github&logoColor=white" alt="License">
</a>

</div>

<p align="center">
This repository accompanies the study <strong>Stage-Specific Transcriptomic Biomarker Discovery in Skin Cancer Using Machine Learning and Statistical Approaches</strong>.
</p>

<div align="center">

[Overview](#overview) • [Publication](#associated-publication) • [Quick Facts](#quick-facts) • [Repository Structure](#repository-structure) • [Dataset](#dataset-availability) • [Pipeline](#pipeline-documentation) • [Results](#repository-outputs) • [Citation](#citation) • [License](#license) • [Contact](#contact)

</div>

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

Stage-Specific-Biomarkers-Skin-Cancer-ML/
│
├── Data/
│ └── README.md
│
├── Stage_Specific_Biomarker_Pipeline/
│ ├── Pictures/
│ └── README.md
│
├── Supplementary-Tables/
│ └── README.md
│
├── LICENSE
└── README.md

| Folder | Description |
|--------|-------------|
| `Data/` | Dataset information, metadata, and download instructions for the GitHub Release dataset |
| `Stage_Specific_Biomarker_Pipeline/` | Complete pipeline documentation, workflow description, pseudocode, installation guide, required software, and pipeline figures |
| `Supplementary-Tables/` | Supplementary tables, model outputs, manuscript figures, biomarker summaries, and supporting material |
| `LICENSE` | Repository license |
| `README.md` | Main project documentation |

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

👉 [**`Stage_Specific_Biomarker_Pipeline/README.md`**](./Stage_Specific_Biomarker_Pipeline/README.md)

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
TCGA-SKCM Dataset
│
▼
Data Cleaning
│
▼
Normalization
│
▼
Dimensionality Reduction
(PCA / Factor Analysis)
│
▼
35 Machine Learning
and Statistical Models
│
▼
Feature Importance
│
▼
Top Biomarker Selection
│
▼
Model Comparison
│
▼
Stage-Specific Biomarker Discovery

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

<p align="center">Made for reproducible transcriptomic biomarker discovery using machine learning.</p>

<p align="center"><a href="#readme-top">Back to top</a></p>

## Repository Structure
