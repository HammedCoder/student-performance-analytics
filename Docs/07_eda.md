# Exploratory Data Analysis (EDA)

## Project

**Project Title:** Improving Student Academic Performance Through Data
Analytics: Identifying the Key Drivers of Student Success

**Dataset:** Student Performance Dataset  
**Analysis Tool:** Python (Pandas, NumPy, Matplotlib)

------------------------------------------------------------------------

## 1. Objective

The objective of the Exploratory Data Analysis (EDA) was to understand
the structure and characteristics of the student performance dataset,
identify important patterns and relationships, assess the distribution
of academic outcomes, and determine whether the available variables
provide evidence of factors associated with student success.

------------------------------------------------------------------------

## 2. Dataset Overview

The dataset contains **5,000 student records** and includes demographic,
engagement, academic, and outcome variables.

| Category             | Variables                                                       |
|----------------------|-----------------------------------------------------------------|
| Student Information  | Student_ID, Age, Gender, Class                                  |
| Engagement           | Study_Hours_Per_Day, Attendance_Percentage                      |
| Background           | Parental_Education, Internet_Access, Extracurricular_Activities |
| Academic Performance | Math_Score, Science_Score, English_Score, Previous_Year_Score   |
| Outcome              | Final_Percentage, Performance_Level, Pass_Fail                  |

### Dataset Scope

The dataset contains scores for only three academic subjects:

- Mathematics
- Science
- English

It does not contain Business, Humanities, Arts, or other subject areas.
Therefore, conclusions about overall academic performance should be
interpreted as conclusions based on the subjects and variables available
in this dataset.

------------------------------------------------------------------------

## 3. Data Structure and Completeness

The dataset contains:

- **5,000 rows**
- **15 columns**
- **5,000 unique Student IDs**
- **No missing values**
- **No duplicate records**

Python checks confirmed that all columns contained zero missing values
and that no duplicate records were identified.

------------------------------------------------------------------------

## 4. Descriptive Statistics

| Variable              |  Mean | Median |   Min |    Max |
|-----------------------|------:|-------:|------:|-------:|
| Age                   | 16.51 |  17.00 | 14.00 |  19.00 |
| Class                 | 10.50 |  10.00 |  9.00 |  12.00 |
| Study Hours Per Day   |  3.29 |   3.30 |  0.50 |   6.00 |
| Attendance Percentage | 74.92 |  75.00 | 50.00 | 100.00 |
| Math Score            | 67.75 |  68.00 | 35.00 | 100.00 |
| Science Score         | 66.90 |  67.00 | 35.00 | 100.00 |
| English Score         | 67.78 |  68.00 | 35.00 | 100.00 |
| Previous Year Score   | 67.28 |  67.00 | 40.00 |  95.00 |
| Final Percentage      | 67.48 |  67.33 | 36.33 |  98.33 |

------------------------------------------------------------------------

## 5. Final Percentage Distribution

A histogram was created to examine the distribution of
`Final_Percentage`.

The distribution is broadly centered around the high-60s and appears
approximately bell-shaped.

- Mean final percentage: **67.48%**
- Median final percentage: **67.33%**
- Minimum: **36.33%**
- Maximum: **98.33%**
- Skewness: approximately **-0.018**

### Interpretation

The skewness value is very close to zero, indicating that the final
percentage distribution is approximately symmetric.

------------------------------------------------------------------------

## 6. Study Hours and Final Percentage

The relationship between `Study_Hours_Per_Day` and `Final_Percentage`
was examined using a scatter plot and correlation analysis.

**Pearson correlation: r = -0.013**

This represents an extremely weak negative linear relationship.

### Interpretation

Within this dataset, the number of reported study hours per day does not
show a meaningful linear relationship with final percentage.

This does **not** mean that studying has no effect on academic
performance. It means that the available data does not show a meaningful
**linear association** between these two variables.

------------------------------------------------------------------------

## 7. Attendance and Final Percentage

The relationship between `Attendance_Percentage` and `Final_Percentage`
was examined.

**Pearson correlation: r = -0.017**

This indicates an extremely weak negative linear relationship.

### Interpretation

Attendance percentage does not show a meaningful linear association with
final percentage in this dataset.

The result should be interpreted cautiously because the dataset does not
capture factors such as classroom participation, teaching effectiveness,
student motivation, or learning environment.

