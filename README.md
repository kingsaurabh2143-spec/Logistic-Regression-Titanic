# Titanic Survival Prediction 🚢

## 1. Project Overview

This project predicts whether a passenger survived the Titanic disaster using machine learning.

The goal is to build a binary classification model using passenger information and evaluate its performance using multiple classification metrics.

## 2. Problem Statement

The task is to predict the `Survived` target variable:

- `0` — Did not survive
- `1` — Survived

This project uses Logistic Regression to learn patterns from historical passenger data.

## 3. Dataset

The dataset comes from the Kaggle Titanic competition.

Dataset source: https://www.kaggle.com/competitions/titanic/data

The training dataset contains passenger information and survival labels. The test dataset contains passenger information without survival labels.

## 4. Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- scikit-learn
- Jupyter Notebook

## 5. Features Used

The model uses the following input features:

- `Pclass`
- `Sex`
- `Age`
- `SibSp`
- `Parch`
- `Fare`
- `Embarked`

The target variable is `Survived`.

## 6. Methodology

The project follows these steps:

1. Load and inspect the dataset.
2. Perform Exploratory Data Analysis (EDA).
3. Select input features and the target variable.
4. Split the training data into training and validation subsets.
5. Handle missing numerical values using median imputation.
6. Handle missing categorical values using most-frequent imputation.
7. Encode categorical features using One-Hot Encoding.
8. Build a preprocessing and classification Pipeline.
9. Train a Logistic Regression model.
10. Evaluate the model using classification metrics and ROC-AUC.
11. Generate predictions for the Kaggle test dataset.
12. Export predictions to `submission.csv`.

The preprocessing transformations are fitted through the Pipeline using the training data, helping prevent data leakage from the held-out validation set.

## 7. Model Evaluation

The model was evaluated on a held-out validation set.

| Metric | Result |
|---|---:|
| Accuracy | 80.45% |
| Precision | 79.31% |
| Recall | 66.67% |
| F1-score | 72.79% |
| ROC-AUC | 0.8443 |

These results represent the local validation performance, not a Kaggle leaderboard score.

## 8. Project Structure

```
Logistic-Regression-Titanic/
├── logistic_regression_titanic.ipynb
├── submission.csv
├── README.md
├── requirements.txt
└── .gitignore
```

The original Kaggle datasets are excluded from version control. Download them from the official competition page before running the notebook.

## 9. How to Run

1. Clone or download this repository.
2. Download `train.csv` and `test.csv` from the Kaggle competition.
3. Place both CSV files in the project directory.
4. Install the required Python dependencies listed in `requirements.txt`.
5. Open `logistic_regression_titanic.ipynb` in Jupyter Notebook or VS Code.
6. Select the appropriate Python environment.
7. Run all notebook cells in order.

## 10. Output

The notebook generates `submission.csv` containing two columns:

- `PassengerId`
- `Survived`

The file follows the required column structure for a Titanic competition submission.

## 11. Limitations and Future Improvements

Potential improvements include:

- Comparing Logistic Regression with other classification algorithms.
- Performing cross-validation.
- Conducting systematic hyperparameter tuning.
- Evaluating alternative feature engineering approaches.

## 12. Author

**Saurabh Chauhan**