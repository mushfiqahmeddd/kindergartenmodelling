# kindergartenmodelling

# Kindergarten Achievement Prediction Modelling
**Predicting student reading and math outcomes using the Project STAR dataset.**

---

## Project Overview
This project builds a multi-output machine learning pipeline to estimate kindergarten students’ academic performance. Using data inspired by Tennessee’s **Project STAR** experiment, the analysis explores how classroom environments, teacher experience, and student demographics influence early childhood literacy and numeracy.

The core challenge was to move beyond simple linear relationships and evaluate whether non-linear machine learning models could significantly improve prediction accuracy over traditional statistical baselines.

---

## The Dataset
The model is trained on approximately **5,000 student records**. 

* **Target Variables:** Reading Score and Math Score (Multi-output regression).
* **Key Features:** * **Classroom:** Class type (small vs. regular), school identifier.
    * **Teacher:** Years of experience, degree level.
    * **Student:** Gender, birth quarter, lunch status (socioeconomic proxy).

---

## Technical Workflow

### 1. Exploratory Data Analysis (EDA)
Identified key correlations between socioeconomic status (lunch status) and test scores. Handled significant missingness in teacher-related variables using median and categorical imputation.

### 2. Feature Engineering & Preprocessing
* **Encoding:** Applied One-Hot Encoding to categorical variables (School ID, Class Type).
* **Scaling:** Standardized numerical features for linear and neural network models.
* **Multi-Output Wrapper:** Leveraged `scikit-learn`'s `MultiOutputRegressor` to predict both reading and math scores simultaneously.

### 3. Model Selection & Evaluation
Models were evaluated using **5-Fold Cross-Validation** to ensure generalizability. The Mean Squared Error (MSE) was the primary metric for comparison.

| Model Category | Algorithms Evaluated |
| :--- | :--- |
| **Baselines** | OLS Linear Regression |
| **Regularized** | Ridge, Lasso, Elastic Net |
| **Ensembles** | Random Forest, **Gradient Boosting (Winner)** |
| **Deep Learning** | Multi-Layer Perceptron (MLP) |

---

## Key Results
* **Best Model:** **Gradient Boosting Regressor** achieved the lowest Mean Squared Error.
* **Performance:** Achieved a **~17% reduction in prediction error** compared to the OLS baseline.
* **Feature Importance:** The most influential predictors of student success were **School Identifiers**, **Birth Quarter**, and **Teacher Experience**.


---

## 🧰 Tools Used
* **Language:** Python 3.x
* **Libraries:** `pandas`, `numpy`, `scikit-learn`, `matplotlib`, `seaborn`
* **Environment:** Jupyter Notebook

~17% improvement over the baseline linear regression model

Important predictors included school identifiers, birth quarter, gender, and teacher experience
