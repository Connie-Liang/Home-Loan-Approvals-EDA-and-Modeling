# Home-Loan-Approvals-EDA-and-Modeling

# GOAL
To predict whether a company will approve a loan or not, with special attention to minimizing the False Positive rate, and to examine which features were more influential.

WHY:
when a company approves a loan, they are predicting that the applicant will be able to pay the loan back. If the applicant ends up in the False Positive realm, the applicant poses a financial risk of default.

# FINDINGS
Using a logistic regression model with 10 fold K-fold cross validation, I found that just income and hoepa status (high cost loan) could reliably predict whether a home loan would be approved or rejected with an accuracy score of .91, a precision score of .99, and a recall score of .88.

I improved my model when using a random forest model and including 10 features. Here, I produced an accuracy score of .94, a precision score of .96, and a recall score of .95. My random forest model further affirmed my logistic regression findings by classifying the income, hoepa status, and applicant credit score type as the most influential features in the data.

The random forest model still outperforms the logistic regression, as the accuracy and recall is higher, and the higher recall in the random forest model offers better balance between prediction of False Positive and False Negative predictions.

# Google Presentation Slides: 
https://docs.google.com/presentation/d/1Sr2aJVaEza6V-AZvfgQOq2F1klLFUHwjjSL3fCFvIe4/edit#slide=id.g35f391192_029


# NEXT STEPS:
- rerun the models with more refined dummified features (try loan term, age, ethnicity, gender)
- plot the roc curve of logistic regression vs decision tree vs random forest
- expriment with pca and reducing dimensionality
- plot a profit curve with varying thresholds


# ABOUT THE DATA:
662,100 rows (loan applications)
99 columns

CLEANING:
removed 38 columns
10 columns used for modeling

INITIAL FEATURES OF INTEREST:
- income
- hoepa status
- debt to income ratio
- applicant ethnicity
- applicant age

MULTICOLLINEAR FEATURE TO EXCLUDE:
-denial reason (1-4)

MODELS USED:
logistic regression with 10 fold k-fold cross validation
random forest

# DATA SOURCE
Federal Financial Institutions Examination Council's (FFIEC), Home Mortgage Disclosure Act - https://ffiec.cfpb.gov/data-browser/data/2019?category=states&items=CA
Index of Features
- https://ffiec.cfpb.gov/documentation/2019/lar-data-fields/


