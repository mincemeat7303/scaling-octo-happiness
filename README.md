# Group Members

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

## Dataset

- **Dataset:** Online Shoppers Purchasing Intention Dataset
- **Source:** UCI Machine Learning Repository
- **Instances:** 12,330
- **Features:** 17 input features and 1 target (`Revenue`)
- **Task:** Binary Classification

Official dataset:
https://archive.ics.uci.edu/dataset/468/online+shoppers+purchasing+intention+dataset

## Project Structure



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




## Typical Workflow

1. Activate the virtual environment.
2. Open VS Code.
3. Select the **Python (Online Shopper)** kernel.
"""4. Run:
  """ - `EDA.ipynb`
   - `preprocessing.ipynb`
   - `model_training.ipynb`"""
"5. Compare baseline and tuned models."""

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
