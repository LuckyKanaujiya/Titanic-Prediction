# 🚢 Titanic Survival Prediction Using IBM SPSS Modeler

## 📚 Project Overview
This project builds a machine learning model to predict Titanic passenger survival based on features like age, gender, ticket class, and fare.  
The model is developed using IBM SPSS Modeler, including data cleaning, model training, evaluation, and prediction.

---

## 🧩 Dataset
The dataset contains the following features:
- **PassengerId**
- **Pclass**
- **Name**
- **Sex**
- **Age**
- **SibSp**
- **Parch**
- **Ticket**
- **Fare**
- **Cabin**
- **Embarked**
- **Survived** (Target Variable)

---

## 🛠️ Tools Used
- IBM SPSS Modeler
- GitHub

---

## ⚙️ Project Workflow

### 1. Data Loading
- Used `Var. File` node to load CSV dataset (`tested.csv`).

### 2. Data Preprocessing

- **Data Audit Node**: Identified missing values.
- **Filler Node**: Replaced missing data.

Example Filler Node Expression:
```plaintext
For Age:
if (missing(Age)) 28 else Age

For Embarked:
if (missing(Embarked)) 'S' else Embarked
Creating a child/adult feature:
if (Age <= 16) 'Child' else 'Adult'

