# Module-12-Challenge
#
$ FinTech Bootcamp Module 12 Challange due June 11, 2023

# Challenge - Credit Risk Classification

Credit Risk Classificationjupyter notebook

## Analysis

We create a logistic regression model using supplied historical lending activity dataset to compare two versions of the dataset, the original dataset, and an enlarged, resampled dataset.

* Purpose

Credit risk poses a classification problem that’s imbalanced. We use imbalanced classes from the lending_data.csv dataset of historic lending activity to build and compare models to identify creditworthiness.

We use lending_data.csv which contains historical lending activity from a peer-to-peer lending services company. We are trying the best models to predict creditworthiness.

* The variables we evaluate and are trying to predict are:

  * value_counts : the number of target values for X and y. Should differ for original data. Should be equal after resampling.

  * balanced_accuracy_score : (TP rate + TN rate) divided by 2, (TP / (TP + FN) + TN / (TN + FP)) / 2

  * confusion_matrix : 2 by 2 matrix of (TP, FP) in 1st row, (FN, TN) in 2nd row.

  * precisiom : the ratio of TP, TP / (TP + FN).
  
  * recall : the percentage of positives predicted, TP / (TP + FP).

  * F1 : indicates efficiency, 2 x ((recall * precision) / (recall + precision}), one of the most used metrics here.

* The stages of the machine learning process for this analysis are:

  * Split the Data into Training and Testing Sets.

  * Create a Logistic Regression Model with the Original Data.

  * Predict a Logistic Regression Model with Resampled Data.

* The methods used:

  * We split the data using train_test_split()

  * We create a Logistic Regression Model with the Original Data using LogisticRegression().

  * We predict a Logistic Regression Model with Resampled Training Data using RandomOverSampler().

## Results

* Logistic Regression Model with the Original Data:
 
  *   balanced_accuracy_score: 0.95
  *                 Precision: 0.85
  *                    Recall: 0.91
  *                        F1: 0.88


* Logistic Regression Model with Resampled Data:
  
  *   balanced_accuracy_score: 0.99
  *                 Precision: 0.84
  *                    Recall: 0.99
  *                        F1: 0.91

## Summary

* The f1-score for Oversampled 0.91 indicates higher accuracy than the Original 0.88, higher means better.

* The precision for Oversampled 0.84 is slightly less accurate at making predictions than the Original 0.85.

- The recall for Oversampled 0.99 indicates more accuracy at predicting than the Original 0.91.

The F1 Score for Oversampled rose 3 points, a measure of how many the model got right. Thus the Oversmpled seems to perform best. We can try other models to see how they perform?

It is very important to predict the number of '0's since it represents actual loans versus multiples of '1's. 

# github.com repository link

	https://github.com/NvPahrump/Module-12-Challenge

## Technologies

This app is designed for Python 3.7 notebooks on Anaconda 3

It uses Python 3.7 libraries

	numpy
	pandas
	pathlib
	sklearn.metrics
	imblearn.metrics
	matplotlib
    
## Source Files:

    README.md

	credit_risk_resampling.ipynb

##  Resource Files:

	Resources/lending_data.cs

## To Run on Anaconda 3:

	jupyter lab &

	open credit_risk_resampling.ipynb

## Contributors

Randy Miyazaki modified forecasting_net_prophet.ipynb for the class assignment

## License

Intended for Randy Miyazaki and Fintech Bootcamp class personnel
