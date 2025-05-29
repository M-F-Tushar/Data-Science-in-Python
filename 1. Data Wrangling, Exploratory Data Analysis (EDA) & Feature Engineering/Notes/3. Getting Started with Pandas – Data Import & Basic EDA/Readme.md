# 📘 Lesson 1: 📊 Getting Started with Pandas – Data Import & Basic EDA

## 🎯 Goal

Build a strong foundation in **data wrangling** using the **Pandas** library. Learn to load datasets, explore data structures, clean and preprocess missing values, and apply basic **EDA techniques** essential for real-world machine learning.

---

## 🧱 Notebook Structure

The notebook contains **8 main tasks**, each representing a core data wrangling concept:

| Task | Focus |
|------|-------|
| **Task 1** | Load dataset and inspect basic statistics |
| **Task 2** | Handle missing values (e.g., dropping or imputing) |
| **Task 3** | Encode categorical features using one-hot encoding |
| **Task 4** | Normalize and standardize numerical features |
| **Task 5** | Apply filtering and data selection with Pandas |
| **Task 6** | Perform simple exploratory data analysis (EDA) |
| **Task 7** | Use `apply()` to transform data using custom functions |
| **Task 8** | Visualize with histograms and correlation matrices |

Each task includes:
- 🧠 Key Concepts
- 💡 Practice Exercises
- ✅ Solutions at the end (try solving first!)

---

## 🧪 Step-by-Step Guide

### 1️⃣ Import the Pandas Library

```python
import pandas as pd
2️⃣ Display All Rows and Columns (Optional)

pd.set_option('display.max_columns', None)
pd.set_option('display.max_rows', None)
Helps when viewing large datasets in Jupyter Notebook.

📂 Load the Dataset
Upload Instructions (Jupyter)
Click the File icon on the left sidebar.

Click the upload arrow to upload human_resources.csv.

Read CSV into a DataFrame

hr_df = pd.read_csv('human_resources.csv')
You can now start analyzing the data using the hr_df object.

🔍 Dataset Preview
The dataset contains columns like:

Age

BusinessTravel

Department

MonthlyIncome

Attrition (target variable)

Common challenges you'll explore:

Missing values

Mixed data types

Categorical features needing encoding

📌 Why This Dataset?
This HR dataset is a realistic classification use case:

Predict whether an employee leaves (Attrition)

Analyze relationships between job satisfaction, income, and demographics

🚀 What's Ahead
You’ll complete a capstone project at the end of this section:

Apply everything you’ve learned

Clean and explore a new dataset

Compare with a provided solution

✅ Quick Start Code
import pandas as pd

# Load dataset
hr_df = pd.read_csv('human_resources.csv')

# Display first few rows
hr_df.head()
📌 Pro Tip
Always explore your data before building models.
Clean data = Better predictions!
