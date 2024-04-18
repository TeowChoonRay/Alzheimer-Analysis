# Welcome to Alzheimer-Analysis Respository

## About

This is ACDA1 Team 4's Mini-Project for SC1015 (Introduction to Data Science and Artificial Intelligence) which focuses on the dataset from [MRI and Alzheimers](https://www.kaggle.com/datasets/jboysen/mri-and-alzheimers?resource=download) (CSV Data) and [OASIS Alzheimer's Detection](https://www.kaggle.com/datasets/ninadaithal/imagesoasis) (MRI Images). For detailed walkthrough, please view the source code in order from:

1. [Data Extraction and Cleaning](https://github.com/TeowChoonRay/Alzheimer-Analysis/blob/main/Data%20Extraction%20and%20Cleaning.ipynb)
2. [Exploratory Data Analysis](https://github.com/TeowChoonRay/Alzheimer-Analysis/blob/main/Exploratory%20Data%20Analysis.ipynb)
3. [Classification Tree](https://github.com/TeowChoonRay/Alzheimer-Analysis/blob/main/Classification%20Tree.ipynb)
5. [Convolution Neural Network](https://github.com/TeowChoonRay/Alzheimer-Analysis/blob/main/Convolution%20Neural%20Network%20(VGG19).ipynb)

*Note: As the Brain MRI JPG Images file size is too large, it is not upload on Github. it would be ideal for you to download the dataset from kaggle first before proceeding with VGG19 CNN Model.*
  
## Contributors

- @TeowChoonRay (Teow Choon Ray) - Convolution Neural Network (VGG19)
- @nicoleang18 (Nicole Ang Xuan Jie) - Classification Tree & Random Forest
- @its.chloechloe (Chloe Yeo (Yang Enxi)) - Exploratory Data Analysis

## Introduction & Problem Definition 

Alzheimer’s disease is a brain disorder that slowly destroys memory and thinking skills, and eventually, the ability to carry out the simplest tasks. In most people with Alzheimer’s, symptoms first appear later in life ( ). There is no cure for Alzheimer’s, but there are treatments that may change disease progression, and drug and non-drug options that may help treat symptoms ( ).

It is important to realise that the progression of Alzheimer's can be slowed if detected at early stage. Hence, the aim of the project is to **detect Alzheimer's disease at early stage using OASIS brain data set**. This project involves using implementing machine learning techniques and exploring different algorithms and methods to accurately detect the type of Alzheimer's through the given data. 

We aim to achieve this with two different types of data: **Text** and **Image**

In **Text**, we aim to determine a correlation between the different demographic data (predictor) with the `Clinical Dementia Rating (CDR)` (response). The demographic data includes Gender (`M/F`), `Age`, Educational Level (`Educ`) and Socio-Economic Status (`SES`).

In **Image**, we aim to create an image recognition model that can predict the type of dementia (`Non Demented`, `Very Mild Dementia`, `Mild Dementia` and `Moderate Dementia`) based on Brain MRI Images of 4 different brain slice image types.

## Models Used

1. Classification Tree
2. Random Forest
3. Neural Networks (Transfer Learning - VGG19)

## Conclusion


## What did we learn from this project?


## References
https://www.nia.nih.gov/health/alzheimers-and-dementia/alzheimers-disease-fact-sheet#:~:text=Alzheimer's%20disease%20is%20a%20brain,first%20appear%20later%20in%20life.
https://www.alz.org/alzheimers-dementia/treatments#:~:text=There's%20no%20cure%20for%20Alzheimer's,that%20may%20help%20treat%20symptoms.
