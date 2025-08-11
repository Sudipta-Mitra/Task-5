# Task-5
# Heart Disease Prediction using Machine Learning

# Project Overview
This project uses machine learning to predict heart disease from a dataset of 1025 patient records, each with 14 clinical features such as age, cholesterol, and blood pressure. The goal is to classify patients as having heart disease (represented by a target value of 1) or not having heart disease (target value of 0). The project focuses on two key classification algorithms: Decision Trees and Random Forests.
# Methodology
The project followed a clear and structured workflow:
 * Data Preparation: The dataset was loaded and inspected for quality. No missing values were found, ensuring a clean foundation for model training.
 * Decision Tree Analysis: A DecisionTreeClassifier was trained to understand its performance and limitations. The impact of overfitting was explored by systematically varying the max_depth parameter from 1 to 20. The training and test accuracy were plotted against tree depth to visualize this effect, showing how the model's performance on unseen data peaks before it begins to memorize the training data.
 * Random Forest Modeling: To overcome the limitations of a single decision tree, a RandomForestClassifier with 100 trees was trained. This ensemble method significantly improved predictive power, achieving a test accuracy of 98.5%. A key observation was the perfect training accuracy (100%), which is common in Random Forests but makes robust evaluation methods like cross-validation even more critical.
 * Feature Importance: The trained Random Forest model was used to determine which features were most influential in the predictions. A ranking of feature importance was generated and visualized using a bar plot, providing insight into the clinical factors most associated with heart disease in this dataset.
 * Cross-Validation: To ensure the model's performance was not due to a lucky data split, a 5-fold cross-validation was performed. This process involved training and testing the model on different subsets of the data five times. The results confirmed the model's reliability, yielding a mean accuracy of 99.7% with a low standard deviation of 0.0058, indicating high consistency.
# Results and Techniques
| Model | Training Accuracy | Test Accuracy | Cross-Validation Mean Accuracy |
|---|---|---|---|
| Decision Tree | Varies with depth | Peaks around 85–90% | Not performed |
| Random Forest | 100% | 98.5% | 99.7% |
# This project leveraged several fundamental machine learning concepts:
 * Ensemble Learning: By combining multiple decision trees, the Random Forest model demonstrated superior performance and stability.
 * Overfitting Analysis: By plotting accuracy against model complexity (tree depth), the project visually demonstrated the trade-off between a model's ability to learn and its tendency to overfit.
 * Model Interpretation: Feature importance provided a way to understand the model's internal logic and identify key predictors.
 * Robust Evaluation: The use of k-fold cross-validation provided a more reliable estimate of the model's performance on new data.
The entire analysis was conducted using Python, with key libraries including Scikit-learn for modeling, Pandas and NumPy for data handling, and Matplotlib and Seaborn for visualization.
