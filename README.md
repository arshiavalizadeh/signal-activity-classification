# Signal Activity Classification (UCI HAR)

Time-series classification on smartphone inertial signals (accelerometer/gyroscope) using the UCI Human Activity Recognition dataset.

## Goal
Build a clean baseline + reproducible pipeline (metrics, confusion matrix, saved results), then improve via simple feature engineering (windowing, time-domain stats, FFT features).
## Baseline (Logistic Regression)
- Accuracy: 0.9606
- Macro F1: 0.9605

Most common confusion: SITTING vs STANDING.

## Setup
Recommended conda env: `har` (Python 3.12)

Install dependencies:
```bash
pip install -r requirements.txt
git status
git log --oneline -n 3
