# Bank Marketing — Modelling in Python

Binary classification on the Portuguese bank marketing dataset. I built and compared **Logistic Regression (baseline)** vs **Weighted Logistic Regression** with simple, interpretable features. The weighted model significantly improved recall on the minority class (term-deposit **Yes**).

![Overview](reports/BankMarketing_lab_overview.png)

## TL;DR (Results)
- **Baseline Logistic Regression:** Accuracy ≈ **0.900**, Precision (Yes) **0.67**, Recall (Yes) **0.22**, F1 (Yes) **0.33**.  
- **Weighted Logistic Regression:** Accuracy ≈ **0.833**, Precision (Yes) **0.36**, Recall (Yes) **0.64**, F1 (Yes) **0.47**.  
- Business take: Higher recall matters more than a small drop in accuracy for marketing outreach, so the **weighted model** is preferred. :contentReference[oaicite:0]{index=0}

## Why weighted?
The dataset is imbalanced (~11% subscribed). Reweighting (`class_weight='balanced'`) reduces **false negatives** (missed true subscribers) at the cost of more **false positives**, which is acceptable for outreach. :contentReference[oaicite:1]{index=1}

## Repository Structure
notebooks/ -> 01_bank_marketing_models.ipynb
reports/ -> BankMarketing_lab_report.pdf, BankMarketing_lab_overview.png
data/ -> README.md (no raw data committed)
requirements.txt
LICENSE
README.md


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
