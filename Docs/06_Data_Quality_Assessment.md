# Phase 6: Data Quality Assessment

## Project Title

**Improving Student Academic Performance Through Data Analytics: Identifying the Key Drivers of Student Success**

---

# 1. Introduction

Data quality assessment is a critical stage in the analytics lifecycle that evaluates whether a dataset is reliable, accurate, and suitable for analysis. Unlike data cleaning, which focuses on correcting identified issues, data quality assessment measures the overall quality of the dataset against established quality dimensions.

This assessment was conducted after completing the data cleaning process using Power Query in Power BI to determine whether the Student Performance Dataset is fit for exploratory analysis, SQL analysis, KPI development, and dashboard reporting.

---

# 2. Objective

The objectives of this assessment were to:

- Evaluate the overall quality of the dataset.
- Assess the dataset against industry-standard data quality dimensions.
- Identify potential risks and limitations.
- Determine whether the dataset is suitable for business analysis.
- Establish confidence in the analytical results.

---

# 3. Assessment Methodology

The dataset was evaluated using the following data quality dimensions:

- Completeness
- Uniqueness
- Validity
- Consistency
- Accuracy
- Integrity

The assessment was performed using Power Query profiling tools and manual validation.

---

# 4. Data Quality Assessment

## 4.1 Completeness

Completeness measures whether all required data is available without missing or blank values.

### Assessment Results

| Metric             | Result   |
| ------------------ | -------- |
| Total Records      | 5,000    |
| Missing Values     | 0        |
| Blank Records      | 0        |
| Completeness Score | **100%** |

### Observation

No missing values or blank records were identified. Every observation contains complete information across all variables.

**Assessment:** Excellent

---

## 4.2 Uniqueness

Uniqueness ensures that each observation represents a distinct entity.

### Assessment Results

| Metric                | Result     |
| --------------------- | ---------- |
| Duplicate Records     | 0          |
| Duplicate Student IDs | 0          |
| Primary Key           | Student_ID |

### Observation

Each student record is uniquely identified by **Student_ID**, with no duplicate records detected.

**Assessment:** Excellent

---

## 4.3 Validity

Validity determines whether data values fall within acceptable business rules and expected ranges.

### Validation Rules

| Variable              | Expected Rule           | Status  |
| --------------------- | ----------------------- | ------- |
| Age                   | Between 14 and 19 years | ✅ Pass |
| Attendance Percentage | Between 50 and 100      | ✅ Pass |
| Study Hours Per Day   | Positive values         | ✅ Pass |
| Math Score            | Between 35 and 100      | ✅ Pass |
| English Score         | Between 35 and 100      | ✅ Pass |
| Science Score         | Between 35 and 100      | ✅ Pass |
| Previous Year Score   | Between 40 and 95       | ✅ Pass |
| Final Percentage      | Between 39.67 and 98.33 | ✅ Pass |
| Class                 | Between 9 and 12        | ✅ Pass |

### Observation

All numeric values fall within expected and realistic ranges.

**Assessment:** Excellent

---

## 4.4 Consistency

Consistency evaluates whether data follows uniform formatting and standardized values.

### Assessment Results

The following categorical variables were reviewed:

- Gender
- Parental_Education
- Internet_Access
- Extracurricular_Activities
- Performance_Level
- Pass_Fail

Power Query transformations applied:

- Trim Text
- Clean Text

### Observation

No inconsistent spellings, formatting issues, or unexpected categories were identified.

**Assessment:** Excellent

---

## 4.5 Accuracy

Accuracy measures how closely the data reflects real-world values.

Since no external reference dataset is available, accuracy was evaluated based on plausibility.

Examples include:

- Student ages are appropriate for secondary school.
- Attendance percentages are realistic.
- Study hours fall within expected daily ranges.
- Academic scores are within acceptable grading limits.

### Observation

The dataset appears realistic and internally consistent.

**Assessment:** High

---

## 4.6 Integrity

Integrity ensures that relationships within the dataset remain valid.

### Assessment Results

| Check                | Result     |
| -------------------- | ---------- |
| Unique Identifier    | Maintained |
| Record Structure     | Valid      |
| Broken Relationships | None       |

### Observation

Each row represents one student and the unique identifier was preserved throughout the cleaning process.

**Assessment:** Excellent

---

# 5. Data Quality Scorecard

| Quality Dimension |   Rating   | Status    |
| ----------------- | :--------: | --------- |
| Completeness      | ⭐⭐⭐⭐⭐ | Excellent |
| Uniqueness        | ⭐⭐⭐⭐⭐ | Excellent |
| Validity          | ⭐⭐⭐⭐⭐ | Excellent |
| Consistency       | ⭐⭐⭐⭐⭐ | Excellent |
| Accuracy          | ⭐⭐⭐⭐☆  | High      |
| Integrity         | ⭐⭐⭐⭐⭐ | Excellent |

---

# 6. Risks and Limitations

Although the dataset demonstrates excellent quality, several limitations should be acknowledged.

- The dataset contains only three academic subjects (Mathematics, English, and Science).
- Business, arts, and humanities subjects are not represented.
- Household income and other socioeconomic indicators are unavailable.
- Teacher-related variables are not included.
- School-level information is absent.
- Geographic information is unavailable.
- The dataset represents a single point in time and does not support longitudinal analysis.

These limitations relate to the scope of the dataset rather than its quality.

---

# 7. Overall Assessment

The Student Performance Dataset demonstrates a high level of quality across all assessed dimensions.

### Key Findings

- No missing values were detected.
- No duplicate records were identified.
- Data types were appropriate.
- Numeric values satisfied expected business rules.
- Categorical variables were consistent.
- Data integrity was maintained.
- The dataset is suitable for statistical analysis and visualization.

---

# 8. Conclusion

The Data Quality Assessment confirms that the Student Performance Dataset is reliable and suitable for analysis. The dataset satisfies the key dimensions of completeness, validity, consistency, uniqueness, and integrity, while demonstrating a high degree of internal accuracy.

Although some limitations exist due to the scope of available variables, these do not compromise the reliability of the dataset for achieving the objectives of this project.

The dataset is therefore considered **fit for Exploratory Data Analysis (EDA), SQL analysis, KPI development, and Power BI dashboard reporting**.
