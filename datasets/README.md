\# Dataset Information



This project uses publicly available retinal fundus image datasets for glaucoma classification and severity estimation.



\## Datasets Used



\### 1. REFUGE2



REFUGE2 is used for the glaucoma classification experiments, including the EfficientNet-B3 classification branch and the ResNet50 baseline.



The dataset is not included in this repository.



Users should obtain the dataset from the appropriate official source and follow the dataset's terms of use.



\### 2. DRISHTI-GS



DRISHTI-GS is used for CDR-related experiments, including:



\- ResNet50 baseline

\- Hybrid ResNet50–ViT model

\- CDR regression

\- Glaucoma severity estimation



The dataset is not included in this repository.



Users should obtain the dataset from the appropriate official source and follow the dataset's terms of use.



\## Dataset Configuration



After obtaining the datasets, configure the dataset paths in the corresponding notebooks according to the local environment.



The repository does not contain:



\- Raw fundus images

\- Patient data

\- Dataset archives

\- Dataset copies

\- Private dataset credentials



\## Recommended Local Organization



A local setup may follow a structure such as:



```text

data/

├── REFUGE2/

└── DRISHTI-GS/



The exact directory structure may vary depending on the downloaded dataset and local environment.



Important Note



Dataset files are intentionally excluded from this GitHub repository due to dataset distribution, size, and usage considerations.

