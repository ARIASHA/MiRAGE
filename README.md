# MiRAGE

MiRAGE: Mining Relationships for Advanced Generative Evaluation in Drug Repositioning

This is the official code base for MiRAGE, a novel computational method for drug repositioning.
Drug repositioning, the identification of new therapeutic uses for existing drugs, is crucial for accelerating drug
discovery and reducing development costs. Some methods rely on heterogeneous networks, which may not fully capture
the complex relationships between drugs and diseases. However, integrating diverse biological data sources offers promise
for discovering new drug-disease associations (DDAs). Previous evidence indicates that the combination of information
would be conducive to the discovery of new DDAs. However, the challenge lies in effectively integrating different biological
data sources to identify the most effective drugs for a certain disease based on drug-disease coupled mechanisms.
Results: In response to this challenge, we present MiRAGE, a novel computational method for drug repositioning.
MiRAGE leverages a three-step framework, comprising negative sampling using hard negative mining, classification
employing random forest models, and feature selection based on feature importance. We evaluate MiRAGE on multiple
benchmark datasets, demonstrating its superiority over state-of-the-art algorithms across various metrics. Notably,
MiRAGE consistently outperforms other methods in uncovering novel drug-disease associations. Case studies focusing on
Parkinson’s disease and schizophrenia showcase MiRAGE’s ability to identify top candidate drugs supported by previous
studies. Overall, our study underscores MiRAGE’s efficacy and versatility as a computational tool for drug repositioning,
offering valuable insights for therapeutic discoveries and addressing unmet medical needs.

This repository is made of two main parts:

## Datasets

This section contains four datasets, including three well-known benchmark datasets: F, B, and C-Dataset. Additionally, a larger and more diverse dataset named DDC-Dataset is introduced, offering extensive features for both drugs and diseases. Each dataset folder comprises four subfolders:

- Evaluation: Contains training and test datasets for the respective dataset.

- Features: Provides drug features in all datasets, as well as disease features for the DDC-Dataset.

- Similarity Matrices: Contains similarity matrices derived from different features. For the benchmark datasets, the disease similarity is extracted from the dataset provided by [AMDGT](https://github.com/JK-Liu7/AMDGT/tree/main).

- Mapping: Includes the main drug-disease mapping and an 80-20 split of the train and test datasets.

## Codes

This section is divided into two parts:

1. Evaluation: All the code used to produce the results and figures in the paper is stored in the code folder. The calculations and visualizations are executed within Jupyter notebooks.
#### (Note: All the datasets are zip files and have to be extracted and put in the correct path for execution.)

2. MiRAGE Score Calculation: The main component of this section focuses on calculating the MiRAGE score. This is provided in a separate Python notebook and relies on single drug-drug similarity, disease-disease similarity, and drug-disease mapping data from the training dataset. The dataset folder contains a sample that demonstrates the needed data for running the mirage function. Now this can be adapted to different mappings and numbers of features.

