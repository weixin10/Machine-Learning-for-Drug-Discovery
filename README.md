# Machine-Learning-for-Drug-Discovery

##Overview
A Python script predicting IC50 values of compounds obtained from the ChEMBL database against the target protein, aromatase. The molecular descriptors used in this script is PubChem fingerprints.

##Introduction
The time taken for a drug to jump past all the hurdles from initial discovery to being marketed can be roughly a decade and the cost associated with research and subsequent clinical trials is in the order of a billion US dollars.¹(https://www.ncbi.nlm.nih.gov/pmc/articles/PMC3058157/) This is not the end of the list of challenges as only 12% of of drugs make it to market.². The aim of this project is to train a model that can predict IC50 values, which is a measure of drug potency based on PubChem fingerprints. PubChem fingerprints are a series of binary digits used to represent the chemical structure. For example, the first bit position indicates whether the compound has at least 4 hydrogen atoms.³ With a well trained model, we can then look at the important features for IC50 prediction to understand which structural features drive potency to aid optimisation of the chemical structure. This model would also be helpful for predicting IC50 values of libraries of compounds against the target protein, aromotase, which can be useful to narrow down compounds to test in the lab.

This project is inspired by a bioinformatics project done by Chanin Nantasenamat.⁴
