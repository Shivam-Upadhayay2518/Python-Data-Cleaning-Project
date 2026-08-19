<div align="center">

# 🧹 E-Commerce Data Cleaning & Manipulation

### 🐍 Python • Pandas • NumPy • Jupyter Notebook

<img src="https://img.icons8.com/3d-fluency/94/python.png" width="65"/>
<img src="https://img.icons8.com/3d-fluency/94/jupyter.png" width="65"/>
<img src="https://img.icons8.com/3d-fluency/94/database.png" width="65"/>
<img src="https://img.icons8.com/3d-fluency/94/bar-chart.png" width="65"/>
<img src="https://img.icons8.com/3d-fluency/94/github.png" width="65"/>

### Transforming messy E-Commerce data into clean, validated & analysis-ready data.

<img src="https://img.shields.io/badge/Task-03-111827?style=for-the-badge"/>
<img src="https://img.shields.io/badge/Python-3.x-3776AB?style=for-the-badge&logo=python&logoColor=white"/>
<img src="https://img.shields.io/badge/Pandas-Data%20Cleaning-150458?style=for-the-badge&logo=pandas&logoColor=white"/>
<img src="https://img.shields.io/badge/NumPy-Transformation-013243?style=for-the-badge&logo=numpy&logoColor=white"/>
<img src="https://img.shields.io/badge/Jupyter-Notebook-F37626?style=for-the-badge&logo=jupyter&logoColor=white"/>

</div>

---

## 🎯 Project Objective

This project focuses on **data cleaning, validation, transformation, and manipulation** of a dirty E-Commerce dataset using **Python, Pandas, and NumPy**.

The objective is to transform raw operational data containing duplicates, missing values, inconsistent data types, and date-format issues into a **clean, reliable, and analysis-ready dataset**.

---

## 🔄 Data Cleaning Pipeline

```text
🗃️ Raw E-Commerce Dataset
          ↓
🔎 Data Inspection
          ↓
📋 Shape • Columns • Data Types
          ↓
⚠️ Missing Values & Duplicates
          ↓
🧹 Data Cleaning
          ↓
🔧 Data Type Conversion
          ↓
🩹 Missing Value Imputation
          ↓
📅 Date Standardization
          ↓
🏷️ Feature Engineering
          ↓
✅ Final Validation
          ↓
📊 Before vs After Comparison
          ↓
💾 Cleaned Dataset
```

---

## 📌 Dataset Overview

| Attribute               | Details                  |
| ----------------------- | ------------------------ |
| 📦 Dataset              | Dirty E-Commerce Dataset |
| 📊 Initial Rows         | **1,010**                |
| 📑 Initial Columns      | **14**                   |
| 🔁 Duplicate Rows       | **8**                    |
| 📊 Final Rows           | **1,002**                |
| 📑 Final Columns        | **15**                   |
| ❌ Final Missing Values  | **0**                    |
| 🔁 Final Duplicate Rows | **0**                    |
| 🏷️ New Feature         | `Price_Category`         |

---

## 🧹 Data Cleaning Operations

### 1️⃣ Duplicate Removal

Duplicate records were identified and removed using Pandas:

```python
df = df.drop_duplicates()
```

---

### 2️⃣ Numeric Data Type Conversion

`Unit_Price` was converted into a numeric data type while handling invalid values:

```python
df["Unit_Price"] = pd.to_numeric(
    df["Unit_Price"],
    errors="coerce"
)
```

---

### 3️⃣ Date Standardization

`Order_Date` was converted into a proper datetime format:

```python
df["Order_Date"] = pd.to_datetime(
    df["Order_Date"],
    format="mixed",
    errors="coerce"
)
```

---

### 4️⃣ Missing Value Treatment

#### Numerical Columns

Median imputation was applied to:

* `Unit_Price`
* `Customer_Rating`
* `Delivery_Days`

#### Categorical Columns

Mode imputation was applied to:

* `City`
* `Payment_Method`

---

### 5️⃣ Date Gap Handling

Remaining missing values in `Order_Date` were handled using forward filling:

```python
df["Order_Date"] = df["Order_Date"].ffill()
```

---

### 6️⃣ 🏷️ Feature Engineering

A new feature named `Price_Category` was created using the median `Unit_Price` as the threshold.

```python
df["Price_Category"] = np.where(
    df["Unit_Price"] >= df["Unit_Price"].median(),
    "High",
    "Low"
)
```

---

## 📊 Before vs After

| Quality Metric    | Before |     After |
| ----------------- | -----: | --------: |
| 📦 Rows           |  1,010 | **1,002** |
| 📑 Columns        |     14 |    **15** |
| ⚠️ Missing Values |    160 |     **0** |
| 🔁 Duplicate Rows |      8 |     **0** |

