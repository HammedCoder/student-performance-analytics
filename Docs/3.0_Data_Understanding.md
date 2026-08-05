## 3.1 Introduction

The Data Understanding phase explores the structure, content, and characteristics of the Student Performance Dataset. The objective is to gain familiarity with the data, identify potential quality issues, understand each variable, and determine how the dataset can answer the business questions from the previous phase.

## 3.2 Dataset Overview

| Attribute         | Value                                          |
| ----------------- | ---------------------------------------------- |
| Dataset Name      | Student Performance Dataset                    |
| Source            | Kaggle                                         |
| File Format       | CSV                                            |
| Number of Records | 5,000                                          |
| Number of Columns | 16                                             |
| Target Variables  | Final_Percentage, Performance_Level, Pass_Fail |
| Unique Identifier | Student_ID                                     |

## 3.3 Dataset Structure

### Identifier

- Student_ID

### Demographic Variables

- Age
- Gender

### Academic Variables

- Class
- Math_Score
- Science_Score
- English_Score
- Previous_Year_Score

### Behavioural Variables

- Study_Hours_Per_Day
- Attendance_Percentage
- Extracurricular_Activities

### Socioeconomic / Environmental Variables

- Parental_Education
- Internet_Access

### Outcome Variables

- Final_Percentage
- Performance_Level
- Pass_Fail

## 3.4 Data Dictionary

| Column                     | Description                 | Data Type   | Category      |
| -------------------------- | --------------------------- | ----------- | ------------- |
| Student_ID                 | Unique student identifier   | Text        | Identifier    |
| Age                        | Student age                 | Integer     | Demographic   |
| Gender                     | Student gender              | Text        | Demographic   |
| Class                      | Grade level or classroom    | Integer     | Academic      |
| Math_Score                 | Math exam score             | Integer     | Academic      |
| Science_Score              | Science exam score          | Integer     | Academic      |
| English_Score              | English exam score          | Integer     | Academic      |
| Previous_Year_Score        | Prior year score            | Integer     | Academic      |
| Study_Hours_Per_Day        | Daily study hours           | Numeric     | Behavioural   |
| Attendance_Percentage      | Attendance rate             | Numeric     | Behavioural   |
| Extracurricular_Activities | Participation in activities | Text/Binary | Behavioural   |
| Parental_Education         | Parent education level      | Text        | Socioeconomic |
| Internet_Access            | Access to internet at home  | Text/Binary | Socioeconomic |
| Final_Percentage           | Final percentage score      | Numeric     | Outcome       |
| Performance_Level          | Performance category        | Text        | Outcome       |
| Pass_Fail                  | Pass or fail status         | Text/Binary | Outcome       |

## 3.5 Initial Data Inspection

Before cleaning, examine:

- Number of observations
- Number of variables
- Data types
- Missing values
- Duplicate records
- Invalid values
- Outliers
- Inconsistent categories
- Blank values

## 3.6 Business Importance of Variables

| Variable                   | Business Importance                           |
| -------------------------- | --------------------------------------------- |
| Attendance                 | Measures classroom engagement                 |
| Study_Hours_Per_Day        | Indicates study habits                        |
| Previous_Year_Score        | Measures academic consistency                 |
| Internet_Access            | Indicates access to learning resources        |
| Parental_Education         | Reflects possible educational support at home |
| Extracurricular_Activities | Captures student engagement outside class     |
| Final_Percentage           | Primary measure of student success            |
| Performance_Level          | Simplifies performance segmentation           |
| Pass_Fail                  | Supports risk identification and intervention |

## 3.7 Variables for Analysis

### Independent Variables

- Age
- Gender
- Attendance_Percentage
- Study_Hours_Per_Day
- Internet_Access
- Parental_Education
- Extracurricular_Activities
- Previous_Year_Score

### Dependent Variables

- Final_Percentage
- Performance_Level
- Pass_Fail

## 3.8 Initial Observations

- The dataset contains both numerical and categorical variables.
- A unique identifier (`Student_ID`) is available.
- Academic performance is represented using multiple outcome variables.
- The dataset includes behavioural and demographic factors useful for identifying performance drivers.

## 3.9 Dataset Assumptions

- Each row represents one unique student.
- Scores are measured consistently.
- Attendance is accurately recorded.
- Previous year scores are comparable across students.

## 3.10 Dataset Limitations

- Only Mathematics, English, and Science scores are available.
- The dataset does not include subjects from business, arts, or humanities.
- Socioeconomic indicators such as household income are absent.
- Teacher-related variables are unavailable.
- School-specific information is not included.
- The analysis identifies associations rather than proving causation.

## 3.11 Potential Business Questions

- Does attendance improve academic performance?
- How strongly do study hours relate to final grades?
- Does parental education influence performance?
- Which students are most at risk of failing?
- Which class performs best?
