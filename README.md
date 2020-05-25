# Capstone Project: Create a Customer Segmentation Report for Arvato Financial Services

In this project, you will analyze demographics data for customers of a mail-order sales company in Germany, comparing it against demographics information for the general population. You'll use unsupervised learning techniques to perform customer segmentation, identifying the parts of the population that best describe the core customer base of the company. Then, you'll apply what you've learned on a third dataset with demographics information for targets of a marketing campaign for the company, and use a model to predict which individuals are most likely to convert into becoming customers for the company. The data that you will use has been provided by our partners at Bertelsmann Arvato Analytics, and represents a real-life data science task.

If you completed the first term of this program, you will be familiar with the first part of this project, from the unsupervised learning project. The versions of those two datasets used in this project will include many more features and has not been pre-cleaned. You are also free to choose whatever approach you'd like to analyzing the data rather than follow pre-determined steps. In your work on this project, make sure that you carefully document your steps and decisions, since your main deliverable for this project will be a blog post reporting your findings.


## Table of Contents

 1. Project Overview 
 2. Data 
 3. Technical Overview 
 4. Requirements 
 5. Libraries
 6. Summary/Report of findings 
 7. Acknowledgements


## 1. Project Overview
 In this project, we are provided with demographic data of customers of a mail-order company in Germany and demographic data of general population of Germany. Using this data, we are required to identify new customers for the company.

 We approach this project in 2 phases:

 Use Unsupervised Learning to perform customer segmentation and identify clusters/segments from general population who best match mail-order company's customer base.
 Use Supervised Learning to identify targets for marketing campaign of the mail-order company who could possibly become their customers.
 Goal of this project is to predict individuals who are most likely to become customers for a mail-order sales company in Germany.

 Please find detailed overview of the project in blog post: https://medium.com/@ranjeetraj2005/customer-segmentation-report-for-arvato-financial-services-a6c463d9373d

## 2. DataSet

 Total 4 datasets were provided: 
 • Udacity_AZDIAS_052018.csv: Demographics data for the general population of Germany; 891 211 persons (rows) x 366 features (columns). 
 • Udacity_CUSTOMERS_052018.csv: Demographics data for customers of a mail-order company; 191 652 persons (rows) x 369 features (columns). 
 • Udacity_MAILOUT_052018_TRAIN.csv: Demographics data for individuals who were targets of a marketing campaign; 42 982 persons (rows) x 367 (columns). 
 • Udacity_MAILOUT_052018_TEST.csv: Demographics data for individuals who were targets of a marketing campaign; 42 833 persons (rows) x 366 (columns). 
 The first two datasets were used for comparison analysis – how customers are similar or differ to the general population. The results from this analysis were then used to create predictions on the MAILOUT files. Another file (feat_info) was also provided which includes a list of attributes, description and corresponding data values. This dataset had 324 attributes.

## 3. Technical overview:

   Step by step workflow from data exploration, processing to inference is approached in a structured fashion. Because of the large volume of source data, we build preprocessing pipeline to get rid of unnecessary and outlier data and implement Dimensionality Reduction and Clustering to identify segments. Due to the nature of the data (details in notebook), AUC/ROC is used as the evaluation metric for this project. Prediction for test set is to be submitted to Kaggle competition for evaluation.

   Following concepts implemented and covered in detail in the notebook:

   ### Part 1:
     Data Exploration & Data wrangling/Cleansing
     Principal component analysis (PCA)
     Customer Clustering
   ### Part 2:
     Supervised Learning Model
     Final Model Evaluation
     Analyse most important feature Importance
     Analysis of identified important features in clusters to find relevance
     Scoring and submisstion to Kaggle

## 4. Requirements
    All of the requirements are captured in requirements.txt. Run: pip install -r requirements.txt

## 5. Libraries
    Pandas, Numpy, Sklearn, Time, Seaborn, Pickle, matplotlib

## 6. Summary/Report of findings
    A detailed report can be found at: https://medium.com/@ranjeetraj2005/customer-segmentation-report-for-arvato-financial-services-a6c463d9373d

## Acknowledgements
I would like to than Bertelsmann Arvato Analytics for providing the data used for this project and for all the mentors at Udacity.
