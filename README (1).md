# ML Lab 5 – K-Nearest Neighbors (KNN) Classification

## Overview

This project implements a **K-Nearest Neighbors (KNN)** classification model to predict whether a person has diabetes using the **Pima Indians Diabetes dataset**.

The notebook covers data loading, exploratory data analysis, preprocessing, feature scaling, KNN model training, evaluation, and cross-validation for selecting a suitable value of **K**.

## Dataset

The dataset is loaded from:

```text
diabetes.csv
```

It contains **768 records** and **9 columns**.

### Features

- Pregnancies
- Glucose
- BloodPressure
- SkinThickness
- Insulin
- BMI
- DiabetesPedigreeFunction
- Age

### Target

- `Outcome`
  - `0` – No Diabetes
  - `1` – Diabetes

## Technologies Used

- Python
- NumPy
- Pandas
- Matplotlib
- Seaborn
- Scikit-learn
- Google Colab / Jupyter Notebook

## Methodology

The notebook follows these main steps:

1. Import the required Python libraries.
2. Load the `diabetes.csv` dataset.
3. Inspect the dataset using functions such as `head()`, `describe()`, and null-value checks.
4. Perform exploratory data analysis and visualization.
5. Separate the input features and target variable.
6. Split the data into training and testing sets.
7. Apply `StandardScaler` for feature scaling.
8. Train a `KNeighborsClassifier`.
9. Generate predictions on the test data.
10. Evaluate the model using:
    - Accuracy
    - Precision
    - Recall
    - F1-score
    - Confusion Matrix
    - Classification Report
11. Perform **5-fold cross-validation** for different values of K.
12. Identify the K value with the highest cross-validation accuracy.

## Model

The machine learning algorithm used is:

**K-Nearest Neighbors (KNN)**

KNN classifies a new data point based on the classes of its nearest neighboring data points.

## Results

For the evaluated KNN model in the notebook:

| Metric | Score |
|---|---:|
| Accuracy | 0.694805 |
| Precision | 0.583333 |
| Recall | 0.509091 |
| F1 Score | 0.543689 |

### Confusion Matrix

```text
[[79 20]
 [27 28]]
```

The classification report in the notebook shows:

| Class | Precision | Recall | F1-score |
|---|---:|---:|---:|
| No Diabetes | 0.75 | 0.80 | 0.77 |
| Diabetes | 0.58 | 0.51 | 0.54 |

### Cross-Validation

A 5-fold cross-validation experiment was performed for K values from **1 to 30**.

The notebook obtained:

- **Best K based on cross-validation: 23**
- **Best cross-validation accuracy: 0.75555**

## Project Structure

```text
ML-Lab5/
│
├── ML_Lab5 (1).ipynb
├── diabetes.csv
└── README.md
```

## How to Run

### Using Google Colab

1. Upload the notebook and `diabetes.csv` to Google Colab.
2. Open `ML_Lab5 (1).ipynb`.
3. Make sure `diabetes.csv` is available in the working directory.
4. Run the notebook cells from top to bottom.

### Using Jupyter Notebook

Install the required libraries:

```bash
pip install numpy pandas matplotlib seaborn scikit-learn
```

Then open the notebook:

```bash
jupyter notebook
```

Run the cells in order.

## Key Learning Outcomes

- Understanding the KNN classification algorithm.
- Performing exploratory data analysis.
- Preparing data for machine learning.
- Using feature scaling with `StandardScaler`.
- Evaluating classification models using multiple metrics.
- Understanding confusion matrices and classification reports.
- Using cross-validation to select an appropriate K value.

## Author

**Shreya Sharma**

B.Tech – Computer Science Engineering (AI & ML)

Ramdeobaba University
