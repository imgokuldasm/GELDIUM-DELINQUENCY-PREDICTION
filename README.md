# GELDIUM-DELINQUENCY-PREDICTION
The project aims to predict customer credit delinquency using two models: Logistic
Regression and Random Forest.
Workflow:
1. Data Preprocessing:
- Loaded dataset and explored class imbalance (84% non-delinquent, 16% delinquent).
- Handled missing values and encoded categorical features.
- Scaled features using StandardScaler.
2. Handling Class Imbalance:
- No SMOTE used. Instead, applied class_weight='balanced' for both models to handle
imbalance during training.
3. Model Training:
- Logistic Regression: Used for baseline performance and interpretability.
- Random Forest: Tuned with n_estimators=350, max_depth=5, and balanced class weight.
4. Evaluation:
- Metrics: Accuracy, Confusion Matrix, Precision, Recall, F1 Score, ROC AUC.
- Compared models based on performance and ability to predict the minority class.
- - Metrics Used: Accuracy, Recall, F1 Score, Confusion Matrix, and ROC AUC.
- Interpretation:
- Logistic Regression: Overfit to the majority class (no class 1 predictions).
- Random Forest: Better class balance and recall for minority class.
- Bias Mitigation:
- Used class_weight='balanced' instead of oversampling (e.g., SMOTE).
- Evaluated both class-specific metrics and overall fairness.
- Ethical Considerations:
- Avoided using sensitive or proxy variables (e.g., gender, race).
- Chose interpretable models to meet regulatory needs and explainability standards in
financial institutions.
