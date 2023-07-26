# credit-risk-classification

In this exercise we used machine learning techniques to analyze find credot-worthiness from historical lending activity of a peer-to-peer lending service.

# Analysis
The data included the following fields:

* loan size
* hits/bad marks against the applicant
* applicant income
* total applicant debt
* applicant debt-to-income ratio
* interest rate
* applicants # of open accounts

1. Data split into training and testing sets. We used the training set to build a first logistic regression model.
2. We applied the LogisticRegression module to the testing dataset. 
3. We could determine an applicants level of risk
    * This intial model was drawing from a dataset that had 75k low-risk loan data points and 2.5k high-risk data points. 
4. To resample the training data and ensure that the logistic regression model had an equal number of data points to draw from, the training set data was resampled with the RandomOverSampler. 
    * This generated 56k data points for both low-risk and high-risk loans.
    * Resampled data was used in building a second logistic regression model.

# Model Results
## First Logistic Regression Model

Model scored as 93% precise. Note: the model was only 87% precise in predicting risky loans, despite 100% in non-risky loans.

Model scored a 94% accuracy.

Recall came in at 95%. Note: the model had only 89% recall in risky loans, despite 100% in non-risky loans. 

## Second Logistic Regression Model (More Accurate)

Model scored as 93% precise. Note: the model was only 87% precise in predicting risky loans, despite 100% in non-risky loans.predicting high-risk loans. (no change from first model)

Model scored a 100% accuracy.

Recall came in at 100%. 

* This second model is less likely to produce "false-negative" results. 
* While this model did produce a few more "false-positives" I believe it is a more accurate model when determining the riskiness of an applicant.
