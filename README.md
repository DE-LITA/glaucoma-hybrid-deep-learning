\# A Hybrid Deep Learning Framework for Automated Glaucoma Detection and Severity Estimation Using Fundus Images with Explainable Artificial Intelligence



\## Overview



This repository contains the implementation associated with the research work:



\*\*A Hybrid Deep Learning Framework for Automated Glaucoma Detection and Severity Estimation Using Fundus Images with Explainable Artificial Intelligence\*\*



The project focuses on automated glaucoma detection and severity estimation from retinal fundus images using deep learning and Explainable Artificial Intelligence (XAI).



The framework consists of two major components:



1\. \*\*Glaucoma Classification\*\*

&#x20;  - EfficientNet-B3

&#x20;  - REFUGE2 dataset

&#x20;  - Focal Loss

&#x20;  - Clinical validation and calibration

&#x20;  - Grad-CAM based explainability



2\. \*\*Glaucoma Severity Estimation\*\*

&#x20;  - Hybrid ResNet50–Vision Transformer (ViT)

&#x20;  - Cup-to-Disc Ratio (CDR) regression

&#x20;  - DRISHTI-GS dataset

&#x20;  - CDR-based severity estimation

&#x20;  - Vision Transformer attention rollout



\---



\## Research Objectives



The main objectives of this research are:



\- To develop an automated deep learning framework for glaucoma detection from retinal fundus images.

\- To investigate EfficientNet-B3 for glaucoma classification.

\- To develop a hybrid ResNet50–Vision Transformer architecture for CDR regression.

\- To estimate glaucoma severity using CDR-based measurements.

\- To evaluate the proposed models using appropriate classification, regression, and clinical evaluation metrics.

\- To incorporate Explainable Artificial Intelligence techniques to improve model interpretability.



\---



\## Proposed Framework



\### 1. Glaucoma Classification



The classification branch uses \*\*EfficientNet-B3\*\* for automated glaucoma detection using the REFUGE2 dataset.



The workflow is:



```text

Fundus Images

&#x20;     |

&#x20;     v

Image Preprocessing

&#x20;     |

&#x20;     v

EfficientNet-B3

&#x20;     |

&#x20;     v

Glaucoma Classification

&#x20;     |

&#x20;     v

Clinical Validation \& Calibration

&#x20;     |

&#x20;     v

Grad-CAM Explainability

2\. Glaucoma Severity Estimation



The severity estimation branch uses a hybrid ResNet50–Vision Transformer (ViT) architecture for CDR regression and glaucoma severity estimation using the DRISHTI-GS dataset.



The workflow is:



Fundus Images

&#x20;     |

&#x20;     +-------------------+

&#x20;     |                   |

&#x20;     v                   v

&#x20;  ResNet50              ViT

&#x20;     |                   |

&#x20;     +---------+---------+

&#x20;               |

&#x20;               v

&#x20;         Feature Fusion

&#x20;               |

&#x20;               v

&#x20;         CDR Regression

&#x20;               |

&#x20;               v

&#x20;      Severity Estimation

&#x20;               |

&#x20;               v

&#x20;        Attention Rollout

Repository Structure

glaucoma-hybrid-deep-learning/

|

|-- README.md

|

`-- notebooks/

&#x20;   |-- 01\_ResNet50\_Baseline\_DrishtiGS.ipynb

&#x20;   |-- 02\_Hybrid\_ResNet50\_ViT.ipynb

&#x20;   |-- 03\_CDR\_GroundTruth\_Preparation.ipynb

&#x20;   |-- 04\_Hybrid\_CDR\_Regression.ipynb

&#x20;   |-- 05\_CDR\_Severity\_Estimation.ipynb

&#x20;   |-- 06\_ResNet50\_REFUGE2\_Baseline.ipynb

&#x20;   |-- 07\_EfficientNetB3\_Glaucoma\_Classification.ipynb

&#x20;   |-- 08\_Clinical\_Validation\_Calibration.ipynb

