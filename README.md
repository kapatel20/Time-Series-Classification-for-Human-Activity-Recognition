# Project README

## Time Series Classification for Human Activity Recognition

### Overview:

This project focuses on the classification of human activities based on time series data obtained from a Wireless Sensor Network. The dataset used is the AReM (Activity Recognition system based on Multisensor data fusion) dataset, which consists of seven folders representing seven types of activities. Each folder contains multiple files, each representing an instance of a human performing an activity. Each file contains six time series: avg rss12, var rss12, avg rss13, var rss13, vg rss23, and ar rss23. The goal is to classify the activities using time-domain features extracted from these time series.

### Part 1: Feature Creation/Extraction

#### (a) Data Download:

- Download the AReM data from [UCI Machine Learning Repository](https://archive.ics.uci.edu/ml/datasets/Activity+Recognition+system+based+on+Multisensor+data+fusion+%28AReM%29).
  
#### (b) Data Split:

- Keep datasets 1 and 2 in folders bending1 and bending 2 as test data, and datasets 1, 2, and 3 in other folders as train data.

#### (c) Feature Extraction:

- Research and extract time-domain features (e.g., minimum, maximum, mean, median, standard deviation, first quartile, and third quartile) for all six time series in each instance.
- Normalize/standardize features if needed.
- Estimate the standard deviation and create a 90% bootstrap confidence interval for each feature.
- Select the three most important time-domain features.

### Part 2: Binary and Multiclass Classification

#### (a) Binary Classification Using Logistic Regression:

- Depict scatter plots for features extracted from time series 1, 2, and 6 to distinguish bending vs. other activities.
- Break time series into two parts and compare results.
- Break time series into l segments and use logistic regression for binary classification.
- Use 5-fold cross-validation to find the best value of l. Consider class imbalance and use stratified cross-validation if needed.
- Report confusion matrix, ROC, AUC, logistic regression parameters, and p-values.
- Test the classifier on the test set and compare accuracy.

#### (b) Binary Classification Using L1-penalized Logistic Regression:

- Repeat binary classification using L1-penalized logistic regression.
- Cross-validate for both the number of time series (l) and the weight of L1 penalty ().
- Compare results with variable selection using p-values.

#### (c) Multiclass Classification:

- Find the best l for L1-penalized multinomial regression.
- Report test error, confusion matrix, ROC, and AUC for multiclass classification.
- Repeat using Naive Bayes classifier with Gaussian and Multinomial priors.
- Compare methods for multi-class classification.

### Conclusion:

Summarize the results, discuss the performance of different classifiers, and provide insights into the suitability of methods for time series classification in this context.
