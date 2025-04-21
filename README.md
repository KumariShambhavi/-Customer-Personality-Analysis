# -Customer-Personality-Analysis
Task_1
# 🧹 Data Cleaning Summary – Customer Personality Analysis Dataset

## 📌 Objective:
To clean and prepare a raw marketing dataset by handling missing values, removing duplicates, standardizing formats, and ensuring consistency for further analysis.

---

## 🔍 Questions & Answers on Data Cleaning

### 1. **What are missing values and how do you handle them?**  
Missing values are gaps in the dataset where no data has been recorded for a specific field.  
**Handled by:**  
- Replacing missing `Income` values with the mean using `fillna()`.  
- Dropping remaining rows with null values using `dropna()`.

---

### 2. **How do you treat duplicate records?**  
Duplicate records can introduce bias and inaccuracies in analysis.  
**Solution:** Used `.drop_duplicates()` to remove exact duplicate rows.

---

### 3. **Difference between `dropna()` and `fillna()` in Pandas?**  
- `dropna()`: Deletes rows/columns with null values.  
- `fillna()`: Replaces missing values with a defined strategy (e.g., mean, median, or constant).  
**Usage in this project:** Both were used — first `fillna()` for income, then `dropna()` for the rest.

---

### 4. **What is outlier treatment and why is it important?**  
Outlier treatment ensures extreme values do not distort analysis.  
**Approach used:**  
- Created an `age` column (`2024 - Year_Birth`).  
- Filtered out records with `age < 18` and `age > 100`.

---

### 5. **Explain the process of standardizing data.**  
Standardization improves readability and consistency.  
**Steps taken:**  
- Renamed columns to lowercase with underscores.  
- Standardized categorical text fields like `education`, `marital_status`.

---

### 6. **How do you handle inconsistent data formats (e.g., date/time)?**  
Uniform formats prevent parsing errors.  
**Example:**  
- Converted `Dt_Customer` to a consistent datetime format using `pd.to_datetime()`.

---

### 7. **What are common data cleaning challenges?**  
- Missing/null values  
- Duplicate records  
- Inconsistent text/date formats  
- Outliers and incorrect data types  
- Ambiguous or redundant columns

---

### 8. **How can you check data quality?**  
Use Pandas tools:  
- `df.isnull().sum()` – Check for missing values  
- `df.duplicated().sum()` – Detect duplicates  
- `df.dtypes` – Confirm data types  
- `df.describe()` – Review statistical summaries  
- Manual inspection for inconsistencies

---

## ✅ Final Output:
- Cleaned dataset saved as: `cleaned_marketing_campaign.csv`
- No missing values  
- All columns formatted consistently  
- Duplicate and outlier records handled  
- Date and categorical values standardized  
- Age column added and verified

---


