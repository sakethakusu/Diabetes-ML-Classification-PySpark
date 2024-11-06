# Diabetes-ML-Classification-PySpark

Diabetes Prediction and Classification using Machine Learning Models with PySpark

Project Overview

This project aims to predict and classify types of diabetes and related conditions using machine learning models on a structured health dataset. It involves preprocessing the data, implementing various classification algorithms, and evaluating model performance based on multiple metrics, including accuracy, precision, recall, F1 score, and specificity.

Objective

The goal is to leverage machine learning to improve the prediction and classification of diabetes categories. This is achieved through comparing the performance of multiple machine learning models, each implemented by different team members.

Varshitha: Random Forest

Saketha: K-Nearest Neighbors (KNN)

Karunakar: Logistic Regression

The models are evaluated to determine which performs best in terms of predictive accuracy, handling complexity, and achieving high specificity.

Data Preprocessing

Several preprocessing steps were conducted on the dataset to prepare it for machine learning:

Handling Missing Values: Numerical columns with missing values were filled with the median.

Column Name Normalization: Spaces were removed from column names to facilitate handling.

Label Encoding: Categorical labels were converted into numeric form using label encoding, enabling compatibility with machine learning algorithms.

Feature Vector Assembly: Numeric features were assembled into a single vector column using VectorAssembler, allowing streamlined integration into Spark ML pipelines.

Methods and Models

Logistic Regression (Karunakar): A linear model for binary classification, configured for 10 iterations.

K-Nearest Neighbors (KNN) (Saketha): Classifies data points based on proximity to neighbors, implemented with Scikit-Learn.

Random Forest (Varshitha): An ensemble method that constructs multiple decision trees to enhance accuracy and reduce overfitting.

Evaluation Metrics

Accuracy: The proportion of correct predictions.

Precision: The ratio of true positives to total predicted positives.

Recall: The ratio of true positives to actual positives.

F1 Score: The harmonic mean of precision and recall.

Specificity: True negative rate for each class.

AUC (for binary classification): Area Under the Curve to assess model sensitivity and specificity.

Results

The Random Forest model outperformed the other models, achieving high accuracy (80.74%), precision (83.28%), recall (80.74%), and specificity (~99.99%), making it the most suitable for diabetes classification. Logistic Regression showed moderate performance with around 64.17% across accuracy, precision, and recall, while K-Nearest Neighbors reached a reasonable accuracy of 69.58% but was computationally intensive. Overall, Random Forest's high specificity and robustness make it the top choice for this predictive task.

Conclusion
The Random Forest model emerged as the top performer, especially in terms of specificity, making it highly reliable for identifying negative cases in diabetes classification. This project highlights the importance of comparing different models to determine the most effective one for healthcare predictions.
