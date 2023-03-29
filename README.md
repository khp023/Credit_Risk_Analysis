# Credit_Risk_Analysis

## Overview 

The purpose of this analysis is to employ machine learning techniques through the `imbalanced-learn` and `scikit-learn` python libraries to assess a method of potentially predicting credit risk. Due to the nature of the situation being an unbalanced set of data to classify, the following algorithms are used resample/reduce bias: 
- RandomOverSampler
- SMOTE
- ClusterCentroids
- SMOTEENN
- BalancedRandomForestClassifier
- EasyEnsembleClassifier

## Results

Following the study and the determination of each method's balanced accuracy scores and imbalanced classification reports, the following chart was compiled: 
![Results](/screenshots/chart.png)

## Summary

Following the results, we see see that the bias reduction models (BalancedRandomForestClassifier and EasyEnsembleClassifier) outperform the resampling models by a significant margin. Across all models; however, the precision scores were `1.00` for identifying low risk instances. 

The recommended machine learning model for this analysis of the ones used is the EasyEnsembleClassifier from `imbalanced-learn`, as it outclasses each of the other models with a balanced accuracy score of 94%. Despite this, it was only able to deliver a precision of `0.07` for high risk loans. That with a combination of a higher recall implies fewer false negatives but higher amounts of false positives in determining high risk loans; it is sensitive in identifying, but may mismark low risk loans as well as high risk.  

The general risk in using this is lower, as though it is still recommended for use, extra vigilance in ruling out the low risk loans from the identified high risk loans is necessary. 