### 📈 Result

**8 duplicate records removed**

**160 missing values handled**

**1 new analytical feature created**

**Final dataset validated successfully**

---

## 🧠 Data Analytics Skills Demonstrated

<div align="center">

| 🧩 Skill                  | ⚙️ Application                          |
| ------------------------- | --------------------------------------- |
| 🔎 Data Inspection        | Shape, columns, data types & statistics |
| 🧹 Data Cleaning          | Duplicate removal & null treatment      |
| 🩹 Missing Value Handling | Median & mode imputation                |
| 🔧 Data Transformation    | Numeric & datetime conversion           |
| 📅 Date Processing        | Date standardization & filling          |
| 🏷️ Feature Engineering   | `Price_Category` creation               |
| ✅ Data Validation         | Final null & duplicate checks           |
| 💾 Data Export            | Cleaned dataset generation              |

</div>

---

## 🛠️ Tech Stack

<div align="center">

### 🐍 Programming & Analytics

<img src="https://img.icons8.com/3d-fluency/94/python.png" width="75"/>
<img src="https://img.icons8.com/3d-fluency/94/jupyter.png" width="75"/>
<img src="https://img.icons8.com/3d-fluency/94/database.png" width="75"/>
<img src="https://img.icons8.com/3d-fluency/94/bar-chart.png" width="75"/>

<br>

**Python** • **Pandas** • **NumPy** • **Jupyter Notebook**

### 🔧 Development Tools

<img src="https://skillicons.dev/icons?i=git,github,vscode" height="50"/>

<br>

**Git** • **GitHub** • **VS Code**

</div>

---

## 📂 Project Structure

```text
TASK-03-E-COMMERCE-DATA-CLEANING/
│
├── 📓 TASK03_DATA ANALYST INTERN.ipynb
│
├── 🗃️ dirty_ecommerce_dataset(1).csv
│
├── 📊 Cleaned Ecommerce Dataset.xls
│
└── 📖 README.md
```

---

## 🚀 How to Run the Project

### 1️⃣ Clone the Repository

```bash
git clone <YOUR_REPOSITORY_URL>
```

```bash
cd TASK-03-E-COMMERCE-DATA-CLEANING
```

### 2️⃣ Install Required Libraries

```bash
pip install pandas numpy jupyter
```

### 3️⃣ Launch Jupyter Notebook

```bash
jupyter notebook
```

Open:

```text
TASK03_DATA ANALYST INTERN.ipynb
```

---

## 🔍 Data Quality Validation

```text
✅ Duplicate records removed
✅ Numeric values converted
✅ Date values standardized
✅ Missing numerical values imputed
✅ Missing categorical values imputed
✅ Remaining date gaps handled
✅ New analytical feature created
✅ Final dataset validated
✅ Cleaned dataset exported
```

---

## 📈 What Can Be Done With the Cleaned Dataset?

The cleaned dataset is ready for further **Data Analytics & Business Intelligence** workflows:

* 📊 Exploratory Data Analysis (EDA)
* 📈 Sales & revenue analysis
* 🛍️ Product/category analysis
* 👥 Customer analysis
* 💳 Payment-method analysis
* 🚚 Delivery-performance analysis
* ⭐ Customer-rating analysis
* 📅 Time-series analysis
* 📊 Power BI dashboards
* 🤖 Machine Learning preprocessing

---

## 💡 Key Takeaway

> **Good analytics starts with good data.**

This project demonstrates the transformation of **raw and inconsistent E-Commerce data into clean, validated, and analysis-ready data**.

The cleaned dataset provides a reliable foundation for **EDA, visualization, business intelligence, and further analytical modeling**.

---

## 🏆 Project Outcome

<div align="center">

### 🗃️ Raw Data

**1,010 Rows • 14 Columns**

⬇️

### 🧹 Cleaned & Transformed

**Duplicates Removed • Missing Values Handled • Data Types Fixed**

⬇️

### 📊 Final Dataset

**1,002 Rows • 15 Columns • 0 Missing Values • 0 Duplicates**

</div>

---

## 👨‍💻 Author

<div align="center">

### **Shivam Upadhayay**

**B.Tech — Artificial Intelligence & Data Science**

📊 Data Analytics | 🐍 Python | 🗄️ SQL | 📈 Power BI | 🤖 AI/ML

</div>

---

<div align="center">

### 🧹 Clean Data → 📊 Better Analysis → 💡 Better Decisions

**Task 03 • Data Analyst Internship**

⭐ If you found this project useful, consider giving the repository a star!

</div>
