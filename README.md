
# **Predict Transaction Fraud Detection with Classification**

# INTRODUCTION


Problem Formulation Due to the private nature of financial data, there is a lack of publicly available datasets that can be used for analysis. In this project, a synthetic dataset, publicly available on Kaggle, generated using a simulator called PaySim is used. The dataset was generated using aggregated metrics from the private dataset of a multinational mobile financial services company.

There are 6362620 instances of data set, The data set has 11 attributes which include is

Type of transactions Amount transacted Customer ID and Recipient ID Old and New balance of Customer and Recipient Time step of the transaction Whether the transaction was fraudulent or not

**Problem Statement**

Leverage the given data set to build an End-to-End Data Science Project and find whether a transaction is Fradulent or not.

**Hypothesis Generation**

This is one of the important stages in any Data Science/Machine Learning pipeline. It involves understanding the problem in detail by brainstorming as many factors as possible which can impact the outcome. It is done by understanding the problem statement thoroughly and before looking at the data.

Below are some of the factors which I think can highly affect the target i.e. Fraudulent transaction:

**Type of transaction:** Based on the type (mode) of payment might impact the fradulent transaction.

**Amount:** The amount of transaction can decide the transaction is fradulent or not, we can find unusual activities through the amount of transaction.

**Initial Balance and Balance left:** By comparing account balances before the transcation and after transaction we might able to find whether there is unusual activity is happened or not
## Steps to follow


It is a Binary Classification Problem.

General Overview: Have a General Overview of the data
- **EDA:** Perform Exploratory Data Analysis(EDA) to gain more clear insights of the data
- **Data Preprocessing:** With the information gained after performing EDA, Preprocess the Data accordingly
- **Model Building:** Once the data is properly cleaned and preprocessed, use this data to build a Machine Learning
- **Model Performance:** Assess the Performance of the Model on the Testing data set
- **confusion matrix:** Evaluate the model using a confusion matrix to obtain an accuracy rate.
- **Predictions:** Make Predictions on the Testing data set
- **ROC Curve:** Receiver Operating Characteristic(ROC) curve is a plot of the true positive rate against the false positive rate. It shows the tradeoff between sensitivity and specificity.
## Loading the data
We now know that we are working with a typical CSV file (i.e., the delimiter is ,, etc.). We proceed to loading the data into memory.
## Inspecting Data Frame
Dataset description
- **step** - maps a unit of time in the real world. In this case 1 step is 1 hour of time. Total steps 744 (30 days simulation).
- **type** - CASH-IN, CASH-OUT, DEBIT, PAYMENT and TRANSFER.
- **amount** - amount of the transaction in local currency.
- **nameOrig** - customer who started the transaction
- **oldbalanceOrg** - initial balance before the transaction
- **newbalanceOrig** - new balance after the transaction
- **nameDest** - customer who is the recipient of the transaction
- **oldbalanceDest** - initial balance recipient before the transaction. Note that there is not information for customers that start with M (Merchants).
- **newbalanceDest** - new balance recipient after the transaction. Note that there is not information for customers that start with M (Merchants).
- **isFraud** - This is the transactions made by the fraudulent agents inside the simulation. In this specific dataset the fraudulent behavior of the agents aims to profit by taking control or customers accounts and try to empty the funds by transferring to another account and then cashing out of the system.
- **isFlaggedFraud** - The business model aims to control massive transfers from one account to another and flags illegal attempts. An illegal attempt in this dataset is an attempt to transfer more than 200.000 in a single transaction.
## Training Model
Metrics considered for Model Evaluation
- Cell Time for model Evaluation
- CV_Score
- Accuracy
- RMS Value
- Roc_Auc_Score
Confusion Matrix for different models
Model Development and Prediction using Random Forest Classifier Algorithm and we get 997% accuracy.


## Conclusion

With the advent of digital transactions, the possibility of money laundering have also soared up with the use of tech. Millions of investigators are on the field fighting against the fraudulent transactions. In the current industry we have a large inflow of false positives hits and it consumes a long time to clear the false positive hits. Customers across the world using fintech platforms demand lightning fast services. Hence automating the hits with machine learning and reducing the false positive hits is our aim. But not at the cost of leaving out the false negatives. Hence we need to be more mindful about false negatives when we try to reduce the false positives.an be explained by other variables in our dataset.

We get ROC AUC is 99%.that is best fitted model to predict fraud.


## What are the key factors that predict fraudulent customer?

Customer's identity (email addresses, credit card numbers, etc.) Their preferred payment methods, The source of request is secured or not Their network (emails, phone numbers, and payment details entered with the online account), The past order details.

## What kind of prevention should be adopted while company update its infrastructure?

- Setting the right risk threshold for your business
- screen public records of the user that might have been published in a given time period against the applicant
- Secure Infrastructure : Secure infrastructure implies the database systems and servers where data is stored and the boundaries established to secure these.Production data is usually encrypted in any core banking system. If required for testing, it is mandatory that important data like bank account number, customer name, and address be masked. Access to production systems is restricted. Vendors who deal with infrastructure are generally different from those who deal with applications. Bank employees are usually given special equipment where access to social websites, personal emails, and USB ports is blocked. Employees can only access the banks’ network over a VPN when using public Wi-Fi.
- Secure Processes : Banks have established many processes to ensure that security is implemented and tested. This includes KYC (Know Your Customer) updates for customers, NDA (Non-disclosure agreement) for employees and vendors, securing special zones within the premises and remote data centers.
- Continuous Communication : Banks also communicate regularly with consumers on upgrades to systems, the introduction of new authentication procedures, etc., in addition to the periodic account statements that are generated and sent to customers. Customers can also set limits and alerts based on different conditions to ensure that they are informed if any unexpected activity takes place concerning their accounts. While there are multiple channels of communication available, the set-up is flexible to cater to customers’ convenience.

## Assuming these actions have been implemented, how would you determine if they work?

- Bank sending E-statements.
- Customers keeping a check of their account activity.
- Always keep a log of your payments.
