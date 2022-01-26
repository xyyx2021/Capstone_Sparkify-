# Capstone_Sparkify
Udacity Data Science Nano degree

## Table of contents
* [Overview](#overview)
* [Dataset](#dataset)
* [Context](#context)
* [Files](#files)
* [Installation](#installation)
* [Results](#results)
* [Blog](#blog)

## Overview
**Sparkify** is a digital platform providing digital music service, similar as Spotify or Pandora. In Sparkify, many of the users stream their favorite songs in Sparkify, either using free tier service from advertisement link, or using the subscription model with a monthly flat rate to stream free music. User can upgrade, downgrade or cancel their service at anytime. This project is to build model to predict churn events. This results could be also used for business strategy development to reduce the churn. 

## Dataset
The full dataset is 12Gb, for this project, we only use a mini subset saved as .json file provided by Udacity cluster workspace, about 128 Mb size.

## Context
Following steps are taken to reach the goal.
* Load and clean dataset: remove the null values and duplicated values
* Exploratory data analysis: get, display and find the relevant attributes from the data using spark.sql
* Define churn event and group relevant attributes data with the churn event
* Feature engineering: creating and normalizing the relevant features, including categorial features and numerical features, for modeling
* Modeling: three ML methods, Logistic Regression, Decision Tree Classifier, and Random Forest Classifier are applied in training and test to model churn events.

## Files
*mini_sparkify_event_data.json*: The minisub data file provided by Udacity                                                    
*Sparkify.ipynb*: The code steps


## Installation
* Python 3.6
* Pyspark ML
* NumPy                                         
* pandas                                                   
* Matplotlib                                 
* Seaborn                                      

## Results
By combining both categorical features and numerical features, the Decision Tree Classifier has the best performance with the F1-score of 0.73, and the least time spent (296s). The Logistic Regression and Random Forest Classifier have a slightly lower F1-score, but quite close, with 0.65 and 0.63. Further refinement on the Decision Tree Classifier with adding maximum of tree depth and bins didn't improve the F1-score, but at the risk of overfitting. 

## Blog

[Predict Sparkify Custormer Churn using Data Science and ML](https://medium.com/@xueyang1983/predict-churn-using-big-data-analysis-with-sparkify-37c3f6885b57)
