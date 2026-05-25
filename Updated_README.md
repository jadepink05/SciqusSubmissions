
# MINI ML IMPLEMENTATION – Predictive Maintenance Failure Prediction

## Dataset
Dataset used: `SciqusDS.csv`

The dataset contains industrial machine operation records and the goal is to predict whether a machine failure will occur.

---

# Approach

## 1. Understanding the Data
The dataset contains:
- Product identifiers
- Machine type
- Temperature measurements
- Rotational speed
- Torque
- Tool wear
- Failure target column

Target variable:
- `Target`
    - 0 = No Failure
    - 1 = Failure

---

## 2. Preprocessing
The following preprocessing steps were performed:

- Removed identifier columns:
  - `UDI`
  - `Product ID`

- Removed `Failure Type`
  - This column directly describes failures and may leak information to the model.

- Encoded categorical column:
  - `Type`

- Split dataset into training and testing data.

---

# Models Used

## Logistic Regression
Used as a simple baseline model because it is interpretable and easy to explain.

## Random Forest Classifier
Chosen because:
- Works well on tabular data
- Handles nonlinear relationships
- Provides strong predictive performance

---

# Evaluation Metrics

The models were evaluated using:
- Accuracy
- Precision
- Recall
- F1 Score
- ROC-AUC Score
- Confusion Matrix

---

# Conclusion

Random Forest performed better than Logistic Regression because it captured more complex relationships in the dataset.

---

# Future Improvements

If given more time:
- Hyperparameter tuning
- Cross-validation
- Feature importance analysis
- Better imbalance handling
- Trying boosting algorithms

