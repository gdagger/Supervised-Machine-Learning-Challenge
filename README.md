# Supervised Machine Learning Challenge
### Glen Dagger

The purpose of this challenge is create and fit a Logistic Regression model and Random Forest Classifier to the provided data in order to see which performed better.

<hr>
### Predict Model Performance

I predicted that the logistic regression will perform better since there are only 7 features and all seem like they could plausibly be related to whether a loan would be denied or approved (i.e. less noise in the parameters to tune out). We are only categorizing the data into two possible groups (approved/denied) so it seems like logistic regression would be the better choice.

### Split the Data into Training and Testing Sets
 
I first read in the csv file using Pandas and removed all duplicate rows (no values were missing). I created the features dataframe, X, by removing the "loan_status" column from the original dataframe. I created the labels set by setting 'y' equal to the "loan_status" column. I used the train_test_split function on X and y to split the data into training and testing datasets.

### Create, Fit, and Compare Models

I first created and fit a Logistic Regression model using SciKitLearn. This model had a score of about 92% on the testing data. I then created and fit a Random Forest Classifier model with 500 estimators. This model scored about 86% on the testing data. Ultimately, this showed that the Logistic Regression outperformed the Random Forest Classifier and did so much faster.