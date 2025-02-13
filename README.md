# Diabetes Prediction and Classification using Machine Learning with PySpark

## Project Overview
This project focuses on predicting and classifying diabetes and related conditions using machine learning models on a structured health dataset. It involves preprocessing the data, applying multiple classification algorithms, and evaluating their performance based on accuracy, precision, recall, F1 score, and specificity.

## Objective
The primary goal is to enhance diabetes prediction and classification by comparing various machine learning models. Each model is implemented by different team members:
- **Varshitha**: Random Forest
- **Saketha**: K-Nearest Neighbors (KNN)
- **Karunakar**: Logistic Regression

The models are analyzed to identify the one that delivers the best predictive accuracy, effectively handles complexity, and ensures high specificity.

## Data Preprocessing
To ensure the dataset is ready for machine learning, the following preprocessing steps were performed:
- **Handling Missing Values**: Missing numerical values were replaced with the median.
- **Column Name Normalization**: Spaces were removed from column names for consistency.
- **Label Encoding**: Categorical labels were converted into numerical form using label encoding for compatibility with machine learning models.
- **Feature Vector Assembly**: Numeric features were consolidated into a single vector column using `VectorAssembler` to streamline Spark ML pipeline integration.

## Methods and Models
### Logistic Regression (Karunakar)
- A linear model used for binary classification.
- Configured to run for 10 iterations.

### K-Nearest Neighbors (KNN) (Saketha)
- Classifies data points based on proximity to neighboring points.
- Implemented using Scikit-Learn.

### Random Forest (Varshitha)
- An ensemble learning method that builds multiple decision trees.
- Enhances accuracy while reducing overfitting.

## Evaluation Metrics
The models were assessed using the following metrics:
- **Accuracy**: Proportion of correct predictions.
- **Precision**: Ratio of true positives to total predicted positives.
- **Recall**: Ratio of true positives to actual positives.
- **F1 Score**: Harmonic mean of precision and recall.
- **Specificity**: True negative rate for each class.
- **AUC (for binary classification)**: Measures model sensitivity and specificity.

## Results
The **Random Forest model** emerged as the most effective classifier, achieving:
- **Accuracy**: 80.74%
- **Precision**: 83.28%
- **Recall**: 80.74%
- **Specificity**: ~99.99%

The **Logistic Regression model** demonstrated moderate performance with ~64.17% in accuracy, precision, and recall. The **K-Nearest Neighbors model** achieved **69.58% accuracy** but required significant computational resources.

Overall, Random Forest was the most robust and accurate model, making it the optimal choice for diabetes classification.

## Conclusion
This project underscores the importance of evaluating multiple machine learning models for healthcare predictions. The **Random Forest model** was the best performer, particularly due to its high specificity, making it a reliable tool for identifying negative diabetes cases. Future work may involve testing additional models and incorporating feature engineering to enhance prediction capabilities further.

