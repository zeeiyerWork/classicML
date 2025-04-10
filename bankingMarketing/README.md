# Bank Marketing Campaign Analysis

This project analyzes direct marketing campaign data from a Portuguese bank using a modularized machine learning pipeline. The pipeline includes data preprocessing, model training, evaluation, and logging.

## 📁 Dataset

- **Source**: [UCI Bank Marketing Dataset](https://archive.ics.uci.edu/ml/datasets/Bank+Marketing)
- The dataset represents results from 17 direct phone marketing campaigns (May 2008 to November 2010).

## 🧩 Project Structure

- `FunctionallyModularized_Module17.ipynb`: Main notebook with modular code.
- `logs/`: Directory for storing log files (created during execution).
- Data is loaded from a data directory.
- Both Data/Logs are persisted on google-drive. [so user must edit that location to match theirs]

## ⚙️ Pipeline Overview

### 1. Data Preprocessing

- Impute missing values using `SimpleImputer`
- Standardize numerical features
- One-hot encode categorical features
- Combine preprocessing using `ColumnTransformer`

### 2. Modeling

- Models trained:
  - Logistic Regression
  - K-Nearest Neighbors (KNN)
  - Decision Tree
  - Support Vector Machine (SVC)
- `StratifiedKFold` cross-validation
- Hyperparameter tuning via `GridSearchCV` (except SVM which uses a narrow `RandomizedSearchCV` to restrict search-space/time to compelte).

### 3. Evaluation

- Metrics:
  - Accuracy
  - F1 Score
  - ROC AUC
  - Confusion Matrix
  - Classification Report

### 4. Logging

- Logging setup to capture training durations and metrics
- Logs written to timestamped `.log` files (persisted on Google Drive)

## 🧪 Key Functions

| Function | Arguments | Description |
|----------|-----------|-------------|
| `configureLogging` | logfile | Sets up logging configuration |
| `load_data` | file_path, separator, encoding | Load the dataset from a CSV file |
| `explore_data` | df | Perform initial exploration of the dataset |
| `define_business_objective` | – | Define the business objective of the analysis |
| `prepare_features_and_target` | df, feature_set | Prepare features and target variable for modeling |

## 🚀 How to Run

1. Open `FunctionallyModularized_Module17.ipynb` in Jupyter. 
2. Ensure you have the data file on google drive and the path matches.
2. Load the dataset using `load_data()`.
3. Set up logging with `configureLogging("logname.log")`.
4. Preprocess the dataset and define the model pipeline.
5. Train and evaluate models using modular functions.
6. Review output metrics and logs.

## 📝 Notes

- Ensure all necessary Python packages are installed (`pandas`, `scikit-learn`, `seaborn`, etc.)
- Modify `file_path` when loading data if not in the working directory.

---

