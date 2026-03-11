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
## Week 2: Reproducible Pipeline, SQLite Tracking, and Benchmarking

In week 2, I extended the project from a simple baseline notebook to a reproducible experimentation pipeline. I added:
- a cleaner load/train/evaluate workflow
- SQLite-based experiment logging
- model benchmarking with training time, inference time, and estimated model size
- comparison of Logistic Regression and Random Forest variants

Main result:
Logistic Regression achieved the best overall performance-cost trade-off on the UCI HAR dataset. It outperformed the tested Random Forest models in both accuracy/macro-F1 and efficiency metrics.

### Key Results
- Logistic Regression: Accuracy ≈ 0.9606, Macro-F1 ≈ 0.9606
- Random Forest baseline: Accuracy ≈ 0.9291, Macro-F1 ≈ 0.9275
- Random Forest small: Accuracy ≈ 0.9192, Macro-F1 ≈ 0.9170