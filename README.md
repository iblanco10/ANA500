# ANA500
# Workout Calorie Burn Analysis

This project explores the relationship between workout characteristics and calorie burn using machine learning regression techniques. The analysis helps predict whether a workout session will result in high or low-calorie burns based on factors like session duration, workout type, and personal physical attributes.

---

## **Project Overview**
The project aims to:
- Analyze workout characteristics (e.g., session duration, workout type, body composition).
- Use machine learning models to predict high or low-calorie burns.
- Evaluate models based on performance metrics like F1 Score and AUC.

---

## **Data Preparation**
The dataset underwent the following steps:
- **Outlier Removal**: Handled to ensure data quality.
- **Scaling and Encoding**: Continuous features were scaled, and categorical features were encoded.
- **Train-Test Split**: An 80/20 split was used to train and test the models.

---

## **Machine Learning Models**
The following models were tested:
1. **Logistic Regression**:
   - High interpretability.
   - Strong overall performance.
2. **SVM (Linear Kernel)**:
   - Best-performing model with high F1 Score and AUC.
3. **SVM (RBF Kernel)**:
   - Struggled to distinguish between classes.
4. **Decision Tree**:
   - Performed well but less robust than SVM Linear Kernel.

---

## **Evaluation Metrics**
- **F1 Score**: Chosen as the primary metric to balance precision and recall.
- **AUC (Area Under the Curve)**: Used to evaluate overall model discrimination ability.
- **Accuracy, Precision, and Recall** were also calculated for additional insights.

---

## **Key Results**
| Model                  | Accuracy | Precision | Recall | F1 Score | AUC  |
|------------------------|----------|-----------|--------|----------|------|
| Logistic Regression    | 0.856    | 0.824     | 0.862  | 0.843    | 0.946 |
| SVM Linear Kernel      | 0.867    | 0.821     | 0.897  | 0.857    | 0.944 |
| SVM RBF Kernel         | 0.733    | 0.746     | 0.609  | 0.671    | 0.784 |
| Decision Tree          | 0.872    | 0.837     | 0.885  | 0.860    | 0.918 |

**Final Model**: The **SVM Linear Kernel** was chosen as the best model for its balance of high F1 Score (0.857) and AUC (0.944).
---

## **Visualizations**
The project includes:
1. **ROC Curves**: Compare model performance in terms of AUC.
2. **Confusion Matrices**: Evaluate prediction accuracy and errors for each model.

---

## **Technologies Used**
- **Python Libraries**:
  - `scikit-learn` for machine learning.
  - `pandas` and `numpy` for data handling.
  - `matplotlib` for visualizations.

