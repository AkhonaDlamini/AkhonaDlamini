# 🔍 Predicting Employee Withdrawals from Retirement Savings

## 📌 Project Overview

This project explores the behavioral patterns that lead employees to withdraw from their accessible retirement savings. Using a custom dataset I created—since no existing one fully captured key factors like retirement behavior and income levels—I trained a machine learning model to predict withdrawal behavior using real-world financial indicators.

## 🧠 Reason for Creating the Dataset

Most publicly available datasets lacked important features such as:

* Individual savings behavior
* Income level
* Retirement savings totals
* Economic variables like interest and inflation rates

This dataset was built to enable **comprehensive analysis** of factors influencing withdrawal behavior. The goal was to bridge a data gap in financial planning and retirement behavior studies.

## 📊 Dataset Details

**Number of records**: 1,000
**Columns**:

* Age
* Gender
* Marital Status
* Income Level
* Savings Rate
* Retirement Savings
* Withdrawal Behavior (Target)
* Inflation Rate
* Interest Rate

Each record represents an employee and their financial profile, with the target variable being whether they withdrew from their retirement pot.

## 🧹 Data Preparation

* Checked for null values and duplicates (none found ✅)
* Encoded categorical variables using one-hot encoding
* Performed exploratory analysis (e.g., age vs. withdrawal behavior)

## 📈 Data Visualization

A boxplot revealed that older employees are more likely to make withdrawals, possibly due to retirement, health-related costs, or family obligations. This reinforces real-world trends in personal finance and supports the dataset’s realism.

## 🧪 Modeling Approach

* **Model**: Random Forest Classifier
* **Features**: All columns except the target
* **Split**: 80% training / 20% testing
* **Performance**:

  * Accuracy: \~70%
  * Precision (Class 1): 40%
  * Recall (Class 1): 11%
  * F1-score (Class 1): 17%

While accuracy is decent, the model struggles to detect withdrawals (`class 1`) due to class imbalance.

## 📉 Limitations

* **Imbalanced Classes**: Majority of data points are `0` (no withdrawal), which impacts recall and precision for the minority class.
* **Synthetic Dataset**: Although thoughtfully crafted, the data isn't from real employee records, so conclusions should be treated with caution in a business context.

## 🔮 Forecasting Next Steps

### For Future Improvements:

* Apply SMOTE or other oversampling techniques to address class imbalance.
* Experiment with other models (e.g., Gradient Boosting, XGBoost).
* Introduce more behavioral data (e.g., financial literacy, risk tolerance).
* Track changes over time to turn this into a **time-series** forecasting problem for long-term savings behavior.
