# Loan Default Prediction — Credit Risk Analysis

## Objective
Binary classification model to predict loan approval outcomes and identify 
key credit risk factors relevant to lending decisions.

## Business Context
False positives (approving bad borrowers) directly cause default losses 
for lenders. This model minimises that risk while maintaining approval 
accuracy for creditworthy applicants.

## Models Used
| Model | Accuracy |
|---|---|
| Logistic Regression | 78.86% ✅ Selected |
| Random Forest | 75.61% (used for feature importance) |

## Key Findings
- Credit History (26.3%) is the single strongest predictor of loan default
- Applicant Income (20.3%) and Loan Amount (18.5%) follow closely
- Top 4 variables account for 76% of prediction weight
- Demographic variables (Gender, Education) showed near-zero importance — 
  confirming ethical, non-discriminatory model behaviour

## Business Interpretation
| Error Type | What it means | Cost to lender |
|---|---|---|
| False Positive (25) | Approved a defaulter | Direct financial loss |
| False Negative (1) | Rejected good borrower | Lost interest revenue |

Logistic Regression selected over Random Forest because it produced only 
1 false negative vs 5 — making it safer for real credit decision making.

Income variables combined (31.7%) map directly to DSCR logic used in 
professional credit underwriting. Credit History aligns with bureau-based 
risk scoring used by banks like OakNorth.

## Tools & Libraries
Python, Google Colab, pandas, numpy, scikit-learn, matplotlib, seaborn

## Dataset
Loan Prediction Dataset — Kaggle  
614 records, 12 features, binary classification (Loan Approved: Y/N)

## Project Structure
- `loan_default_prediction.ipynb` — Full code and analysis
- `train.csv` — Dataset used
