# Phase 5: Data Cleaning

## Project Title

**Improving Student Academic Performance Through Data Analytics: Identifying the Key Drivers of Student Success**

---

# 1. Introduction

Data cleaning is a critical phase in the data analytics lifecycle. Its purpose is to ensure that the dataset is accurate, consistent, complete, and ready for analysis. During this phase, the Student Performance Dataset was validated using **Power Query in Power BI**.

Rather than making unnecessary modifications, the dataset was carefully examined to identify potential issues such as missing values, duplicate records, incorrect data types, inconsistent categorical values, and invalid numeric ranges.

---

# 2. Objective

The objectives of the data cleaning phase were to:

- Verify the integrity of the dataset.
- Ensure each column has the correct data type.
- Identify and resolve missing values.
- Detect duplicate records.
- Standardize categorical fields.
- Validate numeric values.
- Prepare an analysis-ready dataset while preserving the original data.

---

# 3. Data Cleaning Environment

| Item                  | Details                         |
| --------------------- | ------------------------------- |
| Tool                  | Microsoft Power BI              |
| Transformation Engine | Power Query                     |
| Dataset               | Student_Performance_Dataset.csv |
| Output Query          | Student Performance Cleaned     |

---

# 4. Data Cleaning Process

The following validation and transformation activities were performed.

| Step | Activity                                             | Status                               |
| ---- | ---------------------------------------------------- | ------------------------------------ |
| 1    | Imported dataset into Power Query                    | ✅ Completed                         |
| 2    | Verified data types                                  | ✅ Completed                         |
| 3    | Checked for missing values                           | ✅ No missing values found           |
| 4    | Checked for duplicate records                        | ✅ No duplicates found               |
| 5    | Reviewed categorical variables                       | ✅ Categories were consistent        |
| 6    | Validated numeric ranges                             | ✅ All values within expected limits |
| 7    | Applied **Trim** transformation to text columns      | ✅ Completed                         |
| 8    | Applied **Clean** transformation to text columns     | ✅ Completed                         |
| 9    | Renamed the query to **Student Performance Cleaned** | ✅ Completed                         |

---

# 5. Data Type Validation

The data types were reviewed and confirmed to be appropriate for analysis.

| Column                     | Data Type      |
| -------------------------- | -------------- |
| Student_ID                 | Text           |
| Age                        | Whole Number   |
| Gender                     | Text           |
| Class                      | Whole Number   |
| Study_Hours_Per_Day        | Decimal Number |
| Attendance_Percentage      | Whole Number   |
| Parental_Education         | Text           |
| Internet_Access            | Text           |
| Extracurricular_Activities | Text           |
| Math_Score                 | Whole Number   |
| Science_Score              | Whole Number   |
| English_Score              | Whole Number   |
| Previous_Year_Score        | Whole Number   |
| Final_Percentage           | Decimal Number |
| Performance_Level          | Text           |
| Pass_Fail                  | Text           |

---

# 6. Missing Value Assessment

No missing values were detected in any column.

| Metric         | Result |
| -------------- | ------ |
| Missing Values | 0      |
| Blank Records  | 0      |

---

# 7. Duplicate Record Assessment

Duplicate records were assessed using the available dataset.

| Metric         | Result |
| -------------- | ------ |
| Duplicate Rows | 0      |

Each student record remained unique throughout the cleaning process.

---

# 8. Numeric Validation

Numeric columns were reviewed to ensure values were within acceptable ranges.

| Variable              | Observed Range | Status   |
| --------------------- | -------------- | -------- |
| Age                   | 14–19          | ✅ Valid |
| Study_Hours_Per_Day   | 0.5–6.0        | ✅ Valid |
| Attendance_Percentage | 50–100         | ✅ Valid |
| Math_Score            | 35–100         | ✅ Valid |
| Science_Score         | 35–100         | ✅ Valid |
| English_Score         | 35–100         | ✅ Valid |
| Previous_Year_Score   | 40–95          | ✅ Valid |
| Final_Percentage      | 39.67–98.33    | ✅ Valid |
| Class                 | 9–12           | ✅ Valid |

No invalid or out-of-range values were identified.

---

# 9. Categorical Data Validation

The categorical columns were inspected for consistency.

| Column                     | Observation                          |
| -------------------------- | ------------------------------------ |
| Gender                     | Consistent values                    |
| Parental_Education         | Graduate, High_School, Post_Graduate |
| Internet_Access            | Consistent values                    |
| Extracurricular_Activities | Consistent values                    |
| Performance_Level          | Consistent values                    |
| Pass_Fail                  | Consistent values                    |

No inconsistencies, spelling variations, or unexpected categories were identified.

---

# 10. Transformations Applied

Although the dataset was already of high quality, two standard text-cleaning transformations were applied to all categorical columns.

## Trim

Removed any leading or trailing spaces from text fields.

## Clean

Removed hidden and non-printable characters from text fields.

These transformations are considered best practice and help ensure reliable filtering, grouping, and reporting.

---

# 11. Applied Steps in Power Query

The Power Query transformation pipeline consisted of the following steps:

1. Source
2. Navigation
3. Changed Type
4. Trimmed Text
5. Cleaned Text

This sequence provides a simple, transparent, and reproducible data preparation process.

---

# 12. Summary of Findings

The Student Performance Dataset demonstrated a high level of data quality.

### Key Findings

- No missing values were identified.
- No duplicate records were found.
- Data types were appropriate.
- Numeric values fell within expected ranges.
- Categorical variables were consistent.
- Standard text-cleaning transformations were applied.
- The dataset is suitable for exploratory analysis, SQL querying, KPI development, and Power BI dashboard creation.

---

# 13. Conclusion

The data cleaning process confirmed that the Student Performance Dataset is structurally sound and analysis-ready. Only minimal, non-destructive transformations were required to improve consistency and ensure reproducibility.

The cleaned dataset will serve as the foundation for the next phase of the project: **Data Quality Assessment**, where the dataset will be evaluated against established data quality dimensions before exploratory analysis begins.
