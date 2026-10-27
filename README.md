# Machine Learning Notebooks

This repository contains exploratory data analysis and classification workflows for two datasets:

- **Online Shoppers Purchasing Intention** — predicts whether a browsing session results in a purchase (`Revenue`).
- **Credit Card Fraud 2023** — explores transaction features and the binary fraud label (`Class`).

## Repository contents

```text
.
├── datasets/
│   ├── online_shoppers_intention.csv
│   └── creditcard_2023.csv
├── ML_online_shopping-tendancy.ipynb
├── ML_learn2.ipynb
├── requirements.txt
└── README.md
```

The datasets are not included in this repository. Download them from their sources and place the CSV files in `datasets/` using the filenames above.

## Notebooks

### Online shoppers

Open `ML_online_shopping-tendancy.ipynb` to:

- inspect and prepare the online-shopping data;
- explore numeric feature distributions and correlations with `Revenue`;
- create fixed-seed, stratified 70% training, 15% validation, and 15% test splits;
- train logistic regression and random forest models using preprocessing pipelines; and
- compare validation accuracy, precision, F1, and ROC AUC, with ROC curves and confusion matrices.

The model comparison uses the training and validation sets only. Keep the test set untouched until model selection is complete.



## Setup

Requirements: Python 3.11 or later, Git, and Visual Studio Code with the Python and Jupyter extensions.

1. Clone the repository and change into its directory:

   ```bash
   git clone https://github.com/mincemeat7303/scaling-octo-happiness.git
   cd scaling-octo-happiness
   ```

2. Create and activate a virtual environment:

   **Windows PowerShell**

   ```powershell
   py -m venv .venv
   .\.venv\Scripts\Activate.ps1
   ```

   **macOS/Linux**

   ```bash
   python3 -m venv .venv
   source .venv/bin/activate
   ```

3. Install the project dependencies:

   ```bash
   python -m pip install --upgrade pip
   python -m pip install -r requirements.txt
   ```

4. Put the CSV files in the `datasets/` directory, open the desired notebook in VS Code, and select the `.venv` Python environment as its kernel.

5. Run the notebook cells from top to bottom.

## Data sources

- [Online Shoppers Purchasing Intention Dataset](https://archive.ics.uci.edu/dataset/468/online+shoppers+purchasing+intention+dataset) — Sakar and Kastro, UCI Machine Learning Repository (2018), licensed under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/).

