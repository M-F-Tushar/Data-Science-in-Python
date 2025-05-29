# Handling Missing Data in Datasets

Welcome to this leacture
In this task, we will learn how to identify and handle missing values in datasets using **pandas** in Python.

---

## Overview

In the previous lesson, we calculated statistical measures like mean, max, and min employee age.  
Now, we will focus on:

- Locating rows with missing or null values.
- Summing missing values per column.
- Handling missing data by either dropping rows or filling missing values.

---

## Step 1: Locate Missing Values

Use the `isnull()` method on the DataFrame to find missing values:

```python
hr_df.isnull()
```
This returns a Boolean DataFrame with True where values are missing.

Visualizing Missing Data
To view rows with missing values:
```python
hr_df[hr_df.isnull().any(axis=1)]
```
Step 2: Count Missing Values Per Column
Sum the missing values for each column:
```python
hr_df.isnull().sum()
```
Example output:

MonthlyIncome    3
Department       1
MonthlyRate      2
JobRole          1
...
Step 3: Strategy 1 – Drop Rows with Missing Values
Drop all rows that contain any missing values:
```python
hr_df.dropna(how='any', inplace=True)
```
how='any' means drop the row if any missing value is present.

inplace=True updates the DataFrame directly.

Verify Changes
```python
hr_df.isnull().sum()
```
All missing values should be removed (output zeros).

Step 4: Strategy 2 – Fill Missing Values
Sometimes, instead of dropping rows, you can fill missing values with a statistic such as the mean.

Re-import Data
```python
import pandas as pd
hr_df = pd.read_csv("Human_Resources.csv")
```
Calculate Mean Monthly Income
```python
mean_income = hr_df['MonthlyIncome'].mean()
print(mean_income)
```
# Example output: 6505.0
Fill Missing Monthly Income Values
```python
hr_df['MonthlyIncome'].fillna(mean_income, inplace=True)
```
This replaces missing values in MonthlyIncome with the average value.

Final Notes
Always inspect your data for missing values before analysis.

Choose the right strategy (drop or fill) based on the dataset and context.

Dropping rows reduces data size but ensures data quality.

Filling missing values preserves dataset size but may introduce bias.

Next Steps
In the next lesson, we will cover the second optional practice opportunity.
Stay tuned!
