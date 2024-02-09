# ICU-Mortality-Prediction
A patient survival prediction model leveraging machine learning techniques and data from the first 24 hours of intensive care.

## Abstract
Intensive Care Units in hospitals are one of the most critical places. A patient is moved to the ICU when their health is deteriorating. The urgency and type of therapy are determined by examining the patient. We can respond to threats ahead of time and offer the patient more advanced care if we can estimate a patient’s survival probability using data from multiple metrics collected during the first 24 hours of admission to an intensive care unit. This increases the patient’s chances of survival. As a result, the mortality rate in hospitals will be lower. A critical point to remember in this case, as in many others, is that the data is highly skewed. The goal is to develop a model that predicts patient survival based on data from the first 24 hours of intensive care.

## Dataset

The dataset has been released as open source by MIT
GOSSIS community initiative, with privacy certification from
the Harvard Privacy Lab. The dataset consists of more than
130,000 hospital Intensive Care Unit (ICU) visits from patients, spanning a one-year timeframe at various hospitals
located in Argentina, Australia, New Zealand, Sri Lanka,
Brazil, and more than 200 hospitals in the United States. The
dataset consists of 186 attributes and 91713 instances – out
of which 15 are categorical and 171 are of numerical type.
The target attribute we are trying to predict is ‘hospital death’
– 1 implies death and 0 implies survival. Out of the 91713
instances in our dataset - 83798 entries correspond to a survival
7915 entries correspond to a death. As we can see, the dataset
is skewed and this is addressed in the following sections.

## Machine Learning Models

Logistic Regression,
Decision Trees, and
XGBoost

## Results

The Logistic Regression and Decision Tree algorithms perform well in accuracy on the whole dataset but fail to predict
a death with proper precision when original data is used.
Undersampling and Oversampling solve the metric problem to
an extent when we deal with an unbalanced dataset, but they
add their own baggage - undersampling results in data loss and
oversampling creates lots of false data. The effects of sampling differ for each technique; some algorithms work better
with undersampled data and some algorithms work better with
oversampled data. ROC-AUC score is taken as a metric when
class imbalance is present. XGBoost successfully boosts both
the ROC and F1 scores. Recursive Feature Elimination results
in a subset of features that give comparable metric values
when compared with the results associated with the original set
of columns. All the models make better generalizations when
sampling techniques are applied to this problem. It betters
the model’s capacity of predicting mortality for a patient
appropriately.
