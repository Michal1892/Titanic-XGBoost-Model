# Titanic Survival Prediction using XGBoost

This project implements a machine learning pipeline to predict passenger survival on the Titanic using the **XGBoost** (Extreme Gradient Boosting) algorithm. The goal is to achieve high accuracy while maintaining model interpretability.

## 📊 Dataset Overview
The dataset contains several explanatory variables used for prediction:
* **Survived** – Survival status (0 = No, 1 = Yes)
* **PClass** – Ticket class (1st, 2nd, 3rd)
* **Name** – Passenger name
* **Age** – Passenger age
* **Parch** – Number of parents/children on board
* **SibSp** – Number of siblings/spouses on board
* **Ticket** – Ticket number
* **Fare** – Passenger fare
* **Cabin** – Cabin number
* **Embarked** – Port of embarkation

---

## 🛠️ Project Workflow

### 1. Data Preprocessing & Feature Selection
* **Data Cleaning:** Handled missing values and removed non-predictive features (e.g., `Ticket`, `Cabin`, `Name`) to reduce noise.
* **Feature Engineering:** Categorical variables were converted into numerical format using dummy encoding.
* **Train/Test Split:** The dataset was divided into training and testing sets to evaluate the model on unseen data.

### 2. Model Development & Optimization
* **Algorithm:** Built a classification model using **XGBoost**.
* **Hyperparameter Tuning:** Optimized key parameters (such as `learning_rate`, `max_depth`, and `n_estimators`) to improve performance and prevent overfitting.

### 3. Evaluation & Interpretability
The model's performance and decision-making process were analyzed using:
* **Confusion Matrix:** To visualize the balance between True Positives, True Negatives, and misclassifications.
* **SHAP Values (Explainable AI):** Used SHAP summary plots to understand the global impact of each feature. This helps identify which factors (like gender or class) most significantly influenced the model's survival predictions.

---

## 📈 Key Insights from SHAP Analysis
Based on the SHAP summary plot, the following patterns were observed:
1. **Gender (`Sex_male`):** Being male was the strongest negative predictor of survival.
2. **Class (`Pclass_3`):** Traveling in the 3rd class significantly decreased the probability of survival.
3. **Age (`Age_Baby`):** Infants had a high positive impact on survival probability, aligning with historical rescue priorities.

---
 
