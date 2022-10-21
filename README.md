# Machine-Learning-for-Drug-Discovery

## Overview
A Python script predicting pIC50 values of compounds obtained from the ChEMBL database against the target protein, aromatase. The molecular descriptor used in this script is PubChem fingerprint.

## Introduction
The time taken for a drug to jump past all the hurdles from initial discovery to being marketed can be roughly a decade and the cost associated with research and subsequent clinical trials is in the order of a billion US dollars.[¹](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC3058157/) This is not the end of the list of challenges as only 12% of of drugs make it to market.[²](https://www.cbo.gov/publication/57126). The aim of this project is to train a model that can **predict IC50 values**, which is a measure of **drug potency** based on **PubChem fingerprints**. PubChem fingerprints are a series of binary digits used to represent the chemical structure. For example, the first bit position indicates whether the compound has at least 4 hydrogen atoms.[³](https://web.cse.ohio-state.edu/~zhang.10631/bak/drugreposition/list_fingerprints.pdf) With a well trained model, we can then look at the important features for IC50 prediction to understand which structural features drive potency to aid optimisation of the chemical structure. This model would also be helpful for predicting IC50 values of libraries of compounds against the target protein, aromotase, which can be useful to narrow down compounds to test in the lab.

This project is inspired by a bioinformatics project done by Chanin Nantasenamat.[⁴](https://github.com/dataprofessor/code/tree/master/python)

## Data Description
1. compound_data.csv - dataset obtained from ChEMBL query filtered for IC50 values and removed instances where standard values were missing and standard units were not in nM.
2. preprocessed_compound_data.csv - dataset with only three columns: canonical smiles, molecule ChEMBL id and the standard value. 
3. compounds_descriptors.csv - dataset with the same columns as preprocessed_compound_data.csv with additional four columns: Molecular Weight, LogP, number of hydrogen bond donors and number of hydrogen bond acceptors.
4. molecule.smi - smi file containing the canonical smiles and molecule ChEMBL ids needed for computing the PubChem fingerprints.
5. descriptors_output.csv -  file containing the PubChem fingerprints for each molecule.
6. train_and_test.csv -  file containing the PubChem fingerprints and the pIC50 values.
7. grid_ran_for.csv - Results of running GridSearchCV to find optimal parameters for Random Forest Model in DataFrame format.
8. grid_svm.csv - Results of running GridSearchCV to find optimal parameters for SVR Model in DataFrame format.

## Plots
All plots obtained from conducting exploratory data analysis can be found in the Plots folder. This folder also contains plots of predicted pIC50 against experimental pIC50 in linear regression plot format and residual plot format.
