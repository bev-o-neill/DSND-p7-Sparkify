# DSND-p7-Sparkify


## Installation

The notebook in this repository was developed using Python v3.6.3, Pyspark v2.4.3, Pandas v0.23.3, and Matplotlib v2.1.0.

## Project Motivation

Customer churn is thorny issue for many businesses. Losing customers means losing revenue. British businesses are losing an eye-watering £25bn per year in avoidable customer churn.

Sparkify, a fictitions music streaming company, are concerned about their own customer churn rates. They have given us access to a sample of their user event log to develop a model that predicts which of their customers are a flight risk.


## File Descriptions

* Sparkify.ipynb contains all the code for data loading, preprocessing, analysis and model development.

* mini_sparkify_event_data.json is a copy of the dataset used for our notebook (JSON format).


## Results

The main findings of this analysis are summarised in a blog post available here: 

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

We tested four different machine learning classifiers with default parameters to see which was best for the data. The classifiers and their results were:
* Naive Bayes (f1 score xxxx)
* Logistic Regression (f1 score xxxx)
* Gradient Boosting Tree (f1 score xxxx)
* Linear SVM (f1 score xxxx)

We took the Gradient Boosting Tree forward for final hyperparamter tuning. The parameters and performance for the best model were:
* F1 score: 
* Area under the Precision-recall curve: 


## Licensing

Dataset in this repository appear courtesy of Udacity.
