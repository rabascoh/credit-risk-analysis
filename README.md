# Credit Risk Analysis

## Overview of Credit Risk Analysis
The purpose of this analysis is to predict credit card risk using machine learning. We evaluate several machine learning models to determine the model that best predicts credit card risk. This analysis is based on credit card credit data from LendingClub, a peer-to-peer lending services company. 

## Results

### RandomOverSampler
* **Balanced Accuracy Score:** 0.64
* **Precision:** 
    * High risk: 0.01
    * Low risk: 1.00
* **Recall:** 
    * High risk: 0.61
    * Low risk: 0.68

![ROS](https://github.com/rabascoh/credit-risk-analysis/blob/main/Resources/Resampling/naive_random_oversampling.png)


### SMOTE
* **Balanced Accuracy Score:** 0.62
* **Precision:** 
    * High risk: 0.01
    * Low risk: 1.00
* **Recall:** 
    * High risk: 0.60
    * Low risk: 0.64

![SMOTE](https://github.com/rabascoh/credit-risk-analysis/blob/main/Resources/Resampling/SMOTE_oversampling.png)


### ClusterCentroids
* **Balanced Accuracy Score:** 0.62
* **Precision:** 
    * High risk: 0.01
    * Low risk: 1.00
* **Recall:** 
    * High risk: 0.59
    * Low risk: 0.43

![CC](https://github.com/rabascoh/credit-risk-analysis/blob/main/Resources/Resampling/cluster_centroids_undersampling.png)


### SMOTEENN
* **Balanced Accuracy Score:** 0.51
* **Precision:** 
    * High risk: 0.01
    * Low risk: 1.00
* **Recall:** 
    * High risk: 0.70
    * Low risk: 0.57

![SMOTEENN](https://github.com/rabascoh/credit-risk-analysis/blob/main/Resources/Resampling/SMOTEENN.png)


### BalancedRandomForestClassifier
* **Balanced Accuracy Score:** 0.67
* **Precision:** 
    * High risk: 0.73
    * Low risk: 1.00
* **Recall:** 
    * High risk: 0.34
    * Low risk: 1.00

![RF](https://github.com/rabascoh/credit-risk-analysis/blob/main/Resources/Ensemble/random_forest.png)


### EasyEnsembleClassifier
* **Balanced Accuracy Score:** 0.93
* **Precision:** 
    * High risk: 0.07
    * Low risk: 1.00
* **Recall:** 
    * High risk: 0.91
    * Low risk: 0.94

![EE](https://github.com/rabascoh/credit-risk-analysis/blob/main/Resources/Ensemble/easy_ensemble.png)


## Summary
The Balanced Random Forest Classifier and Easy Ensemble Classifier both outperform the over- and under-sampling algorithms with accuracy scores of 0.67 and 0.93 respectively. 

However, we do not recommend using any of the models to predict credit card risk. 

The Balanced Random Forest Classifier still has fairly low accuracy at 0.67 and the recall for high risk is only 0.34. Given that falsely categorizing high risk credit would result in negative outcomes for credit card companies and individuals, we recommend against using this model to predict credit card risk. 

Although the Easy Ensemble Classifier has the highest accuracy score (0.93) and recall across high (0.91) and low (0.94) risk, the precision for high risk is only 0.07. This indicates that the reliability of the high risk categorization is too low to be effective. 

