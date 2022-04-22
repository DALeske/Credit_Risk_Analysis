# Module 17 Challenge: Credit Risk Analysis

## Overview
The purpose of this analysis is to predict high credit card risk using machine learning. The features (factors going into the predictive model) include various information on the amount and type of credit, credit limit, home ownership, annual income, current and past debt, utility payments, previous bankruptcy, and other financial hardships. The goal of the analysis is to use machine learning algorithms to identify applicants with high risk for default on their credit card payments.

The following machine learning models were used to predict high credit card risk.

1. Naive random over-sampling 
2. SMOTE over-sampling
3. Cluster centroids under-sampling
4. SMOTEENN combination (over and under) sampling: 
5. Balanced Random Forest Classifier ensemble sampling
6. Easy Ensemble AdaBoost Classifier

The same dataset was used for all analyses. Data was cleaned and transformed into numerical constructs prior to analysis.

## Results

The following are a summary of the balanced accuracy scores, precision, and sensitivity (recall) for the six difference machine learning models:

1. Naive:               Accuracy = 0.66   Precision = 0.01   Sensitivity = 0.67  Specificity = 0.65
2. SMOTE:               Accuracy = 0.65   Precision = 0.01   Sensitivity = 0.61  Specificity = 0.68
3. Cluster centroids:   Accuracy = 0.55   Precision = 0.01   Sensitivity = 0.69  Specificity = 0.42
4. SMOTEENN:            Accuracy = 0.63   Precision = 0.01   Sensitivity = 0.68  Specificity = 0.57
5. Random Forest:       Accuracy = 0.76   Precision = 0.03   Sensitivity = 0.64  Specificity = 0.88
6. AdaBoost:            Accuracy = 0.69   Precision = 0.88   Sensitivity = 0.38  Specificity = 1.00

| METHOD | ACCURACY | PRECISION | SENSITIVITY | SPECIFICITY |
| :---: | :---: | :---: | :---: | :---: |
| Naive | 0.66 | 0.01 | 0.67 | 0.65 |
| SMOTE | 0.65 | 0.01 | 0.61 | 0.68 |
| Cluster centroids | 0.55 | 0.01 | 0.69 | 0.42 |
| SMOTEENN | 0.63 | 0.01 | 0.68 | 0.57 |
| Random forest | 0.76 | 0.03 | 0.64 | 0.88 |
| AdaBoost | 0.69 | 0.88 | 0.38 | 1.00 |

## Summary
Among all of the methods, the accuracy was reasonable for all models except for cluster centroids, the only pure under-sampling model. Precision was poor for all models with the exception of the AdaBoost model. All models had moderate sensitivity (recall) with the exception of the AdaBoost model, which had relatively poor sensitivity. 

There is no single model that will perfectly predict whether an applicant is truly high risk and will default on credit card payments. Of all six of the models, two models that stand out are the two ensemble models, random forest and AdaBoost. Random forest has slightly better accuracy, but has poor accuracy, meaning that many of the applicants identified as high risk may actually not be. In contrast the AdaBoost model has a high degree of precision, meaning that most applicants identified as high risk truly are likely to be high risk. That makes for a happy customer (they get approved), but at a cost to the company because of failing to identify some of the high risk applicants, reflected in the low sensitivity of the AdaBoost. 

## Recommendation
Ultimately, the decision comes down to management's needs. If the company wants lower risk, I would recommend the Random forest model, which identifies more of the high risk applicants while turning away some good customers. If the company is willing to take on more risk to keep their applicant pool happy, then I would recommend using the AdaBoost model. 


