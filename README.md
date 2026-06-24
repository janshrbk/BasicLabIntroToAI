---Random Forest Algorithm---

Overview:
This project analyzes the relationship between student phone usage habits, social 
media engagement, and academic performance. It uses a Random Forest Classifier to 
predict student addiction levels based on various behavioral metrics.

Methodology & Algorithm Pipeline: 
Our machine learning pipeline follows a strict, reproducible process to ensure data integrity and model accuracy:

*Data Cleaning & Preparation: The dataset is loaded and immediately purged of rows missing the target 
variable (addiction_level), as supervised models cannot train without ground-truth labels. 
    -Irrelevant features (such as age) that do not contribute to behavioral patterns are dropped

*Train/Test Split: The data is separated into input features (X) and target labels (y).
    -It is then split into a Training Set (80%) and a Testing Set (20%) using a fixed random state. This ensures the model's 
    final evaluation is strictly on unseen data.

*Missing Value Imputation: Instead of dropping rows with missing feature data, we employ scikit-learn's SimpleImputer(strategy='mean').

*Model Training: A RandomForestClassifier is initialized. This ensemble algorithm builds 
hundreds of decision trees using random subsets of the data and features, making it highly 
robust against overfitting and capable of capturing complex, non-linear behavioral thresholds.

*Evaluation & Visual Insights: The trained model makes predictions on the unseen Test Set.
    -Performance is evaluated using a Confusion Matrix and a classification report (Accuracy, Precision, Recall). Finally, 
    the algorithm outputs Feature Importance metrics to identify which specific behaviors most heavily influence addiction levels.


***How to Run the Code and Reproduce Results***

*To reproduce our exact results:
    -Open your terminal and ensure you are in the project folder.
    -Run the training script: "python random_forest_training.py"



