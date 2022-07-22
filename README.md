# Credit_card_default_prediction
## Introduction
This work aims to highlight the mathematical features of the methodologies utilised by utilising some supervised machine learning algorithms to discover the important drivers that impact the chance of credit card default. When you have fallen far behind on your credit card payments, you enter credit card default. Taiwan's card-issuing banks overissued cash and credit cards to unqualified applicants in an effort to gain market dominance. In addition, most cardholders abused their credit cards for consumption, regardless of their ability to pay back the balance, and racked up significant debt.

The objective is to create an automated model that can both identify the important variables and predict a credit card default based on the client's information and previous transactions. Later, the fundamental ideas of the supervised machine learning paradigm are provided together with a thorough analysis of all the methods and algorithms employed to create the models. The algorithms for Logistic Regression, Random Forest, and Support Vector Machines have been used in particular.

## Feature Analysis
The dataset used in this study is the Default of credit card clients from the UCI machine learning repository, available at the following link.
It consists of 30000 observations that represent distinct credit card clients. Each observation has 24 attributes that contain information on default payments, demographic factors, credit data, history of payment, and bill statements of credit card clients in Taiwan from April 2005 to September 2005.

The first group of variables contains information about the client personal information:

    ID: ID of each client, categorical variable
    LIMIT_BAL: Amount of given credit in NT dollars (includes individual and family/supplementary credit)
    SEX: Gender, categorical variable (1=male, 2=female)
    EDUCATION: level of education, categorical variable (1=graduate school, 2=university, 3=high school, 4=others, 5=unknown, 6=unknown)
    MARRIAGE: Marital status, categorical variable (1=married, 2=single, 3=others)
    AGE: Age in years, numerical variable

The following attributes contains information about the delay of the past payment referred to a specific month:

    PAY_0: Repayment status in September 2005 (-1=pay duly, 1=payment delay for one month, 2=payment delay for two months, … 8=payment delay for eight months, 9=payment delay for nine months and above)
    PAY_2: Repayment status in August 2005 (same scale as before)
    PAY_3: Repayment status in July 2005 (same scale as before)
    PAY_4: Repayment status in June 2005 (same scale as before)
    PAY_5: Repayment status in May 2005 (same scale as before)
    PAY_6: Repayment status in April 2005 (same scale as before)

Other variables instead consider the information related to the amount of bill statement (i.e. a monthly report that credit card companies issue to credit card holders in a specific month):

    BILL_AMT1: Amount of bill statement in September, 2005 (NT dollar)
    BILL_AMT2: Amount of bill statement in August, 2005 (NT dollar)
    BILL_AMT3: Amount of bill statement in July, 2005 (NT dollar)
    BILL_AMT4: Amount of bill statement in June, 2005 (NT dollar)
    BILL_AMT5: Amount of bill statement in May, 2005 (NT dollar)
    BILL_AMT6: Amount of bill statement in April, 2005 (NT dollar)

The following variables instead consider the amount of previous payment in a specific month:

    PAY_AMT1: Amount of previous payment in September, 2005 (NT dollar)
    PAY_AMT2: Amount of previous payment in August, 2005 (NT dollar)
    PAY_AMT3: Amount of previous payment in July, 2005 (NT dollar)
    PAY_AMT4: Amount of previous payment in June, 2005 (NT dollar)
    PAY_AMT5: Amount of previous payment in May, 2005 (NT dollar)
    PAY_AMT6: Amount of previous payment in April, 2005 (NT dollar)

The last variable is the one to be predicted:

    default.payment.next.month: indicate whether the credit card holders are defaulters or non-defaulters (1=yes, 0=no)

The main aim of the data is to discriminate clients that are predicted to credit card default the next month, according to the default.payment.next.month column which is set to “0” for non-defaulters and “1” for defaulters. Thus, it is a binary classification problem on a relatively unbalanced dataset

