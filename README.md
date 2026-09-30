# A Hybrid Deep Learning Framework for Automated Glaucoma Detection and Severity Estimation Using Fundus Images with Explainable Artificial Intelligence

## Overview

This repository contains the implementation associated with the research work:

**A Hybrid Deep Learning Framework for Automated Glaucoma Detection and Severity Estimation Using Fundus Images with Explainable Artificial Intelligence**

The project investigates automated glaucoma detection and severity estimation from retinal fundus images using deep learning and Explainable Artificial Intelligence (XAI).

The framework consists of two major components:

1. **Glaucoma Classification**
   - EfficientNet-B3
   - REFUGE2 dataset
   - Focal Loss
   - Clinical validation and calibration
   - Grad-CAM explainability

2. **Glaucoma Severity Estimation**
   - Hybrid ResNet50 + Vision Transformer (ViT)
   - Cup-to-Disc Ratio (CDR) regression
   - DRISHTI-GS dataset
   - CDR-based severity estimation
   - Vision Transformer attention rollout

---

## Research Objectives

The main objectives of this research are:

- To develop an automated deep learning framework for glaucoma detection from retinal fundus images.
- To investigate EfficientNet-B3 for glaucoma classification.
- To develop a hybrid ResNet50 + Vision Transformer architecture for CDR regression.
- To estimate glaucoma severity using CDR-based measurements.
- To evaluate the proposed models using classification, regression, and clinical evaluation metrics.
- To incorporate Explainable Artificial Intelligence techniques to improve model interpretability.

---

## Proposed Framework

### 1. Glaucoma Classification

The classification branch uses **EfficientNet-B3** for automated glaucoma detection using the REFUGE2 dataset.

The workflow is:

```text
Fundus Images
      |
      v
Image Preprocessing
      |
      v
EfficientNet-B3
      |
      v
Glaucoma Classification
      |
      v
Clinical Validation and Calibration
      |
      v
Grad-CAM Explainability


###2. **Glaucoma Severity Estimation**

The severity estimation branch uses a hybrid ResNet50 + Vision Transformer (ViT) architecture for CDR regression and glaucoma severity estimation using the DRISHTI-GS dataset.

The workflow is:

Fundus Images
      |
      +-------------------+
      |                   |
      v                   v
   ResNet50              ViT
      |                   |
      +---------+---------+
                |
                v
         Feature Fusion
                |
                v
          CDR Regression
                |
                v
       Severity Estimation
                |
                v
        Attention Rollout
```

## Repository Structure

