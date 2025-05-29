# 🧠 Exploratory Data Analysis (EDA) with Pandas 🐼

Welcome to this lesson on **Exploratory Data Analysis (EDA)** using the powerful Python library **Pandas**. This guide will walk you through essential EDA concepts and tools using real-world Human Resources data.

---

## 🎯 Objective

By the end of this lesson, you will be able to:

- Perform basic statistical analysis on datasets.
- Apply feature engineering strategies.
- Use encoding and normalization techniques.
- Handle missing data.
- Work with Pandas DataFrame operations.
- Visualize data relationships using heatmaps.

---

## 🔍 What is EDA?

**Exploratory Data Analysis (EDA)** is the process of investigating data sets to:

- 🧠 Understand the data structure.
- 🔍 Detect patterns and relationships.
- 🚨 Identify outliers or anomalies.

EDA is a key first step in the data science lifecycle to make informed decisions about data preprocessing and modeling.

---

## 🐼 What is Pandas?

**Pandas** is an open-source Python library designed for:

- 📊 High-performance data manipulation.
- 📈 Easy and flexible data analysis.
- 🧾 Handling structured data formats like CSV, Excel, SQL, etc.

---

## 📁 Use Case

We will analyze a **Human Resources dataset** using Pandas to demonstrate practical EDA techniques.

---

## 🧪 Topics Covered

### 1️⃣ Perform Statistical Analysis
- Use descriptive statistics like mean, median, mode, and standard deviation.
- Functions: `.describe()`, `.mean()`, `.std()`, `.value_counts()`

---

### 2️⃣ Understand Feature Engineering
- 🔧 Creating new features from existing columns (e.g., combining first and last names, extracting year from dates).
- 📐 Helps improve the accuracy and performance of machine learning models.

---

### 3️⃣ One-Hot Encoding & Normalization

#### 🔢 One-Hot Encoding
Convert categorical values into binary columns.
```python
pd.get_dummies(df['category_column'])
📏 Normalization
Scale numeric values to a range (0 to 1).
from sklearn.preprocessing import MinMaxScaler
scaler = MinMaxScaler()
df[['normalized_column']] = scaler.fit_transform(df[['original_column']])

4️⃣ Normalization vs Standardization
Technique	        Scale	              When to Use
Normalization	    0 to 1	            Algorithms using distance
Standardization	  Mean = 0, Std = 1	  For normal distribution assumptions

# Standardization example
from sklearn.preprocessing import StandardScaler
scaler = StandardScaler()
df[['standardized_column']] = scaler.fit_transform(df[['original_column']])

5️⃣ Handling Missing Data
Use Pandas to detect and manage missing values.
df.isnull().sum()
df.dropna()  # Drop rows with missing values
df.fillna(value)  # Replace missing values

6️⃣ Changing Data Types
Convert column data types for memory optimization and consistency.

df['column_name'] = df['column_name'].astype('int')

7️⃣ Apply Custom Functions
Define and apply your own functions to transform data.

def square(x):
    return x * x

df['new_column'] = df['existing_column'].apply(square)
8️⃣ Pandas Operations and Filtering
Filter rows based on conditions.

df_filtered = df[(df['age'] > 30) & (df['department'] == 'Sales')]
9️⃣ Correlation Matrix & Heatmap
Use Seaborn and Matplotlib to visualize relationships between numerical columns.

import seaborn as sns
import matplotlib.pyplot as plt

corr_matrix = df.corr()
sns.heatmap(corr_matrix, annot=True, cmap='coolwarm')
plt.title('Correlation Matrix Heatmap')
plt.show()
🚀 Let’s Get Started!
Now that you have an overview of EDA and Pandas, you're ready to dive into real datasets and apply these skills. Happy analyzing! 🎉
