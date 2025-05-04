# 🚢 Titanic Data Analysis & Preprocessing

This project focuses on cleaning, preprocessing, and performing **exploratory data analysis (EDA)** on the famous [Titanic dataset](https://www.kaggle.com/competitions/titanic). It uses **statistical visualizations** and techniques to extract meaningful insights from passenger data.

---

## 📁 Dataset Overview

- **Source**: Titanic survival dataset (Kaggle)
- **Features**:
  - **Categorical**: `Sex`, `Embarked`, `Pclass`
  - **Numerical**: `Age`, `Fare`, `SibSp`, `Parch`
  - **Target**: `Survived` (0 = No, 1 = Yes)

---

## 🧹 Preprocessing Steps

### 1. 🔍 Import & Explore the Dataset
- Loaded the dataset using `pandas`.
- Inspected data types, null values, and basic structure with `info()` and `describe()` functions.

---

### 2. 🧩 Handle Missing Values
- **Age**: Missing values were filled with the **mean** of the column.
- **Embarked**: Missing entries were replaced with the **mode** (most frequent value).
- **Cabin**: The column was dropped due to a high percentage of missing data (77%).

---

### 3. 🔤 Categorical Encoding
- **Sex** and **Embarked** were converted into numerical values using **Label Encoding**.

---

### 4. ⚖️ Feature Normalization
- **StandardScaler** was applied to normalize numerical features like `Age` and `Fare` to ensure features contribute equally to models.

---

## 📊 Exploratory Data Analysis (EDA)

### 1. **Generate Summary Statistics (Mean, Median, Std, etc.)**
- **Summary Statistics**: Key statistics such as mean, median, standard deviation, and percentiles were generated for numerical features to understand the central tendency and spread of the data. This helps identify typical values and detect skewness or outliers.

### 2. **Create Histograms and Boxplots for Numeric Features**
- **Histograms**: Distributions of numerical features such as `Age`, `Fare`, `SibSp`, and `Parch` were visualized to understand their frequency and distribution.
- **Boxplots**: Used boxplots to identify outliers and the spread of numerical data like `Age`, `Fare`, and `SibSp`.

### 3. **Use Pairplot/Correlation Matrix for Feature Relationships**
- **Correlation Matrix**: Plotted a heatmap to examine the correlation between numerical features and their relationships with the target variable `Survived`.
- **Pairplot**: Visualized the relationships between key features (such as `Age`, `Fare`, `Pclass`) and survival status to identify patterns, trends, and possible interactions.

### 4. **Identify Patterns, Trends, or Anomalies in the Data**
- Patterns such as higher survival rates among women, first-class passengers, and younger passengers were identified. Trends like the relationship between `Fare` and survival rate were also examined. Anomalies such as extreme outliers in the `Fare` feature were spotted.

### 5. **Make Basic Feature-Level Inferences from Visuals**
- **Sex**: Women had a higher survival rate compared to men.
- **Pclass**: First-class passengers had a higher survival rate than second or third-class passengers.
- **Fare**: Higher fares were associated with higher survival rates.
- **Age**: Younger passengers had a better chance of survival, particularly children.

---