------------------------------------------------------------------------

## 8. Previous Year Score and Final Percentage

The relationship between `Previous_Year_Score` and `Final_Percentage`
was examined using a scatter plot and correlation analysis.

**Pearson correlation: r = -0.017**

This represents an extremely weak negative linear relationship.

### Interpretation

Previous-year score does not show a meaningful linear association with
final percentage in this dataset.

------------------------------------------------------------------------

## 9. Subject-Level Performance

| Subject     |       Mean |     Median | Standard Deviation |
|-------------|-----------:|-----------:|-------------------:|
| Mathematics |     67.75% |     68.00% |              18.72 |
| English     | **67.78%** | **68.00%** |          **19.25** |
| Science     |     66.90% |     67.00% |              19.14 |

### Interpretation

English recorded the highest average score at **67.78%**, followed very
closely by Mathematics at **67.75%**. Science recorded the lowest
average at **66.90%**.

The difference between the highest and lowest subject averages is only
**0.88 percentage points**, indicating broadly similar performance
across the three subjects.

English had the highest standard deviation, indicating slightly greater
variation in English scores. However, the differences in variability
between subjects were relatively small.

------------------------------------------------------------------------

## 10. Correlation Between Subject Scores

|         |  Math | Science | English |
|---------|------:|--------:|--------:|
| Math    |  1.00 |   -0.02 |    0.01 |
| Science | -0.02 |    1.00 |    0.00 |
| English |  0.01 |    0.00 |    1.00 |

### Interpretation

The three subject scores show virtually no linear association with one
another.

- Math vs Science: **r = -0.020**
- Math vs English: **r = 0.010**
- Science vs English: **r = 0.002**

This indicates that a student’s performance in one subject does not
reliably predict performance in another subject through a linear
relationship within this dataset.

Correlation measures linear association and does not establish the
absence of non-linear relationships.

------------------------------------------------------------------------

## 11. Demographic and Background Analysis

### 11.1 Gender

| Gender | Count | Mean Final % | Median | Std. Dev. |
|--------|------:|-------------:|-------:|----------:|
| Female | 2,553 |        67.42 |  67.33 |     10.89 |
| Male   | 2,447 |        67.54 |  67.67 |     11.05 |

The difference in average final percentage between males and females is
very small.

**Finding:** Gender does not appear to be an important differentiating
factor in final academic performance within this dataset.

### 11.2 Parental Education

| Parental Education | Count | Mean Final % | Median | Std. Dev. |
|--------------------|------:|-------------:|-------:|----------:|
| Graduate           | 1,661 |        67.45 |  67.67 |     11.01 |
| High School        | 1,660 |        67.57 |  67.33 |     10.83 |
| Postgraduate       | 1,679 |        67.41 |  67.33 |     11.06 |

The average final percentages are very similar across the three parental
education groups.

**Finding:** The available data does not show a substantial difference
in final performance based on parental education.

### 11.3 Internet Access

| Internet Access | Count | Mean Final % | Median | Std. Dev. |
|-----------------|------:|-------------:|-------:|----------:|
| No              | 2,622 |        67.53 |  67.50 |     10.93 |
| Yes             | 2,378 |        67.42 |  67.33 |     11.01 |

The difference between the groups is very small.

**Finding:** Internet access does not show a substantial difference in
average final percentage within this dataset.

### 11.4 Extracurricular Activities

| Extracurricular Activities | Count | Mean Final % | Median | Std. Dev. |
|----------------------------|------:|-------------:|-------:|----------:|
| No                         | 2,481 |        67.17 |  67.33 |     10.91 |
| Yes                        | 2,519 |        67.78 |  67.67 |     11.01 |

Students participating in extracurricular activities have a slightly
higher average final percentage.

The difference is approximately **0.61 percentage points**.

**Finding:** Although the extracurricular-activity group has a slightly
higher average, the difference is small and does not provide sufficient
evidence of a strong relationship.

------------------------------------------------------------------------

## 12. Class-Level Analysis

Final percentage distributions were examined across Classes 9, 10, 11,
and 12.

The box plots showed broadly similar distributions across the four
classes.

A small number of low-score observations were identified as potential
outliers. These observations were investigated and confirmed as valid
student records rather than data-entry errors.

Examples include:

- Student S1687: Final Percentage = **37.67%**
- Student S2719: Final Percentage = **36.33%**

