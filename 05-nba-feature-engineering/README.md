# Project 5: NBA Feature Engineering

## 📌 Overview

This project aims to predict the longevity of NBA players in the league, specifically whether a player will last at least 5 years. This is a supervised machine learning task where player statistics are analyzed through comprehensive feature engineering and correlation analysis.

---

## 🎯 Learning Objectives

- Understand feature engineering principles and techniques
- Perform correlation analysis to identify relationships between features
- Handle multicollinearity in datasets
- Create composite features for improved model performance
- Clean and preprocess data for machine learning
- Conduct exploratory data analysis (EDA)

---

## 📊 Dataset

- **Source:** nba-players.csv
- **Size:** NBA player statistics with multiple performance metrics
- **Features:** Games played, minutes, points, rebounds, assists, and various other performance metrics
- **Target Variable:** target_5yrs (whether a player lasts 5+ years in the league)
- **Task Type:** Binary classification

---

## 🔧 Technologies & Libraries

- Python 3.x
- Pandas - Data manipulation and analysis
- NumPy - Numerical computing
- scikit-learn - Preprocessing and modeling
- Matplotlib/Seaborn - Visualization
- Jupyter Notebook - Analysis environment

---

## 📂 Project Structure

```
05-nba-feature-engineering/
├── README.md (this file)
├── notebooks/
│   └── nba_feature_engineering.ipynb
├── nba_feature_engineering.ipynb.pdf (Analysis report)
├── data/
│   ├── raw/
│   │   └── nba-players.csv
│   └── processed/
│       └── cleaned_data.csv
└── requirements.txt
```

---

## 🚀 How to Run

1. **Navigate to project folder:**
   ```bash
   cd 05-nba-feature-engineering
   ```

2. **Install dependencies:**
   ```bash
   pip install -r requirements.txt
   ```

3. **Open Jupyter Notebook:**
   ```bash
   jupyter notebook notebooks/nba_feature_engineering.ipynb
   ```

---

## 📈 Key Findings

### Dataset Overview
- The dataset contains various statistical measures for NBA players
- Each row represents a player with performance metrics as features
- Target variable explicitly defined: target_5yrs

### Feature Engineering Steps Performed

1. **Target Variable Definition:** Explicitly defined target_5yrs as the dependent variable

2. **Dropping Non-Predictive Columns:** 
   - Removed Unnamed: 0 (artifact)
   - Removed name (player's name - no predictive power)

3. **Correlation Analysis:**
   - Generated comprehensive correlation matrix
   - Visualized relationships between features and target variable
   - Identified strongly correlated features

4. **Creating New Composite Features:**
   - Engineered `ppm` (Points Per Minute) = pts / min
   - Provides normalized measure of scoring efficiency
   - Handles potential differences in playing time

5. **Multicollinearity Handling:**
   - Dropped highly correlated features: fgm, fga, fta, dreb, 3pa
   - Reduced redundancy while preserving predictive power

6. **Data Cleaning:**
   - Thoroughly checked for missing values
   - Confirmed no nulls present in performance columns
   - Clean dataset ready for modeling

---

## 💡 Key Learnings

- Feature engineering is critical for model performance
- Correlation analysis helps identify redundant features
- Multicollinearity can negatively impact model interpretability
- Creating composite features can capture domain knowledge
- Data quality checks are essential before modeling

---

## 🔮 Next Steps

1. Split data into training and testing sets
2. Explore various ML models (Logistic Regression, Decision Trees, Random Forests, Gradient Boosting)
3. Train and evaluate models using appropriate metrics (accuracy, precision, recall, F1-score, ROC-AUC)
4. Perform hyperparameter tuning for optimized performance
5. Interpret results and identify most influential features

---

## 📚 Resources & References

- Pandas Documentation: https://pandas.pydata.org/
- scikit-learn Documentation: https://scikit-learn.org/
- Feature Engineering Best Practices
- Correlation Analysis Techniques

---

## 📝 Author

**Name:** Shola Saliu  
**Program:** 3MTT DHFoundation  
**Date Completed:** July 2026

---

**Files:**
- 📓 Jupyter Notebook: `notebooks/nba_feature_engineering.ipynb`
- 📄 PDF Report: `nba_feature_engineering.ipynb.pdf`
- 📊 Data: `data/`

**GitHub:** [Original Repository](https://github.com/SholaSaliu/nba_feature_engineering_project)
