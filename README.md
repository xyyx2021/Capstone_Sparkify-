# Capstone_Sparkify-
Udacity Data Science Nano degree

## Table of contents
* [Overview](#overview)
* [Dataset](#dataset)
* [Context](#context)
* [Files](#files)
* [Installation](#installation)
* [Results](#results)

## Overview
**Sparkify** is a digital platform providing digital music service, similar as Spotify or Pandora. In Sparkify, many of the users stream their favorite songs in Sparkify, either using free tier service from ads, or using the subscription model with a monthly flat rate to stream free music. User can upgrade, downgrade or cancel their service at anytime. This project is to build more to predict which users are more likely to churn or cancel their service. This results could be also used for business strategy development to reduce the churn. 

## Dataset
The full dataset is 12Gb, for this project, we only use a mini subset saved as .json file provided by Udacity workspace, about 120 Mb size.

## Context
Following steps are taken to reach the goal.
* Load and clean dataset: remove the null values and duplicated values
* Exploratory data analysis: get, display and find the relevant attributes from the data using spark.sql
* Define churn event and group relevant attributes data with the churn event
* Feature engineering: creating and normalizing the relevant features, including categorial features and numerical features, for modeling
* Modeling: four ML methods, Logistic Regression, Decision Tree Classifier, Random Forest Classifier, and Linear SVM, are applied in training and test to model churn events.

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
By combining both categorical features and numerical features, the Linear SVC has the highest f1 score 0.67 comapred to Logistic Regression, Decision Tree and Random Forest classifier. However, the Linear SVC also has the longest training time, almost 10 times than other methods, if ran under the workspace. If we want to apply this to the whole dataset, logistic Regression is preferred method, as the f1 score from the Logistic Regression 0.62 is just 0.05 less than Linear SVC, but 9 times faster. 
