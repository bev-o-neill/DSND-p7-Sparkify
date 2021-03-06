# DSND-p7-Sparkify


## Installation

The notebook in this repository was developed using Python v3.6.3, Pyspark v2.4.3, Pandas v0.23.3, and Matplotlib v2.1.0.

## Project Motivation

Customer churn is thorny issue for many businesses. Losing customers means losing revenue. British businesses are losing an eye-watering £25bn per year in avoidable customer churn.

Sparkify, a fictitions music streaming company, are concerned about their own customer churn rates. They have given us access to a sample of their user event log to develop a model that predicts which of their customers are a flight risk.


## File Descriptions

* Sparkify-analysis and preprocessing.ipynb contains all the code for data loading, preprocessing, analysis and feature engineering. Produces dfFinal.csv as output.

* Sparkify-model build.ipynb does exactly what it says on the tin: develops and tunes a model on the dataset output in Sparkify-analysis and preprocessing.ipynb

* mini_sparkify_event_data.json is a copy of the dataset used for our notebook (JSON format).

* dfFinal.csv the dataset output from Sparkify-analysis and preprocessing.ipynb. This is the data upon which we build our customer churn predictive model.

## Results

The main findings of this analysis are summarised in a blog post available here: https://medium.com/@oneill.beverley/how-deep-is-their-love-749bc9913c66

We engineered 65 features from the event log dataset. These can be broadly categorised as:
* Time since registration and latest activity
* Subscription level
* Session counts
* Interaction counts
* Songs played
* Home/Add Friend/Add to Playlist/Next Song/Thumbs Up/Logout page views
* Days/Weeks/Fortnights active and activity ratios
* Session/interaction/time on site in the weeks 1,2,3,4 prior to latest activity
* Ratio of activity in the final fortnight compared to the fortnight previous.

We tested five different machine learning classifiers with default parameters to see which was best for the data. The classifiers and their results were:
* Naive Bayes (f1 score 0.813)
* Logistic Regression (f1 score 0.828)
* Random Forest (f1 score 0.891)
* Gradient Boosting Tree (f1 score 0.808)
* Linear SVM (f1 score 0.817)

We took the Random Forest forward for final hyperparamter tuning. The parameters and performance for the best model were:
* F1 score: 0.919
* Area under the Precision-recall curve: 0.511

## Improvements
* Reduce the number of features of the input dataset by removing highly correlated variables
* Run over more hyperparameters
* Repeat using the full dataset (which is available in AWS/IBM Watson) running it on a Spark cluster

## Licensing

Dataset in this repository appears courtesy of Udacity.
