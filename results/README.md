# Experimental Results



This directory contains documentation related to the experimental results reported in the associated research work.



## Classification Results



The glaucoma classification experiments use EfficientNet-B3 on the REFUGE2 dataset.



The final clinical validation and calibration experiment includes:



- ROC-AUC

- Sensitivity

- Specificity

- Precision-Recall AUC

- Brier Score

- Bootstrap confidence interval

- Confusion matrix

- Grad-CAM visualizations



The final manuscript-linked classification results are documented in the corresponding clinical validation notebook.



## CDR Regression Results



The glaucoma severity estimation experiments use the hybrid ResNet50-ViT architecture for CDR regression on the DRISHTI-GS dataset.



The reported regression evaluation includes:



- Mean Absolute Error (MAE)

- Root Mean Square Error (RMSE)

- R-squared (R2)

- Pearson correlation

- Confidence interval



## Severity Estimation



CDR values are used to estimate glaucoma severity categories.



The severity analysis also reports within-one-category accuracy.



## Explainability Results



The repository includes explainability experiments using:



- Grad-CAM for EfficientNet-B3

- Vision Transformer attention rollout



These methods provide visual explanations of regions and patches contributing to model predictions.



## Reproducibility



The corresponding notebooks contain the experimental procedures and evaluation code used to generate the reported results.



Results should be interpreted together with the associated research manuscript.



## Important Note



This directory contains result documentation only.



Raw datasets, patient information, private files, and model checkpoints are not included in this repository.

