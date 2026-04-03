# Titanic-XGBoost-Model
Titanic Survival Prediction using XGBoost
This project focuses on building a high-performance binary classification model to predict passenger survival on the Titanic. The solution utilizes the XGBoost algorithm, known for its efficiency and predictive power in structured data tasks.

📊 Dataset Overview
The Titanic dataset contains several explanatory variables:

Survived – Survival status (0 = No, 1 = Yes)

PClass – Passenger class (Ticket standard)

Name – Name of the passenger

Age – Age of the passenger

Parch – Number of children or parents on board

SibSp – Number of siblings or spouses on board

Ticket – Ticket number

Fare – Price paid for the ticket

Cabin – Cabin number

Embarked – Port of embarkation (First letter of the city)

🛠️ Project Workflow
1. Data Preprocessing & Feature Selection
Data Cleaning: Handled missing values and removed low-predictive features (such as Ticket or Cabin) to reduce noise.

Feature Engineering: Categorical variables were encoded to be compatible with the gradient boosting algorithm.

Train/Test Split: The dataset was divided into training and testing sets to ensure an unbiased evaluation of the model's performance.

2. Model Development & Hyperparameter Tuning
Algorithm: Implemented XGBoost (Extreme Gradient Boosting).

Optimization: Performed hyperparameter tuning (optimizing learning_rate, max_depth, and n_estimators) to maximize accuracy while preventing overfitting.

3. Evaluation & Explainability
To go beyond simple accuracy metrics, the model was evaluated using:

Confusion Matrix: Analyzed to understand the balance between Precision and Recall (identifying False Positives vs. False Negatives).

SHAP Values (SHAP Summary Plot): Used to "open the black box" and interpret the model’s decisions. This allowed for a clear visualization of which features (e.g., gender, class, or age) had the strongest impact on survival probability.

📈 Key Insights
Based on the SHAP analysis, the most influential factors for survival were:

Gender (Sex_male): Being male was the strongest negative predictor for survival.

Socio-economic Status (Pclass_3): Passengers in the 3rd class had significantly lower survival rates.

Age Groups: Infants (Age_Baby) showed a high positive correlation with survival, reflecting the "women and children first" rescue priority.
