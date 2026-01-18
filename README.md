# Predictive Maintenance for Aircraft Engines (NASA C-MAPSS)

This project builds a multi-class classification model to predict **when an aircraft engine needs maintenance**

## Problem Framing
RUL was converted into 4 maintenance classes:
- **Healthy** (>60 cycles)
- **Soon** (31–60 cycles)
- **Warning** (16–30 cycles)
- **Critical** (0–15 cycles)

## Key Steps
- Engine-level train/validation split to prevent data leakage
- Temporal feature engineering: rolling mean/std (window=5) + deltas
- Random Forest classifier with explainability via feature importance

## Results (Validation)
- Accuracy: ~85%
- Healthy recall: ~97%
- Critical recall: ~88%
- Near-zero “Critical → Healthy” errors

## Outputs
![Feature Importance](outputs/maintenance_feature_importance.png)

## How to Run
1. Install requirements:
```bash
pip install -r requirements.txt
