# QSAR Model of Beta Amyloid A4 Protein for Alzheimer's Disease: Project Overview
* Created an introductory Computational Drug Discovery model which predicts the bioactivity level of a target Beta Amyloid A4 Protein based on drugs' molecular features.
* Collected bioactivity data from ChEMBL dataset using Chembl Python API.
* Engineered features from the Canonical smiles data for each compound to create Lipinski Detector values -- Molecular Weight, LogP, Number of H Donors, and Number of H Acceptors -- and fingerprint descriptors for each compound
* Created Random Forest, Decision Tree, and Lasso Regressors to predict the pIC50 value of Beta Amyloid A4 Protein with fingerprint descriptors as features. 


# Code and Resources Used
**Python Version:** 3.7

**Packages:** pandas, numpy, sklearn, seaborn, ChEMBL web resource client, rdkit, padel. 

**Project Guidance and Code Inspiration**: [Data Professor YouTube Channel](https://www.youtube.com/channel/UCV8e2g4IWQqK71bbzGDEI4Q)


# Data Collection
Collected bioactivity for the Beta Amyloid A4 Protein from ChEMBL Database using ChEMBL web resource client. 43 features were available for each compound, including: 
* Canonical Smiles
* Standard Value
* Document Year
* Molecule ChEMBL ID
* Activity ID


# Data Cleaning and Preprocessing
With such a large and raw database provided by ChEMBL, data cleaning was necessary before moving on. Some of the steps taken to clean the data include: 
* Remove entries that don't have standard values or canonical smiles and 
* Drop entries with standard value not reported as IC50. 
* Drop duplicate canonical smiles 
* Label compounds as either active, inactive, or intermediate based on their standard value (IC50 values). 
* Keep only each compounds' ChEMBL ID, canonical smiles, IC50 value, and activity classification data for further use. 
* Removed 'Intermediate' activity compounds. 


# Feature Engineering
* Calculated Lipinski Detectors from Canonical Smiles data. 
* Took -log of IC50 values and created and stored resulting pIC50 values. 

# EDA
I wanted to analyze the distributions of each of the Lipinski Descriptors to assess if they are statistically significant. The plots, along with formal statistical calculations in the code, showed that all four features were indeed statistically significant. 
![alt text](https://github.com/aditjain125/Comp-Drug-Discovery-Proj/blob/main/PNG%20Images/plot_LogP-1.png)
![alt text](https://github.com/aditjain125/Comp-Drug-Discovery-Proj/blob/main/PNG%20Images/plot_MW-1.png)
![alt text](https://github.com/aditjain125/Comp-Drug-Discovery-Proj/blob/main/PNG%20Images/plot_NumHAcceptors-1.png)
![alt text](https://github.com/aditjain125/Comp-Drug-Discovery-Proj/blob/main/PNG%20Images/plot_NumHDonors-1.png)
