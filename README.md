# Classification Model Benchmarking

A systematic comparison of **14 classification algorithms** on a synthetic dataset, evaluating accuracy, precision, recall, and confusion matrices to identify the best model for different business objectives.

## Overview

This project takes a systematic approach to model selection, evaluating which classifier is best suited for a given problem rather than defaulting to a single algorithm. It generates a synthetic binary classification dataset and runs a full benchmarking pipeline across a diverse set of ML models.

## Classifiers Benchmarked

| Category | Models |
|----------|--------|
| Ensemble | Random Forest, Gradient Boosting |
| Neural | MLP Classifier |
| Kernel | SVM (RBF), Gaussian Process |
| Distance | K-Nearest Neighbours |
| Tree | Decision Tree |
| *...and more* | 14 total |

## Dataset

- **Type:** Synthetic (generated via `sklearn.datasets.make_classification`)
- **Samples:** 1,000
- **Features:** 5
- **Classes:** 2 (binary)
- **Random state:** 1 (reproducible)

## What This Project Covers

- Synthetic dataset generation with controlled complexity
- Full preprocessing and feature scaling pipeline
- Training 14 classifiers with consistent train/test splits
- Evaluation using accuracy, precision, recall, and confusion matrices
- Performance trade-off analysis for business objective alignment

## Tech Stack

| Tool | Purpose |
|------|---------|
| Python | Core language |
| scikit-learn | All classifiers + evaluation metrics |
| Pandas | Results aggregation |
| Matplotlib | Visualisation of results |

## Key Findings

- Ensemble methods (Gradient Boosting, Random Forest) consistently outperform simpler models
- No single model is optimal across all metrics; the right choice depends on whether minimising false positives or false negatives matters more
- MLP Classifier performs competitively but requires more tuning

## How to Run

```bash
git clone https://github.com/MbongeniThwala-projects/classification-model-benchmarking.git
cd classification-model-benchmarking

pip install scikit-learn pandas numpy matplotlib

jupyter notebook Comparing_Different_Classification_Models.ipynb
```

## Key Learnings

- Benchmarking multiple models is essential before committing to a production solution
- Precision vs. recall trade-offs must be framed in terms of business cost (e.g., false negative in healthcare vs. false positive in spam detection)
