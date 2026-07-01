# Project 6: Naive Bayes NBA Classification

## 📌 Overview

This project implements Naive Bayes classification to predict NBA player longevity. Building on the feature engineering work from Project 5, this project focuses on training and evaluating a Naive Bayes classifier to determine whether a player will last at least 5 years in the league.

---

## 🎯 Learning Objectives

- Understand Naive Bayes algorithm and its assumptions
- Implement Naive Bayes classifier using scikit-learn
- Compare Naive Bayes with other classification algorithms
- Evaluate classification performance using multiple metrics
- Interpret model predictions and feature importance
- Handle probabilistic predictions

---

## 📊 Dataset

- **Source:** nba-players.csv (cleaned and engineered from Project 5)
- **Size:** NBA player statistics with engineered features
- **Features:** Performance metrics including Points Per Minute (ppm) and other selected features
- **Target Variable:** target_5yrs (binary: 1 = lasts 5+ years, 0 = does not)
- **Task Type:** Binary classification

---

## 🔧 Technologies & Libraries

- Python 3.x
- Pandas - Data manipulation
- NumPy - Numerical computing
- scikit-learn - Naive Bayes and model evaluation
- Matplotlib/Seaborn - Visualization
- Jupyter Notebook - Analysis environment

---

## 📂 Project Structure

```
06-naive-bayes-nba/
├── README.md (this file)
├── notebooks/
│   └── naive_bayes_classification.ipynb
├── data/
│   ├── raw/
│   │   └── nba-players.csv
│   └── processed/
│       └── engineered_features.csv
├── outputs/
│   ├── naive_bayes_report.pdf
│   └── visualizations/
│       ├── confusion_matrix.png
│       ├── roc_curve.png
│       └── feature_importance.png
└── requirements.txt
```

---

## 🚀 How to Run

1. **Navigate to project folder:**
   ```bash
   cd 06-naive-bayes-nba
   ```

2. **Install dependencies:**
   ```bash
   pip install -r requirements.txt
   ```

3. **Open Jupyter Notebook:**
   ```bash
   jupyter notebook notebooks/naive_bayes_classification.ipynb
   ```

---

## 📈 Key Concepts

### Naive Bayes Algorithm
- Probabilistic classifier based on Bayes' theorem
- Assumes conditional independence of features
- Fast and efficient for classification tasks
- Works well with both continuous and categorical data

### Classification Approach
1. Data preparation and feature scaling
2. Train-test split
3. Model training (Gaussian Naive Bayes)
4. Model evaluation using multiple metrics
5. Hyperparameter tuning if applicable
6. Comparison with baseline models

---

## 📊 Model Performance

### Expected Metrics
- Accuracy: [To be calculated]
- Precision: [To be calculated]
- Recall: [To be calculated]
- F1-Score: [To be calculated]
- ROC-AUC: [To be calculated]

### Comparison Metrics
- Compare with other algorithms (Logistic Regression, Decision Trees, Random Forests)
- Analyze trade-offs between precision and recall
- Evaluate on test set performance

---

## 💡 Key Learnings

- Naive Bayes is effective for quick, interpretable classifications
- Understanding conditional independence assumptions
- Importance of feature scaling for certain algorithms
- Evaluating probabilistic predictions
- When to use Naive Bayes vs. other classifiers

---

## 🔮 Future Improvements

1. Implement other Naive Bayes variants (Multinomial, Bernoulli)
2. Feature selection and optimization
3. Ensemble methods combining Naive Bayes with other algorithms
4. Cross-validation for more robust evaluation
5. Class imbalance handling techniques

---

## 📚 Resources & References

- scikit-learn Naive Bayes: https://scikit-learn.org/stable/modules/naive_bayes.html
- Bayes' Theorem and Probability
- Classification metrics and evaluation
- Feature engineering best practices

---

## 📝 Author

**Name:** Shola Saliu  
**Program:** 3MTT DHFoundation  
**Date Started:** July 2026

---

**Files:**
- 📓 Jupyter Notebook: `notebooks/naive_bayes_classification.ipynb`
- 📄 PDF Report: `outputs/naive_bayes_report.pdf`
- 📊 Data: `data/`
