# bankmarketing-modelling-in-python

![Overview](reports/BankMarketing_lab_overview.png)

## Overview

This project demonstrates binary classification modeling on the **UCI Bank Marketing dataset**. The analysis compares standard **Logistic Regression** with **Weighted Logistic Regression**, showing how the weighted model improves recall for the minority class ("Yes" - customers who subscribe to a term deposit).

Key findings:
- Standard logistic regression struggles with imbalanced classes
- Weighted logistic regression significantly improves minority class ("Yes") recall
- Trade-offs between precision and recall are explored for business decision-making

## Repository Structure

```
.
├── data/                           # Bank marketing dataset files
├── notebooks/
│   └── 01_bank_marketing_model.ipynb  # Main analysis notebook
├── reports/
│   └── BankMarketing_lab_overview.png # Overview visualization
├── requirements.txt                # Python dependencies
├── LICENSE                         # MIT License
└── README.md                       # This file
```

## Reproduce

To reproduce the analysis on **Windows**:

1. **Create a virtual environment:**
   ```cmd
   python -m venv venv
   venv\Scripts\activate
   ```

2. **Install dependencies:**
   ```cmd
   pip install -r requirements.txt
   ```

3. **Open the notebook:**
   ```cmd
   jupyter notebook notebooks/01_bank_marketing_model.ipynb
   ```

4. Run all cells in the notebook to reproduce the analysis and results.

## Attribution

Dataset: [UCI Bank Marketing Data Set](https://archive.ics.uci.edu/ml/datasets/Bank+Marketing)

**Citation:**
> [Moro et al., 2014] S. Moro, P. Cortez and P. Rita. A Data-Driven Approach to Predict the Success of Bank Telemarketing. Decision Support Systems, Elsevier, 62:22-31, June 2014.
