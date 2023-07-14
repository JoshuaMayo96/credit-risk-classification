# Module 12 Report Template

## Overview of the Analysis

Introduction:
Lending companies provide loans to borrowers, aiming for asset return or loan repayment. However, the risk of borrowers defaulting on loans, known as credit risk, can cause financial losses to lenders. In this analysis, I employ machine learning techniques to analyze a dataset from a peer-to-peer lending services company. The goal is to build a model that accurately predicts the creditworthiness of borrowers.

Methodology:
A dataset of historical lending activity was provided by the lending company to train the model. 

For this analysis, I eomplyed the Logistic Regression algorithm as it is widely employed in predicting target variables for classification problems. To begin the analysis, it was crucial to assess the balance/imbalance within the dataset. I did this by using the value_counts function. From there, I could gain an image of the number of high-risk loans to low-risk loans. 



## Results

Logistic Regression Model with Imbalanced Data:
    * Out of the 18,765 loan status's that are healthy (low-risk), the model predicted 18,663 as healthy correctly and 102 as healthy incorrectly.
    * Out of the 619 loan status's that are non-healthy (high-risk), the model predicted 563 as non-healthy correctly and 56 as non-healthy incorrectly.
    * The model correctly predicted healthy loans 100% of the time, and non-healthy loans at 85% of the time.
    * Accuracy: The model achieved an accuracy score of 95%.
    * Performance: The model exhibited higher recall (99%) for healthy loans (low-risk) but lower recall (91%) for non-healthy loans (high-risk).
    * Imbalanced Dataset: The dataset had a significant class imbalance, with healthy loans (75,036) greatly outnumbering non-healthy loans (2,500).
    * This model trained on imbalanced data is more prone to the following errors:
        * Misclassifying a healthy loan (low-risk) as a non-healthy loan (high-risk).
        * Misclassifying a non-healthy loan (high-risk) as a healthy loan (low-risk).


Logistic Regression Model with Balanced (Oversampled) Data:
    * Out of the 18,765 loan status's that are healthy (low-risk), the model predicted 18,649 as healthy correctly and 116 as healthy incorrectly.
    * Out of the 619 loan status's that are non-healthy (high-risk), the model predicted 615 as non-healthy correctly and 4 as non-healthy incorrectly.
    * The model correctly predicted healthy loans 100% of the time, and non-healthy loans at 84% of the time.
    * Accuracy: The model achieved an accuracy score of 99%, surpassing the model with imbalanced data.
    * Improved Performance: By oversampling the non-healthy loans, the model's recall for non-healthy loans increased to 99%.
    * Balanced Dataset: The oversampling technique created a balanced dataset (56,271 to 56,271), enhancing the model's ability to predict non-healthy loans accurately.
    * This model trained on balanced (oversampled) data is much less prone to the following errors:
        * Misclassifying a healthy loan (low-risk) as a non-healthy loan (high-risk).
        * Misclassifying a non-healthy loan (high-risk) as a healthy loan (low-risk).



## Summary

Based on the analysis, we recommend using the Logistic Regression model fitted with balanced (oversampled) data. This model exhibited higher accuracy and significantly improved recall for non-healthy loans, reducing the possibility of misclassifying high-risk loans as low-risk. By adopting this model, lending companies can minimize potential losses by identifying non-healthy loans more effectively.
