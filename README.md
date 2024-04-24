# Welcome to Alzheimers-Analysis Respository

## About

This is ACDA1 Team 4's Mini-Project for SC1015 (Introduction to Data Science and Artificial Intelligence) which focuses on the dataset from [MRI and Alzheimers](https://www.kaggle.com/datasets/jboysen/mri-and-alzheimers?resource=download) (CSV Data) and [OASIS Alzheimer's Detection](https://www.kaggle.com/datasets/ninadaithal/imagesoasis) (MRI Images). For detailed walkthrough, please view the source code in order from:

1. [Data Extraction and Cleaning](https://github.com/TeowChoonRay/Alzheimer-Analysis/blob/main/Data%20Extraction%20and%20Cleaning.ipynb)
2. [Exploratory Data Analysis](https://github.com/TeowChoonRay/Alzheimer-Analysis/blob/main/Exploratory%20Data%20Analysis.ipynb)
3. [Regression](https://github.com/TeowChoonRay/Alzheimer-Analysis/blob/main/Regression.ipynb)
4. [Classification Tree](https://github.com/TeowChoonRay/Alzheimer-Analysis/blob/main/Classification%20Tree.ipynb)
5. [Convolution Neural Network](https://github.com/TeowChoonRay/Alzheimer-Analysis/blob/main/Convolution%20Neural%20Network%20(VGG19).ipynb)

*Note: As the Brain MRI JPG Images file size is too large, it is not uploaded on Github. it would be ideal for you to download the dataset from kaggle first before proceeding with VGG19 CNN Model. Do note that the trained model is not uploaded on Github as well due to its file size.*
  
## Contributors

- @TeowChoonRay (Teow Choon Ray) - Regression, Convolution Neural Network (VGG19)
- @nicoleang18 (Nicole Ang Xuan Jie) - Classification Tree & Random Forest
- @its.chloechloe (Chloe Yeo (Yang Enxi)) - Exploratory Data Analysis

## Introduction & Problem Definition 

Alzheimer’s disease is a brain disorder that slowly destroys memory and thinking skills, and eventually, the ability to carry out the simplest tasks. In most people with Alzheimer’s, symptoms first appear later in life (Alzheimer's Association, 2021). There is no cure for Alzheimer’s, but there are treatments that may change disease progression, and drug and non-drug options that may help treat symptoms (National Institute of Aging, 2023).

It is important to realise that the progression of Alzheimer's can be slowed if detected at early stage. Hence, the aim of the project is to **develop algorithms and models capable of detecting Alzheimer’s disease at an early stage using the OASIS brain dataset**. By leveraging advanced data analysis techniques, the goal is to accurately identify patterns and biomarkers associated with Alzheimer’s pathology, enabling timely intervention and treatment.

We aim to achieve this with two different types of data: **Text** and **Image**

In **Text**, we aim to determine a correlation between the different demographic and medical data (predictor) with the `Clinical Dementia Rating (CDR)` (response). The demographic data includes Gender (`M/F`), `Age`, Educational Level (`Educ`) and Socio-Economic Status (`SES`). Whereas, the medical data include Mini-Mental State Examination (`MMSE`), Estimated Total Intracranial Volume (`eTIV`), Normalised Whole-Brain Volume (`nWBV`) and Atlas Scaling Factor (`ASF`).

In **Image**, we aim to create an image recognition model that can predict the type of dementia (`Non Demented`, `Very Mild Dementia`, `Mild Dementia` and `Moderate Dementia`) based on Brain MRI Images (were sliced along the z-axis into 256 pieces, and slices ranging from 100 to 160 were selected from each patient).

## Models Used

1. Linear Regression
2. Ordinal Logistic Regression
3. Classification Tree
4. Random Forest
5. Neural Networks (Transfer Learning - VGG19)

## Conclusion
Fundamentally, it is important to note that Alzheimer’s is a complex disease. Alzheimers ​​involves the accumulation of abnormal proteins which causes progressive damage and this relationship to cognitive decline is still not fully understood. Furthermore, Alzheimers is believed to arise from a combination of genetic, environmental, and lifestyle factors which is severely complicated to untangle with our chosen dataset.

Nonetheless, it is clearly evident that some variables have a more clearcut relationship with the onset and type of Alzheimers, including `MMSE` and `Age`. It is important for one to focus on these factors in determining and predicting the onset of Alzheimers so that treatment can be sought earlier, especially if the disease has already been developed.

## What did we learn from this project?

1. Ordinal Logistic Regression - type of regression analysis used when the dependent variable (response variable) is ordinal (values of the variable represent categories)
2. GridSearch - used to finetune hyperparameters to distinguish optimal values found through the randomizedsearch function. 
3. Validation Dataset - used to give an unbiased estimate of the skill of the final tuned model when comparing or selecting between final models
4. Transfer Learning (CNN) -  take a model trained on a large dataset and transfer its knowledge to a smaller dataset

## Future Possibilities
- Classification Tree & GridSearch: Enhancing Alzheimer's predictive modelling using Clinical Dementia Rating (CDR) data, we can leverage advanced machine learning models like XGBoost, LightGBM, or AdaBoost with SAMME.R, tuned to address class imbalances and complex data structures. Additionally, we can incorporate advanced feature engineering, such as interaction terms and polynomial features to capture intricate dependencies in disease progression. Moreover, we can also enhance the interpretability of the model through tools like SHAP (Shapley Additive exPlanations) which would provide crucial insights into decision making processes, enhancing clinical acceptance. These strategies will maximize the predictive power of models focused on Alzheimer’s progression using CDR data.

- CNN: Currently, the model is trained without considering class imbalance, which may lead to a biased model. Furthermore, images were split for training, validation and testing randomly without considering subject identity, which may may impact the model's generalisation performance due to data leakage. Since only 1417 images were used for training, we hence can explore the possibility of training the model using a larger image dataset, selected equally across each class of Alzheimer's and taking subject identity into account. This should be possible given that over 80,000 images are available in the dataset. We may even consider creating our own custom model which is more suited for MRI greyscale images.

## References
Alzheimer's Association. (2021). Tratamientos. Alzheimer’s Disease and Dementia. https://www.alz.org/alzheimers-dementia/treatments#:~:text=There

National Institute on Aging. (2023, April 5). Alzheimer’s Disease Fact Sheet. National Institute on Aging. https://www.nia.nih.gov/health/alzheimers-and-dementia/alzheimers-disease-fact-sheet#:~:text=Alzheimer
