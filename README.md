# QSAR Model of Beta Amyloid A4 Protein for Alzheimer's Disease: Project Overview
* Created an introductory Computational Drug Discovery model which predicts the bioactivity level of a target Beta Amyloid A4 Protein based on drugs' molecular features.
* Collected bioactivity data from Chembl dataset using Chembl Python API.
* Engineered features from the Canonical smiles data for each compound to create Lipinski Detector values -- Molecular Weight, LogP, Number of H Donors, and Number of H Acceptors -- and fingerprint descriptors for each compound
* Created Random Forest, Decision Tree, and Lasso Regressors to predict the pIC50 value of Beta Amyloid A4 Protein with fingerprint descriptors as features. 


# Code and Resources Used
**Python Version:** 3.7
**Packages:** pandas, numpy, sklearn, seaborn, chembl web resource client, rdkit, padel. 
**Project Guidance and Code Inspiration**: [Data Professor YouTube Channel](https://www.youtube.com/channel/UCV8e2g4IWQqK71bbzGDEI4Q)
