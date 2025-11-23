# Bank Marketing — Modelling in Python

<p align="center">
  <img src="reports/BankMarketing_Lab_overview.png" alt="Model comparison overview" width="720">
</p>

Binary classification on the Portuguese bank marketing dataset. I built and compared **Logistic Regression (baseline)** vs **Weighted Logistic Regression** with simple, interpretable features. The weighted model significantly improved recall on the minority class (term-deposit **Yes**).

## TL;DR (Results)
- **Baseline Logistic Regression:** Accuracy ≈ **0.900**, Precision (Yes) **0.67**, Recall (Yes) **0.22**, F1 (Yes) **0.33**.  
- **Weighted Logistic Regression:** Accuracy ≈ **0.833**, Precision (Yes) **0.36**, Recall (Yes) **0.64**, F1 (Yes) **0.47**.  
- **Business take:** Higher recall matters more than a small drop in accuracy for marketing outreach, so the **weighted model** is preferred.

## Why weighted?
The dataset is imbalanced (~11% subscribed). Reweighting (`class_weight='balanced'`) reduces **false negatives** (missed true subscribers) at the cost of more **false positives**, which is acceptable for outreach.

## Repository Structure
- `notebooks/` → `01_bank_marketing_models.ipynb`  
- `reports/` → project PDF + `BankMarketing_lab_overview.png`  
- `data/` → `README.md` (no raw data committed)  
- `requirements.txt`, `LICENSE`, `README.md`

## Dataset

Source: [UCI Machine Learning Repository — Bank Marketing](https://archive.ics.uci.edu/dataset/222/bank+marketing)

**Citation:**  
Moro, S., Cortez, P., & Rita, P. (2014). A data-driven approach to predict the success of bank telemarketing. *Decision Support Systems, 62*, 22–31.

**Files used (locally, not committed):**  
`bank-full.csv` (or a subset). Place the CSV(s) in `data/` before running the notebook.



## Reproduce Locally
```bash
# 1) create & activate a venv (Windows)
python -m venv .venv
.venv\Scripts\activate

# 2) install deps
pip install -r requirements.txt

# 3) run
jupyter notebook
# open notebooks/01_bank_marketing_models.ipynb
