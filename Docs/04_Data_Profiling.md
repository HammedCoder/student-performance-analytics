# Phase 4: Data Profiling

## Objective

The objective of data profiling is to assess the dataset's structure, completeness, consistency, uniqueness, and validity before any transformations are applied.

## 4.1 Dataset Profile

| Attribute         |      Value |
| ----------------- | ---------: |
| Number of Records |      5,000 |
| Number of Columns |         16 |
| Missing Values    |          0 |
| Duplicate Records |          0 |
| Unique Identifier | Student_ID |

### Initial Observation

The dataset is complete with no missing values or duplicate rows, indicating good structural quality.

## 4.2 Data Types

| Data Type     | Columns                                                                                                           |
| ------------- | ----------------------------------------------------------------------------------------------------------------- |
| Text (Object) | Student_ID, Gender, Parental_Education, Internet_Access, Extracurricular_Activities, Performance_Level, Pass_Fail |
| Integer       | Age, Class, Attendance_Percentage, Math_Score, Science_Score, English_Score, Previous_Year_Score                  |
| Decimal       | Study_Hours_Per_Day, Final_Percentage                                                                             |

### Observation

`Student_ID` is stored as text, which is appropriate because it is an identifier rather than a numeric measure.

## 4.3 Completeness Assessment

| Check             | Result           |
| ----------------- | ---------------- |
| Missing Values    | ✅ None          |
| Blank Rows        | ✅ None detected |
| Duplicate Records | ✅ None          |

## 4.4 Uniqueness Assessment

| Column     | Expected | Result    |
| ---------- | -------- | --------- |
| Student_ID | Unique   | ✅ Unique |

## 4.5 Consistency Checks

The following checks will be validated during data cleaning:

- Consistent spelling of categorical values
- Consistent numeric formats
- No unexpected category variations

## 4.6 Validity Checks

| Variable              | Expected Rule               |
| --------------------- | --------------------------- |
| Age                   | Reasonable school-age range |
| Attendance_Percentage | Between 0 and 100           |
| Study_Hours_Per_Day   | Positive values             |
| Subject Scores        | Between 0 and 100           |
| Final_Percentage      | Between 0 and 100           |

## 4.7 Potential Outlier Review

Potential outliers will be reviewed for:

- Study_Hours_Per_Day
- Attendance_Percentage
- Math_Score
- Science_Score
- English_Score
- Previous_Year_Score
- Final_Percentage

## 4.8 Profiling Summary

| Quality Dimension | Status                                     |
| ----------------- | ------------------------------------------ |
| Completeness      | ✅ Excellent                               |
| Uniqueness        | ✅ Excellent                               |
| Missing Values    | ✅ None                                    |
| Duplicate Records | ✅ None                                    |
| Data Types        | ✅ Mostly Appropriate                      |
| Overall Readiness | ✅ Suitable for Data Cleaning and Analysis |

## Key Findings

- The dataset contains **5,000 student records** across **16 variables**.
- No missing values were detected.
- No duplicate records were found.
- `Student_ID` is unique and suitable as the primary identifier.
- Data types are generally appropriate for analysis.
- The dataset is ready for the Data Cleaning phase.

## Conclusion

The Student Performance Dataset demonstrates a high level of structural quality and is suitable for further preparation and analysis. The next phase will focus on validating data consistency, standardizing values where necessary, and preparing the dataset for exploratory analysis and dashboard development.
