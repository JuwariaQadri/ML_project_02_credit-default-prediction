# Project 02 — Credit Default Prediction

Binary classification project to predict loan default with highly imbalanced data.

## Models
- Baseline: Logistic Regression (class-weighted)
- Improved: Gradient Boosting

## Evaluation
- F1-score
- ROC-AUC
- Threshold tuning for business decisions

## Results
See `reports/metrics.json` for final metrics.

## Key Insight
Accuracy is misleading for imbalanced data — Use F1 and ROC-AUC to better capture model quality.


## Getting Started

### 1. Install Dependencies

```bash
pip install -r requirements.txt
```

### 2. Training the baseline model (Logistic regression)

```bash
python -m src.train --model_type logreg
```
### 3. Evaluating the baseline model (Logistic regression)

```bash
python -m src.evaluate --model_path models/logreg_model.joblib
```
### 4. Training the competitor model (Gradient Boosting)

```bash
python -m src.train --model_type gb
```

### 5. Evaluating the competitor model (Gradient Boosting)

```bash
python -m src.evaluate --model_path models/gb_model.joblib
```