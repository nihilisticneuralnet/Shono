# **Shono**: Bengali Speech Recognition

**Abstract**: This code implements a machine learning pipeline for predicting protein functions using the CAFA-5 (Critical Assessment of Function Annotation) dataset in [CAFA 5 Protein Function Prediction *(Kaggle Competition)*](https://www.kaggle.com/competitions/cafa-5-protein-function-prediction). The pipeline first processes protein sequence data that has been pre-embedded using ProtBERT model to convert proteins into numerical vectors. It then trains a Multi-Layer Perceptron to predict which Gene Ontology (GO) terms are associated with each protein, essentially predicting protein functions. The training process uses cross-entropy loss and monitors F1 score performance on both training and validation sets. Finally, it generates predictions for a test set and combines these predictions with other pre-existing predictions (from BlastP, Sprof, QuickGo, and DeepGoZero) through a merge operation, taking the best confidence scores available for each protein-GO term pair. This ensemble approach likely improves the overall prediction accuracy by leveraging multiple prediction methods.

## Description
### Goal of the Competition
The goal of this competition is to predict the function of a set of proteins. You will develop a model trained on the amino-acid sequences of the proteins and on other data. Your work will help ​​researchers better understand the function of proteins, which is important for discovering how cells, tissues, and organs work. This may also aid in the development of new drugs and therapies for various diseases.

### Plots

![Plot1](./images/output.png)

![Plot2](./images/output1.png)
