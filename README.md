# Loan Status Prediction with Logistic Regression

## Overview
This project uses a logistic regression model to predict loan statuses (`healthy` or `high-risk`) based on various borrower attributes. The data is split into training and testing sets, and the performance of the model is evaluated using metrics such as accuracy, precision, recall, and F1-score.

## Data
The dataset used in this project contains the following features:

- `loan_size`: The amount of the loan.
- `interest_rate`: The interest rate on the loan.
- `borrower_income`: The borrower's income.
- `debt_to_income`: The borrower's debt-to-income ratio.
- `num_of_accounts`: The number of accounts the borrower has.
- `derogatory_marks`: The number of derogatory marks in the borrower’s credit history.
- `total_debt`: The total debt of the borrower.
- `loan_status`: The target variable, where `0` indicates a healthy loan, and `1` indicates a high-risk loan.

## Steps

### Step 1: Loading the Data
The dataset (`lending_data.csv`) was loaded into a Pandas DataFrame, and the data was reviewed to understand its structure and contents.

### Step 2: Separating Features and Labels
- The `loan_status` column was used as the target variable (`y`).
- The remaining columns were used as the feature set (`X`).

### Step 3: Splitting the Data
The data was split into training and testing sets using `train_test_split` with an 80/20 split and a `random_state` of 1 for reproducibility.

### Step 4: Building the Model
A logistic regression model was instantiated using `sklearn` and fit on the training data.

### Step 5: Making Predictions
The model was used to predict the loan statuses in the testing set.

### Step 6: Evaluating the Model
The model's performance was evaluated using a confusion matrix and a classification report. Key metrics include:
- **Accuracy**: 99%
- **Precision**, **Recall**, and **F1-Score** for both healthy loans (`0`) and high-risk loans (`1`).

The confusion matrix was:
[[14947 64] [ 47 450]]

markdown
Copy code

The classification report showed:
- **Precision**: The ability of the model to correctly identify positive predictions.
  - For high-risk loans (`1`), the precision was 0.88.
- **Recall**: The ability of the model to capture all relevant instances.
  - For high-risk loans (`1`), the recall was 0.91.
- **F1-score**: A balanced measure of precision and recall, which was 0.89 for high-risk loans.

## Conclusion
The logistic regression model performed very well, achieving an overall accuracy of 99%. It predicts healthy loans with near-perfect accuracy and has a good balance of precision and recall for high-risk loans.

## Dependencies
- Python 3.x
- Pandas
- Scikit-learn

## How to Run
1. Clone this repository.
2. Ensure that you have all required dependencies installed.
3. Load the dataset and execute the steps in the notebook or script.