```text
glaucoma-hybrid-deep-learning/
|
|-- datasets/
|   `-- README.md
|
|-- manuscript/
|   `-- Manuscript.pdf
|
|-- notebooks/
|   |-- 01_ResNet50_Baseline_DrishtiGS.ipynb
|   |-- 02_Hybrid_ResNet50_ViT.ipynb
|   |-- 03_CDR_GroundTruth_Preparation.ipynb
|   |-- 04_Hybrid_CDR_Regression.ipynb
|   |-- 05_CDR_Severity_Estimation.ipynb
|   |-- 06_ResNet50_REFUGE2_Baseline.ipynb
|   |-- 07_EfficientNetB3_Glaucoma_Classification.ipynb
|   |-- 08_Clinical_Validation_Calibration.ipynb
|   |-- 09_ViT_Attention_Rollout.ipynb
|   |-- 10_EfficientNetB3_GradCAM_Captum.ipynb
|   `-- 11_Final_Results_Reproduction.ipynb
|
|-- results/
|   `-- README.md
|
|-- README.md
`-- requirements.txt
```

## Notebook Description

| No.| Notebook                                                 | Description |
|--- |---                                                       |---|
| 01 | `01_ResNet50_Baseline_DrishtiGS.ipynb` 			| ResNet50 baseline experiment on DRISHTI-GS |
| 02 | `02_Hybrid_ResNet50_ViT.ipynb`				| Hybrid ResNet50 + ViT architecture |
| 03 | `03_CDR_GroundTruth_Preparation.ipynb`   		| CDR ground-truth preparation |
| 04 | `04_Hybrid_CDR_Regression.ipynb`         		| Hybrid model-based CDR regression |
| 05 | `05_CDR_Severity_Estimation.ipynb`       		| CDR-based glaucoma severity estimation |
| 06 | `06_ResNet50_REFUGE2_Baseline.ipynb`     		| ResNet50 baseline experiment on REFUGE2 |
| 07 | `07_EfficientNetB3_Glaucoma_Classification.ipynb` 	| EfficientNet-B3 glaucoma classification |
| 08 | `08_Clinical_Validation_Calibration.ipynb` 		| Clinical validation and calibration |
| 09 | `09_ViT_Attention_Rollout.ipynb` 			| Vision Transformer attention rollout |
| 10 | `10_EfficientNetB3_GradCAM_Captum.ipynb` 		| Grad-CAM explainability using Captum |
| 11 | `11_Final_Results_Reproduction.ipynb` 			| Consolidation and reproduction of experimental results |

## Datasets
##Datasets

This project uses two publicly available retinal fundus image datasets.

###REFUGE2

REFUGE2 is used for the glaucoma classification experiments.

The official dataset and challenge information is documented in:

datasets/README.md

Official challenge page:

https://refuge.grand-challenge.org/Home2020/

###DRISHTI-GS

DRISHTI-GS is used for CDR-related experiments, including CDR regression and glaucoma severity estimation.

The official dataset information is documented in:

datasets/README.md

Official dataset information:

https://cvit.iiit.ac.in/mip/datasets.html

###Dataset Availability

The datasets are not included in this repository.

Users should obtain the datasets from their respective official sources and follow the applicable terms of use.

The repository does not contain:

- Raw fundus images
- Patient data
- Dataset archives
- Dataset copies
- Private dataset credentials

##Explainable Artificial Intelligence

The repository includes two explainability approaches.

###Grad-CAM

Grad-CAM is applied to the EfficientNet-B3 classification branch to visualize image regions contributing to the model's glaucoma prediction.

###Vision Transformer Attention Rollout

Attention rollout is applied to the Vision Transformer component of the hybrid severity estimation branch to visualize attention propagation across image patches.

## Evaluation

### Classification Evaluation

The glaucoma classification branch is evaluated using metrics including:

- ROC-AUC
- Sensitivity
- Specificity
- Precision-Recall AUC
- Brier Score
- Confusion Matrix
- Bootstrap Confidence Intervals

### CDR Regression Evaluation

The CDR regression branch is evaluated using:

- Mean Absolute Error (MAE)
- Root Mean Square Error (RMSE)
- R²
- Pearson Correlation
- Confidence Intervals

### Severity Evaluation

The severity estimation component is evaluated using CDR-based severity categories and within-one-category accuracy.

## Reproducibility

The notebooks are organized according to the experimental workflow used in the research project.

Before running the notebooks:

1. Obtain the required datasets from their official sources.
2. Configure the dataset paths according to the local environment.
3. Install the required Python dependencies.
4. Run the notebooks according to their numbering.
5. Review the generated evaluation metrics and visualizations.

The notebooks contain the corresponding preprocessing, model development, training, evaluation, validation, regression, severity estimation, and explainability procedures.

## Requirements

The required Python packages are listed in:

`requirements.txt`

Install the dependencies using:

```bash
pip install -r requirements.txt
```

GPU execution is recommended for deep learning model training.

##Important Notes

- The datasets are not distributed with this repository.
- Dataset paths may need to be modified according to the local environment.
- Model checkpoints are not included in this repository.
- The repository does not contain private dataset credentials or patient data.
- Experimental results should be interpreted together with the corresponding research manuscript.
- This repository is intended primarily for academic and research purposes.

## Research Manuscript

This repository accompanies the research manuscript:

**A Hybrid Deep Learning Framework for Automated Glaucoma Detection and Severity Estimation Using Fundus Images with Explainable Artificial Intelligence**

The manuscript is available in:

`manuscript/Manuscript.pdf`

## Authors

**Delita Tauro**  
M.Tech, Computer Science and Engineering  
Manipal Institute of Technology, MAHE

**Dr. P C Siddalingaswamy**

**Mr. Mayur Pandya**

## License

This repository is intended for academic and research purposes.

No separate open-source license is currently specified for this repository. Please contact the authors regarding permissions for reuse, modification, or redistribution of the research materials.