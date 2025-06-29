# 🚢 Titanic Survival Prediction

A machine learning project that predicts passenger survival on the Titanic using real historical data. This project explores the factors that influenced survival and implements various ML models to make accurate predictions.

---

## 📊 Dataset

The dataset is provided by [Kaggle's Titanic - Machine Learning from Disaster](https://www.kaggle.com/c/titanic). It contains data for passengers aboard the Titanic, including:

- **PassengerId** – Unique identifier for each passenger
- **Pclass** – Ticket class (1st, 2nd, 3rd)
- **Name** – Name of the passenger
- **Sex** – Gender
- **Age** – Age in years
- **SibSp** – Number of siblings/spouses aboard
- **Parch** – Number of parents/children aboard
- **Ticket** – Ticket number
- **Fare** – Passenger fare
- **Cabin** – Cabin number
- **Embarked** – Port of embarkation (C = Cherbourg, Q = Queenstown, S = Southampton)
- **Survived** – Target variable (0 = No, 1 = Yes)

---

## 🔍 Objective

To build a machine learning model that can predict whether a given passenger survived the Titanic disaster based on their personal information and ticket details.

---

## 🛠️ Tech Stack

- **Python**
- **Pandas, NumPy** – Data manipulation and analysis
- **Matplotlib, Seaborn** – Data visualization
- **Scikit-learn** – ML algorithms and model evaluation
- **Jupyter Notebook / Google Colab** – Development environment

---

## 🚀 Project Workflow

### 1. **Data Cleaning**
- Handled missing values in `Age`, `Embarked`, and `Cabin`
- Converted categorical variables (`Sex`, `Embarked`) into numerical format using Label Encoding and One-Hot Encoding
- Dropped less useful features like `Ticket`, `Cabin`, and `Name`

### 2. **Exploratory Data Analysis (EDA)**
- Visualized the survival rate based on:
  - Gender
  - Passenger class
  - Age groups
  - Family size
  - Embarked location
- Found strong survival patterns and trends in different categories

### 3. **Feature Engineering**
- Created new features such as:
  - `FamilySize` = `SibSp` + `Parch` + 1
  - `IsAlone` = 1 if `FamilySize` == 1 else 0
- Binned continuous variables like `Age` and `Fare` for better model performance

### 4. **Model Building**
- Tested various classification models:
  - Logistic Regression
  - Random Forest Classifier
  - Support Vector Machine (SVM)
  - Decision Tree
  - K-Nearest Neighbors (KNN)
- Used cross-validation to evaluate performance

### 5. **Model Evaluation**
- Accuracy, Precision, Recall, F1-Score
- Confusion Matrix
- Best-performing model: **Random Forest Classifier** (based on accuracy and generalization)

---

## 📌 Key Conclusions

- **Gender** played a major role: Females had significantly higher chances of survival.
- **Class mattered**: 1st class passengers had a much higher survival rate than 3rd class.
- **Children and younger passengers** were more likely to survive.
- **Passengers traveling alone** had lower chances compared to those with family aboard.
- **Embarkation point** also showed slight survival differences (those who boarded from Cherbourg had a better chance).

---

## ⚙️ How to Run

1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/titanic-survival-prediction.git
   cd titanic-survival-prediction
