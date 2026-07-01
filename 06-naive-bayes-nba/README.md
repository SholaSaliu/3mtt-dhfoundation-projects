# NBA Player Longevity Prediction Project Overview

## 1. Project Overview
This project aims to build a predictive model to identify NBA players likely to have a career spanning 5 years or more, based on their initial season statistics. We utilized a Gaussian Naive Bayes classifier for this task. The goal is to provide insights for scouting decisions by predicting player longevity and understanding the contributing factors.

## 2. Data
The dataset comprises initial season statistics for NBA players. The target variable, `'target_5yrs'`, indicates whether a player had a long career (1 for 5+ years, 0 for less than 5 years).

## 3. Methodology
1.  **Data Loading**: The `extracted_nba_players_data.csv` dataset was loaded.
2.  **Preprocessing**: 
    *   Features (X) and target (y) were separated.
    *   Missing values were checked (none found).
    *   Feature correlation analysis identified highly correlated pairs (e.g., 'ast' - 'stl', 'ast' - 'tov', 'stl' - 'tov', 'tov' - 'total_points').
3.  **Train-Test Split**: The data was split into training and testing sets (80% train, 20% test) using `stratify=y` to maintain the target variable's distribution.
4.  **Model Training**: A Gaussian Naive Bayes classifier was initialized and trained on the training data.
5.  **Prediction**: Predictions (`y_pred`) and probabilities (`y_pred_proba`) were made on the test set.

## 4. Model Performance Evaluation
The Gaussian Naive Bayes model demonstrated the following performance on the test set:

*   **Accuracy**: 0.638
*   **Precision**: 0.800 (Minimizes false positives - 'busts')
*   **Recall**: 0.554 (Minimizes false negatives - 'missed talent')

**Confusion Matrix:**
```
[[79 23]
 [74 92]]
```
*   **True Negatives (TN)**: 79 - Correctly identified short careers.
*   **False Positives (FP)**: 23 - Predicted long career, but actually short ('busts'). Costs resources.
*   **False Negatives (FN)**: 74 - Predicted short career, but actually long ('missed talent'). Lost opportunity.
*   **True Positives (TP)**: 92 - Correctly identified long careers.

## 5. Feature Importance
Based on the absolute difference in class means (mean for short career vs. mean for long career), the most influential features are:

*   total_points: 277.846
*   fg: 2.774
*   ft: 2.242
*   reb: 1.322
*   ast: 0.564
*   tov: 0.432
*   3p: 0.392
*   stl: 0.208
*   blk: 0.192
*   efficiency: 0.038

## 6. Model Reliability and Limitations

**STRENGTHS:**
*   **Precision of 0.800** means 80.0% of predicted long careers are correct.
*   **Recall of 0.554** means the model correctly identifies 55.4% of all players who actually go on to have long careers.
*   **Simplicity and Speed**: Gaussian Naive Bayes is computationally efficient and simple to implement, making it a good baseline model.

**LIMITATIONS:**
*   **Independence Assumption**: The core assumption of feature independence is often violated in basketball statistics, where features are inherently correlated (e.g., points and minutes). This can lead to suboptimal performance compared to models that can handle correlations better.
*   **Bias-Variance Trade-off**: Naive Bayes is a high-bias, low-variance model, potentially oversimplifying complex relationships.
*   **Sensitivity to Data Distribution**: The 'Gaussian' assumption requires features to be normally distributed; deviations can affect performance.

**CONCLUSION:**
The Gaussian Naive Bayes model provides a quick and interpretable baseline for predicting NBA player longevity. While offering valuable insights into key predictive features and acceptable precision/recall, its underlying assumptions suggest that more sophisticated models might be necessary for higher predictive accuracy, especially with highly correlated features. Future improvements could involve feature engineering, advanced classification algorithms (e.g., Logistic Regression, Random Forest, and robust cross-validation techniques.
