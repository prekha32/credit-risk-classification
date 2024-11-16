# Credit Risk Classification

## Background
In this challenge, we will use various machine learning techniques to train and evaluate a model based on loan risk. The goal is to build a model that can accurately identify the creditworthiness of borrowers by analyzing a dataset of historical lending activity from a peer-to-peer lending services company.

## Project Setup
### Repository Creation
1. Create a new repository on GitHub called `credit-risk-classification`.
2. Clone the repository to your local machine.
3. Create a folder titled `Credit_Risk` inside the repository.
4. Add the `credit_risk_classification.ipynb` and `lending_data.csv` files from the provided `Starter_Code.zip` to the `Credit_Risk` folder.
5. Commit your changes and push them to GitHub.

### Files Used
- `credit_risk_classification.ipynb`: Jupyter Notebook containing the model code and analysis.
- `lending_data.csv`: Dataset containing historical lending data.

## Instructions
### 1. Split the Data into Training and Testing Sets
- Read the `lending_data.csv` data into a Pandas DataFrame.
- Create the labels set (`y`) from the `loan_status` column. A value of `0` indicates a healthy loan, and `1` indicates a high-risk loan.
- Create the features set (`X`) from the remaining columns.
- Split the data into training and testing sets using `train_test_split`.

### 2. Create a Logistic Regression Model with the Original Data
- Fit a logistic regression model using the training data (`X_train` and `y_train`).
- Generate predictions using the testing feature data (`X_test`).
- Evaluate the model’s performance:
  - Generate a confusion matrix.
  - Print the classification report.
  - Answer: How well does the logistic regression model predict the `0` (healthy loan) and `1` (high-risk loan) labels?

### 3. Write a Credit Risk Analysis Report
Write a report summarizing the performance of the machine learning model and your analysis in `README.md`:

- **Overview of the Analysis**: Explain the purpose of this analysis.
- **Results**:
  - **Accuracy Score**: The model's accuracy at predicting both labels.
  - **Precision Score**: The precision for both `0` (healthy) and `1` (high-risk) labels.
  - **Recall Score**: The recall for both `0` (healthy) and `1` (high-risk) labels.
- **Summary**:
  - Summarize the results of the logistic regression model.
  - Provide a recommendation on whether the model should be used by the company, with justification.

## Results
### Performance Metrics
- **Accuracy**: 99%
- **Precision**:
  - Healthy Loans (`0`): 1.00
  - High-Risk Loans (`1`): 0.84
- **Recall**:
  - Healthy Loans (`0`): 0.99
  - High-Risk Loans (`1`): 0.94
- **F1-Score**:
  - Healthy Loans (`0`): 1.00
  - High-Risk Loans (`1`): 0.89

### Summary
The logistic regression model demonstrates high accuracy, with an overall score of 99%. It performs exceptionally well at predicting healthy loans, with perfect precision and recall. For high-risk loans, the precision is slightly lower (84%), but the recall is still strong (94%). This indicates that while the model identifies most high-risk loans accurately, there may be some false positives.

**Recommendation**: The model is highly effective for identifying loan risk and can be recommended for use, given its strong performance metrics. However, consideration should be given to potential improvements for higher precision on high-risk loans to minimize false positives.
