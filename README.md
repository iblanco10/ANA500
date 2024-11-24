# ANA500  
# Workout Calorie Burn Analysis  

This project investigates the relationship between workout characteristics and calorie burn using machine learning and deep learning techniques. The goal is to predict whether a workout session will result in high or low-calorie burns based on factors like session duration, workout type, and personal physical attributes.  

---

## **Project Overview**  
The project aims to:  
- Analyze workout characteristics (e.g., session duration, workout type, body composition).  
- Use machine learning models to predict high or low-calorie burns.  
- Evaluate models based on performance metrics like F1 Score and AUC.  

---

## **Data Preparation**  
The dataset underwent the following steps:  
- **Scaling and Encoding**: Continuous features (e.g., weight, height) were scaled using Min-Max scaling. Categorical features (e.g., gender, workout type) were encoded numerically.  
- **Outlier Analysis**: Outliers were retained as they represented realistic intense workout sessions.  
- **Binary Outcome Variable**: `Calories_Burned` was split at the median into high and low categories for balanced classification.  
- **Train-Test Split**: The data was split 80/20 for training and testing models.  

---

## **Machine Learning Models**  
The following models were tested:  
1. **Logistic Regression**:  
   - High interpretability through feature coefficients.  
   - Strong overall performance.  
2. **SVM (Linear Kernel)**:  
   - Best-performing model with the highest F1 Score and AUC.  
3. **SVM (RBF Kernel)**:  
   - Lower performance, struggled to distinguish between classes.  
4. **Decision Tree**:  
   - Competitive performance but less robust compared to SVM Linear Kernel.  

---

## **Deep Learning Models**  
1. **Feedforward Neural Network (FNN)**:  
   - Captured hidden patterns but underperformed compared to SVM models.  
   - Accuracy: 76%; AUC: 0.84.  
2. **Multilayer Perceptron (MLP)**:  
   - Best deep learning model with an AUC of 0.90 and F1 Score of 0.83.  

---

## **Evaluation Metrics**  
- **F1 Score**: Used to balance precision and recall.  
- **AUC (Area Under the Curve)**: Evaluates the ability to distinguish between high and low-calorie burns.  
- Additional metrics: Accuracy, precision, and recall were calculated for further insights.  

---

## **Key Results**  
| Model                  | Accuracy | Precision | Recall | F1 Score | AUC  |  
|------------------------|----------|-----------|--------|----------|------|  
| Logistic Regression    | 0.856    | 0.824     | 0.862  | 0.843    | 0.946 |  
| SVM Linear Kernel      | 0.867    | 0.821     | 0.897  | 0.857    | 0.944 |  
| SVM RBF Kernel         | 0.733    | 0.746     | 0.609  | 0.671    | 0.784 |  
| Decision Tree          | 0.872    | 0.837     | 0.885  | 0.860    | 0.918 |  

**Final Model**: The **SVM Linear Kernel** was chosen as the best model for its balance of F1 Score (0.857) and AUC (0.944).  

---

## **Visualizations**  
The project includes:  
1. **ROC Curves**: Compare model performance in terms of AUC.  
2. **Confusion Matrices**: Evaluate prediction accuracy and errors.  
3. **Box Plots and Histograms**: Display variable distributions and outliers.  

---

## **Technologies Used**  
- **Python Libraries**:  
  - `scikit-learn` for machine learning.  
  - `pandas` and `numpy` for data handling.  
  - `matplotlib` and `seaborn` for visualizations.  
  - `TensorFlow/Keras` for deep learning models.  

---

## **Conclusion**  
The analysis confirms that session duration and workout type significantly impact calorie burn. The SVM Linear Kernel model was the most effective in predicting high-calorie burns, providing practical insights for optimizing workout plans. This project demonstrates the value of combining machine learning and deep learning techniques for actionable fitness recommendations.  

--- 