&#x20;   |-- 09\_ViT\_Attention\_Rollout.ipynb

&#x20;   |-- 10\_EfficientNetB3\_GradCAM\_Captum.ipynb

&#x20;   `-- 11\_Final\_Results\_Reproduction.ipynb

Notebook Description

No.	Notebook	Description

01	01\_ResNet50\_Baseline\_DrishtiGS.ipynb	ResNet50 baseline experiment on DRISHTI-GS

02	02\_Hybrid\_ResNet50\_ViT.ipynb	Hybrid ResNet50–ViT architecture

03	03\_CDR\_GroundTruth\_Preparation.ipynb	CDR ground-truth preparation

04	04\_Hybrid\_CDR\_Regression.ipynb	Hybrid model-based CDR regression

05	05\_CDR\_Severity\_Estimation.ipynb	CDR-based glaucoma severity estimation

06	06\_ResNet50\_REFUGE2\_Baseline.ipynb	ResNet50 baseline experiment on REFUGE2

07	07\_EfficientNetB3\_Glaucoma\_Classification.ipynb	EfficientNet-B3 glaucoma classification

08	08\_Clinical\_Validation\_Calibration.ipynb	Clinical validation and calibration

09	09\_ViT\_Attention\_Rollout.ipynb	Vision Transformer attention rollout

10	10\_EfficientNetB3\_GradCAM\_Captum.ipynb	Grad-CAM based explainability using Captum

11	11\_Final\_Results\_Reproduction.ipynb	Consolidation and reproduction of experimental results

Datasets



The experiments use retinal fundus image datasets including:



REFUGE2

DRISHTI-GS



The datasets are not included in this repository.



Users should obtain the datasets from their respective official sources and configure the dataset paths according to their local environment before running the notebooks.



Explainable Artificial Intelligence



The repository includes two explainability approaches.



Grad-CAM



Grad-CAM is applied to the EfficientNet-B3 classification branch to visualize image regions contributing to the model's glaucoma prediction.



Vision Transformer Attention Rollout



Attention rollout is applied to the Vision Transformer component of the hybrid severity estimation branch to visualize attention propagation across image patches.



Evaluation

Classification Evaluation



The glaucoma classification branch is evaluated using metrics including:



ROC-AUC

Sensitivity

Specificity

Precision-Recall AUC

Brier Score

Confusion Matrix

Bootstrap Confidence Intervals

CDR Regression Evaluation



The CDR regression branch is evaluated using:



Mean Absolute Error (MAE)

Root Mean Square Error (RMSE)

R²

Pearson Correlation

Confidence Intervals

Severity Evaluation



The severity estimation component is evaluated using CDR-based severity categories and within-one-category accuracy.



Reproducibility



The notebooks are organized according to the experimental workflow used in the research project.



Before running the notebooks:



Obtain the required datasets.

Configure the dataset paths according to the local environment.

Install the required Python dependencies.

Run the notebooks according to their numbering.

Review the generated evaluation metrics and visualizations.



The notebooks contain the corresponding preprocessing, model development, training/evaluation, validation, regression, severity estimation, and explainability procedures.



Important Notes

The datasets are not distributed with this repository.

Dataset paths may need to be modified according to the local environment.

Model checkpoints are not included in this repository.

GPU execution is recommended for deep learning model training.

The repository is intended to accompany the associated research manuscript.

Experimental results should be interpreted together with the corresponding research manuscript.

This repository is intended primarily for academic and research purposes.

Authors



Delita Tauro

M.Tech, Computer Science and Engineering

Manipal Institute of Technology, MAHE



Dr. P C Siddalingaswamy



Mr. Mayur Pandya



Research Manuscript



This repository accompanies the research manuscript:



A Hybrid Deep Learning Framework for Automated Glaucoma Detection and Severity Estimation Using Fundus Images with Explainable Artificial Intelligence



License



This repository is intended for academic and research purposes.



Please refer to the repository license for permitted use, modification, and distribution.

