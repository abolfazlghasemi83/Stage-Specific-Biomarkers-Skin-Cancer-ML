# Stage-Specific Biomarkers Skin Cancer ML

<p align="center">

Machine Learning Framework for Stage-Specific Transcriptomic Biomarker Discovery in Skin Cancer

</p>

<p align="center">

<a href="https://github.com/abolfazlghasemi83/Stage-Specific-Biomarkers-Skin-Cancer-ML">
<img src="https://img.shields.io/badge/GitHub-Repository-black?logo=github">
</a>

<a href="../../releases">
<img src="https://img.shields.io/badge/Dataset-GitHub%20Release-blue">
</a>

<a href="./LICENSE">
<img src="https://img.shields.io/badge/License-MIT-green">
</a>

<a href="#">
<img src="https://img.shields.io/badge/Algorithms-35-orange">
</a>

<a href="#">
<img src="https://img.shields.io/badge/Samples-413-success">
</a>

<a href="#">
<img src="https://img.shields.io/badge/Genes-16,049-red">
</a>

</p>

---

## Overview

This repository accompanies the research article

**Stage-Specific Transcriptomic Biomarker Discovery in Skin Cancer Using Machine Learning and Statistical Approaches**

The project provides the complete computational workflow used for identifying transcriptomic biomarkers associated with skin cancer progression using TCGA-SKCM gene expression data.

The repository includes

* Complete machine learning workflow
* Pipeline documentation
* Pseudocode
* Analysis outputs
* Supplementary tables
* GitHub Release dataset
* Figures used in the manuscript
* Reproducible project structure

The analysis was performed on **413 clinically annotated TCGA-SKCM samples** containing expression measurements for **16,049 genes**, followed by preprocessing, dimensionality reduction, feature ranking and comparative evaluation of **35 machine learning and statistical algorithms** across multiple stage transitions.

---

# Repository Structure

```
Stage-Specific-Biomarkers-Skin-Cancer-ML
│
├── Data/
│   ├── Dataset information
│   ├── Release download instructions
│   └── Metadata
│
├── Pictures/
│   ├── Graphical Abstract
│   ├── Pipeline overview
│   ├── Figures
│   └── Workflow diagrams
│
├── Results/
│   ├── Model outputs
│   ├── Accuracy tables
│   ├── Precision tables
│   ├── Feature importance
│   ├── Biomarker rankings
│   └── Excel exports
│
├── Stage_Specific_Biomarker_Pipeline/
│   ├── Complete pseudocode
│   ├── Installation guide
│   ├── Required packages
│   ├── Pipeline documentation
│   ├── Algorithm descriptions
│   └── Execution workflow
│
├── Supplementary-Tables/
│   ├── Supplementary_Table_S1.xlsx
│   ├── Charts.docx
│   └── Additional supplementary material
│
├── README.md
└── LICENSE
```

---

# Repository Contents

| Folder | Description |
|---------|-------------|
| **Data** | Dataset description, metadata and GitHub Release information |
| **Pictures** | Graphical abstract, workflow figures and manuscript illustrations |
| **Results** | Complete model outputs, feature importance, biomarker rankings and exported analysis |
| **Stage_Specific_Biomarker_Pipeline** | Pipeline documentation, installation guide, pseudocode and execution details |
| **Supplementary-Tables** | Supplementary tables, enrichment results and manuscript supporting documents |

---

# Dataset

The complete TCGA-SKCM expression dataset is distributed through the GitHub **Releases** page because the original dataset exceeds GitHub's recommended repository size.

| Item | Description |
|------|-------------|
| Dataset | skcm_tcga.xlsx |
| Source | TCGA Skin Cutaneous Melanoma (TCGA-SKCM) |
| Samples | 413 |
| Genes | 16,049 |
| Distribution | GitHub Release Asset |

Download the dataset from

**Releases → Latest Release**

```
skcm_tcga.xlsx
```

---

# Machine Learning Pipeline

The complete workflow is documented inside

```
Stage_Specific_Biomarker_Pipeline/
```

The documentation includes

* Installation
* Required software
* Python packages
* IBM SPSS Modeler workflow
* Complete pseudocode
* Data preprocessing
* PCA / Factor Analysis
* Feature Selection
* Model execution
* Biomarker extraction
* Output generation
* Result export

---

# Study Workflow

The analysis follows the pipeline below

```
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

Stage-specific Biomarker Discovery
```

---

# Repository Outputs

The repository contains

| Output | Description |
|---------|-------------|
| Accuracy | Model accuracy for every stage transition |
| Precision | Weighted precision values |
| Top 20 Biomarkers | Highest ranked genes for every algorithm |
| Feature Importance | Normalized importance scores |
| Stage Results | Individual stage transition analyses |
| Excel Reports | Structured output tables |
| Supplementary Tables | Manuscript supplementary files |

---

# Main Findings

The strongest supervised classification performance was observed for

**Stage III → Stage IV**

Frequently identified biomarkers include

* OR2A10
* HIST1H3B
* FAM213B
* SSFA1
* ADAM19
* CAMTA1
* CETP
* SLC25A18

Functional enrichment analysis associated these biomarkers with

* Extracellular matrix organization
* Epigenetic regulation
* Lipid metabolism
* Calcium signaling
* Hippo signaling
* Protein-protein interaction networks

---

# Supplementary Material

Additional analyses are available inside

```
Supplementary-Tables/
```

including

* Supplementary Table S1
* Enrichment analysis
* Biomarker summaries
* Supporting charts
* Manuscript supplementary documents

---

# Results

All generated outputs are available in

```
Results/
```

including

* Accuracy tables
* Precision tables
* Feature importance
* Biomarker rankings
* Exported Excel files
* Stage-specific analyses

---

# Figures

All manuscript figures are available in

```
Pictures/
```

including

* Graphical Abstract
* Pipeline Overview
* KEGG Pathway Figures
* Enrichment Plots
* PPI Network
* Workflow Diagrams

---

# Reproducibility

This repository contains all documentation required to reproduce the complete computational workflow.

The only external component distributed separately is the original expression dataset, which is available through the GitHub Release page.

---

# Citation

If this repository contributes to your research, please cite

**Ghasemi A., Shahbazi M.R., Salimy S., Asgari A.M., Taheri O.**

**Stage-Specific Transcriptomic Biomarker Discovery in Skin Cancer Using Machine Learning and Statistical Approaches**

---

# License

This project is released under the terms of the LICENSE file included in this repository.

---

<p align="center">

Made for reproducible transcriptomic biomarker discovery using machine learning.

</p>
