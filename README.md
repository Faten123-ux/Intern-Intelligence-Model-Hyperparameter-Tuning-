# Intern-Intelligence-Model-Hyperparameter-Tuning-
Model Hyperparameter Tuning 💻 

(Hyperparameter Tuning and Feature Selection on the Breast Cancer Dataset)



This Task Hyperparameter tuning and feature selection are essential steps in optimizing machine learning models for accuracy and efficiency. We performed feature selection on the Breast Cancer dataset to retain the most relevant features before applying hyperparameter tuning. The primary goal was to improve model performance while reducing computational complexity.

1-BACKGROUND: 



📍 Hyperparameter Tuning: is the practice of identifying and selecting the optimal hyperparameters for use in training a machine learning model. When performed correctly, hyperparameter tuning minimizes the loss function of a machine learning model.



2. Dataset Overview:

- Dataset Used: Breast Cancer dataset from Scikit-Learn.

- Number of Samples: 569.

- Target Variable: Binary classification (Malignant = 0, Benign = 1).

- Missing Values: None (all features are complete).



3. Feature Selection Methods:  We applied multiple feature selection techniques to identify the most important features:

📍Random Forest Feature Importance: Ranked features based on their contribution to model predictions.

📍Mutual Information (MI): Evaluated the statistical dependency between features and the target variable.

📍Recursive Feature Elimination (RFE): Selected the top 10 most influential features based on logistic regression.



Selected Features: ['mean radius', 'mean texture', 'mean perimeter', 'mean area', 'worst radius', 'worst texture', 'worst perimeter', 'worst area', 'mean concavity', 'worst concavity']



4. Feature Correlation Analysis To understand relationships between features, we computed the correlation matrix. The heatmap visualization showed that:

📍Highly correlated features include 'mean radius' and 'mean perimeter' due to their dependency on tumor size.



5. Outlier Detection We used boxplots to analyze outliers:

📍Several features such as 'worst area' and 'mean concavity' contained significant outliers.

📍Outliers were retained as they may contain important information related to malignant tumors.



6. Hyperparameter Tuning Methods After selecting the best features, we performed hyperparameter tuning on two models:

📍 Random Forest Classifier using Grid Search and Random Search.

📍XGBoost Classifier using Bayesian Optimization with Optuna.



7-Comparison of Performance Before and After Feature Selection

📍Baseline Accuracy (All Features): 94.5%

📍Optimized Model Accuracy (Selected Features + Hyperparameter Tuning): 97.3%



Best Tuning Method: Optuna's Bayesian Optimization provided the highest accuracy.v