These records were retained because their underlying academic scores
were valid.

**Finding:** Class level does not show a strong visual difference in
final percentage distributions within this dataset.

------------------------------------------------------------------------

## 13. Outlier Investigation

Outlier analysis was performed using distribution plots and box plots.

Some unusually high and low final percentages were observed. The extreme
values were investigated rather than automatically removed.

The unusual observations corresponded to valid combinations of study
hours, attendance, previous-year score, subject scores, and final
percentage.

Therefore, the identified observations were treated as **valid
observations rather than data errors**.

### Analytical Principle

Outliers should not be removed simply because they are unusual. They
should only be removed when there is evidence that they are caused by
data-entry errors, measurement errors, invalid records, or other
documented data-quality problems.

------------------------------------------------------------------------

## 14. Potential Malpractice Interpretation

Some students showed relatively high final percentages despite very low
reported study hours. This pattern was investigated because it could
appear unusual.

However, the dataset does not contain sufficient evidence to conclude
that malpractice or academic misconduct occurred.

Therefore, the analysis **does not label any student as engaging in
malpractice**.

A more appropriate interpretation is:

> Some student records display combinations of high academic scores and
> low reported study hours that may warrant further investigation in a
> real school setting. However, the available dataset does not provide
> sufficient evidence to attribute these observations to malpractice.

In a real educational environment, such cases would require additional
evidence such as examination records, assessment history, invigilation
reports, or other institutional information.

------------------------------------------------------------------------

## 15. Overall EDA Findings

The analysis found no strong linear relationship between final academic
performance and the available demographic, engagement, and historical
performance variables examined in this study.

Variables such as study hours, attendance, previous-year score, gender,
parental education, internet access, extracurricular activities, and
class showed either very weak correlations or only small differences in
average final performance.

Therefore, the available dataset does not provide sufficient evidence to
identify a single dominant driver of student success.

These findings should be interpreted within the limitations of the
dataset. The absence of strong linear relationships does not necessarily
mean that these factors have no influence on academic performance.

Other factors not captured in the dataset—such as teaching quality,
socioeconomic background, student motivation, learning environment,
prior knowledge, assessment conditions, and school resources—may also
contribute to student outcomes.

------------------------------------------------------------------------

## 16. Key EDA Conclusions

1.  The dataset contains 5,000 complete student records with no missing
    values or duplicate records.
2.  Overall final performance is centered around approximately
    **67.5%**.
3.  Final percentage has an approximately symmetric distribution.
4.  Study hours show an extremely weak linear relationship with final
    percentage.
5.  Attendance shows an extremely weak linear relationship with final
    percentage.
6.  Previous-year score shows an extremely weak linear relationship with
    final percentage.
7.  Mathematics, Science, and English have very similar average
    performance levels.
8.  The three subject scores have virtually no linear relationship with
    one another.
9.  Gender, parental education, internet access, extracurricular
    activities, and class show only small differences in average final
    performance.
10. Unusual observations were investigated and retained where they
    represented valid records.
11. The dataset does not provide sufficient evidence to identify a
    single dominant driver of student success.
12. Additional variables would be required to investigate deeper
    educational factors and potential causal relationships.

------------------------------------------------------------------------

## 17. EDA Limitations

- Only three subjects are represented: Mathematics, Science, and
  English.
- Business, Humanities, Arts, and other subjects are not included.
- The dataset does not contain socioeconomic information.
- Teaching quality and school-level factors are not available.
- Student motivation and learning environment are not measured.
- Study hours may be self-reported and may not represent actual study
  quality.
- Correlation analysis identifies linear association, not causation.
- The dataset does not provide sufficient evidence for determining
  academic malpractice.
- The available variables may not capture all important factors
  influencing academic performance.

------------------------------------------------------------------------

## 18. Next Phase

The exploratory analysis has provided sufficient understanding of the
dataset and its major patterns.

The next phase is **KPI Definition**.

The KPI phase will translate the analytical findings into measurable
educational indicators for the Power BI dashboard.

Proposed KPIs include:

- Total Students
- Average Final Percentage
- Pass Rate
- Average Math Score
- Average Science Score
- Average English Score
- Performance Level Distribution

The KPIs will be formally defined before dashboard development so that
every visual has a clear analytical and business purpose.
