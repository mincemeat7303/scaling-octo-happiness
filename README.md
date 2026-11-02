# Group Members
Lin John(1597422)
Nitha 
Piumi

# Online Shoppers Purchasing Intention Prediction

A machine learning project that predicts whether an online shopping session will result in a purchase (`Revenue = True`) using the UCI Online Shoppers Purchasing Intention Dataset.

## Project Overview

#The project explores customer browsing behaviour through:

#- Exploratory Data Analysis (EDA)
#- Data preprocessing
#- Feature encoding and scaling
#- Binary classification models
#- Hyperparameter tuning
#- Model evaluation
#- Feature Importance Analysis

## Dataset

- **Dataset:** Online Shoppers Purchasing Intention Dataset
- **Source:** UCI Machine Learning Repository
- **Instances:** 12,330
- **Features:** 17 input features and 1 target (`Revenue`)
- **Task:** Binary Classification

Official dataset:
https://archive.ics.uci.edu/dataset/468/online+shoppers+purchasing+intention+dataset

## Project Structure

```text
.
├── datasets/
│   └── online_shoppers_intention.csv
├── ML_online_shopping-tendancy.ipynb
├── README.md
└── requirements.txt
```



## Prerequisites

Install the following software:

- Python 3.11 or later
- Git
- Visual Studio Code 
- VS Code Python extension
- VS Code Jupyter extension

## Setup Instructions

### 1. Clone the repository

```bash
git clone https://github.com/mincemeat7303/scaling-octo-happiness.git
cd ML_online_shopping-tendancy
```


## Environment setup

This project uses a Jupyter notebook and the notebook kernel is based on the local `.venv` environment with Python 3.14.6.

### 1) Create and activate the virtual environment
```bash
python -m venv .venv
.\.venv\Scripts\activate
```

### 4. Install dependencies

```bash
python -m pip install --upgrade pip
python -m pip install -r requirements.txt
```

### 5. Register the Jupyter kernel

```bash
python -m ipykernel install --user --name online-shopper-env --display-name ".venv (3.14.6)"
```

## Dataset Setup

Download the dataset from the UCI repository and place it inside:

```text
datasets/
└── online_shoppers_intention.csv
```






## Models

### Baseline

- Logistic Regression

### Modern Machine Learning

- XGBoost
- LightGBM
- MLP

### Hyperparameter Tuning



## Evaluation Metrics

Model performance may be evaluated using:
Accuracy, Precision, Recall,F1 score and ROC curve


## Troubleshooting

### Python not found

Check that Python is installed:

```bash
python --version
```

### Virtual environment not activating

Use Command Prompt instead of PowerShell if execution policies block activation.

### Missing packages

Run:

```bash
python -m pip install -r requirements.txt
```

## References

Sakar, C., & Kastro, Y. (2018). *Online Shoppers Purchasing Intention Dataset*. UCI Machine Learning Repository.

## Current Notebook Workflow and Results

The notebook prepares the dataset, explores its features, then splits it into stratified training (70%), validation (15%), and test (15%) sets using the shared random state `42`. Preprocessing is included in each scikit-learn model pipeline: numeric features are standardized and categorical features are one-hot encoded. The test set is held out for final evaluation.

The notebook compares Logistic Regression, LightGBM, XGBoost, and an MLP. Precision, recall, and F1 score treat a purchase (`Revenue = True`) as the positive class. The following validation scores are from the current comparison:

| Model | Accuracy | Precision | Recall | F1 score | ROC-AUC |
|---|---:|---:|---:|---:|---:|
| LightGBM | 0.894 | 0.644 | 0.703 | 0.672 | 0.921 |
| XGBoost | 0.881 | 0.592 | 0.745 | 0.659 | 0.927 |
| MLP | 0.865 | 0.548 | 0.713 | 0.620 | 0.902 |
| Logistic Regression | 0.855 | 0.522 | 0.738 | 0.612 | 0.898 |

XGBoost was selected for the final held-out test evaluation:

| Metric | Test score |
|---|---:|
| Accuracy | 0.865 |
| Precision | 0.542 |
| Recall | 0.829 |
| F1 score | 0.656 |
| ROC-AUC | 0.933 |

The notebook also plots XGBoost feature importance in descending order using total gain. One-hot encoded category importances are aggregated to their original feature; the leading features are `PageValues`, `Month`, `ExitRates`, `ProductRelated_Duration`, and `BounceRates`. Feature importance is specific to this fitted model and should not be interpreted as causal effect.
