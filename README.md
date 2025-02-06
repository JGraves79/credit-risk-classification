# credit-risk-classification
Module_20_challenge

# Import the modules

---

## Split the Data into Training and Testing Sets

### Step 1: Read the `lending_data.csv` data from the `Resources` folder into a Pandas DataFrame.

### Step 2: Create the labels set (`y`) from the “loan_status” column, and then create the features (`X`) DataFrame from the remaining columns.

### Step 3: Split the data into training and testing datasets by using `train_test_split`.

---

## Create a Logistic Regression Model with the Original Data

### Step 1: Fit a logistic regression model by using the training data (`X_train` and `y_train`).

### Step 2: Save the predictions on the testing data labels by using the testing feature data (`X_test`) and the fitted model.

### Step 3: Evaluate the model’s performance by doing the following:

* Generate a confusion matrix.
* Print the classification report.

### Step 4: Answer the following question.

**Question:** How well does the logistic regression model predict both the `0` (healthy loan) and `1` (high-risk loan) labels?

**Answer:** The model correctly predicts the Healthy loans almost 100%. The high-risk loans are only predicted 84 percent of the time. That is likely not good enough for a credit-rating model. The model should be adjusted as needed with some other regression models to do a better job making the high-risk prediction, even at the expense of a lower healthy loan rating.

### Analysis of the Precision Results

The classification report provides several key performance metrics for the logistic regression model: precision, recall, f1-score, and support. Let's break these down:

- **Precision** indicates the accuracy of the positive predictions. For Healthy loans, the precision is 1.00, meaning the model is very accurate in predicting Healthy loans. For High_Risk loans, the precision is 0.84, indicating that 84% of the loans predicted as High_Risk are actually High_Risk.
  
- **Recall** measures the ability of the model to identify all relevant instances. For Healthy loans, the recall is 0.99, meaning the model correctly identifies 99% of actual Healthy loans. For High_Risk loans, the recall is 0.94, indicating that the model correctly identifies 94% of actual High_Risk loans.

- **F1-Score** is the harmonic mean of precision and recall, providing a single metric for overall model performance. For Healthy loans, the f1-score is 1.00, indicating perfect performance. For High_Risk loans, the f1-score is 0.89, showing a solid performance but with room for improvement.
  
- **Support** is the number of actual occurrences of each class in the dataset. There are 18,765 Healthy loans and 619 High_Risk loans in the test set.

---
