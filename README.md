# InternNova Week 4 – Statistics, Data Visualization & Exploratory Data Analysis

## Project Overview

This project is part of the **InternNova Data Analytics Internship – Week 4 Assignment**.

The objective of this assignment is to apply **Statistics, Data Visualization, and Exploratory Data Analysis (EDA)** techniques using Python.

The project covers statistical analysis, correlation, probability, outlier detection, Matplotlib and Seaborn visualizations, data cleaning, exploratory analysis, insights, and data-driven recommendations.

---

## Objectives

The main objectives of this project are:

- Calculate Mean, Median, and Mode
- Calculate Variance and Standard Deviation
- Analyze Correlation and Probability
- Detect Outliers using the IQR method
- Create visualizations using Matplotlib
- Create visualizations using Seaborn
- Perform Exploratory Data Analysis (EDA)
- Identify and handle missing and inconsistent data
- Analyze correlations and identify meaningful insights
- Provide data-driven recommendations

---

## Dataset

The project uses the **Student Performance Dataset**.

### Dataset Information

- **Rows:** 1,000
- **Columns:** 12

### Columns

- `StudentID`
- `Name`
- `Gender`
- `AttendanceRate`
- `StudyHoursPerWeek`
- `PreviousGrade`
- `ExtracurricularActivities`
- `ParentalSupport`
- `FinalGrade`
- `Study Hours`
- `Attendance (%)`
- `Online Classes Taken`

---

# Tasks Completed

## Task 1 – Statistical Analysis: Mean, Median & Mode

Mean, Median, and Mode were calculated using the `FinalGrade` column.

### Results

- **Mean:** Approximately 80.03
- **Median:** 80
- **Mode:** 72

### Explanation

- **Mean:** Represents the average final grade.
- **Median:** Represents the middle value when grades are arranged in order.
- **Mode:** Represents the most frequently occurring grade.

---

## Task 2 – Variance & Standard Deviation

Variance and Standard Deviation were calculated for `FinalGrade`.

### Results

- **Variance:** Approximately 90.13
- **Standard Deviation:** Approximately 9.49

### Explanation

Variance measures how much the grades vary around the mean.

Standard deviation measures the spread of the grades around the average. A standard deviation of approximately 9.49 indicates that grades generally vary around the mean by about 9.49 grade points.

---

## Task 3 – Correlation & Probability

### Correlation

Correlation was calculated between:

- `StudyHoursPerWeek`
- `FinalGrade`

### Result

**Correlation ≈ 0.036**

This indicates a **very weak positive relationship** between weekly study hours and final grades in this dataset.

### Probability

The probability of randomly selecting a student with a final grade of **70 or above** was calculated.

- Students with FinalGrade ≥ 70: **777**
- Students with available FinalGrade values: **960**
- Probability: **0.8094**
- Probability Percentage: **80.94%**

---

## Task 4 – Outlier Detection

The **Interquartile Range (IQR)** method was used to identify outliers in the `Attendance (%)` column.

### IQR Results

- **Q1:** 63
- **Q3:** 89
- **IQR:** 26
- **Lower Bound:** 24
- **Upper Bound:** 128

Attendance values of **200%** were identified as potential outliers.

Since attendance percentage should normally be between **0% and 100%**, these values were also treated as inconsistent values during data cleaning.

### Visualization

A Seaborn box plot was used to visualize the attendance outliers.

---

# Task 5 – Matplotlib Visualizations

The following visualizations were created using **Matplotlib**:

### 1. Line Chart

**Average Final Grade by Study Hours Per Week**

Shows the average final grade for different weekly study-hour levels.

### 2. Bar Chart

**Average Final Grade by Parental Support**

Compares average final grades across different parental-support levels.

### 3. Pie Chart

**Student Distribution by Gender**

Shows the proportion of students by gender.

### 4. Histogram

**Distribution of Final Grades**

Shows how final grades are distributed across different grade ranges.

### 5. Scatter Plot

**Study Hours Per Week vs Final Grade**

Shows the relationship between weekly study hours and final grades.

---

# Task 6 – Seaborn Visualizations

The following visualizations were created using **Seaborn**:

### 1. Count Plot

Shows the number of students in each gender category.

### 2. Box Plot

Shows the distribution of final grades across different levels of parental support.

### 3. Correlation Heatmap

Shows correlations between numerical variables in the dataset.

### 4. Pair Plot

Provides visual comparisons between:

- Attendance Rate
- Study Hours Per Week
- Previous Grade
- Final Grade

These visualizations help identify patterns, relationships, and possible trends in the dataset.

---

# Task 7 – EDA: Data Inspection & Cleaning

The dataset was inspected for:

- Dataset shape
- Column names
- Data types
- Statistical summary
- Missing values
- Duplicate records
- Invalid values
- Inconsistent values

### Data Cleaning Performed

#### Study Hours

Values outside the expected **0–5 hour range** were identified and converted to missing values.

#### Attendance

Values outside the expected **0–100% range** were identified and converted to missing values.

#### Numerical Missing Values

Missing numerical values were handled using the **median**.

#### Categorical / Boolean Missing Values

Missing categorical and Boolean values were handled using the **mode**.

#### Duplicate Records

Duplicate records were checked and removed.

The dataset was checked again after cleaning to verify the results.

---

# Task 8 – EDA: Correlation & Insights

Correlation analysis was performed on the cleaned dataset.

### Insight 1 – Study Hours

`StudyHoursPerWeek` and `FinalGrade` have a very weak positive correlation of approximately **0.035**.

This indicates that weekly study hours alone do not strongly explain differences in final grades in this dataset.

### Insight 2 – Previous Grade

`PreviousGrade` and `FinalGrade` have an almost zero correlation of approximately **0.004**.

This indicates no meaningful linear relationship between these variables in the supplied dataset.

### Insight 3 – Attendance

`AttendanceRate` and `FinalGrade` have a very weak negative correlation of approximately **-0.011**.

Therefore, attendance rate does not show a meaningful linear relationship with final grades in this particular dataset.

---

# Task 9 – Business Recommendations

Since this project uses student-performance data, business recommendations are interpreted as recommendations for an educational institution.

### Recommendation 1 – Use Multiple Performance Factors

Institutions should not rely only on study hours when evaluating students because the correlation between `StudyHoursPerWeek` and `FinalGrade` is very weak.

Multiple academic and behavioral factors should be considered.

### Recommendation 2 – Implement Data-Quality Validation

Automated validation should be implemented before using student data for analysis.

The dataset contained invalid values such as:

- Attendance = 200%
- Negative Study Hours

Such values should be detected and corrected before making decisions.

### Recommendation 3 – Use EDA Dashboards

Educational institutions can use EDA dashboards to continuously monitor:

- Attendance
- Study patterns
- Previous grades
- Final grades

This can help identify areas that require further investigation.

---

# Tools & Technologies

- **Python**
- **Pandas**
- **NumPy**
- **Matplotlib**
- **Seaborn**
- **Google Colab**
- **GitHub**

---

# Project Structure

```text
InternNova-Week4/
│
├── student_performance_dataset.csv
│
├── internnova_week4_assignment.py
│
├── README.md
│
└── visualizations/
    ├── line_chart.png
    ├── bar_chart.png
    ├── pie_chart.png
    ├── histogram.png
    ├── scatter_plot.png
    ├── count_plot.png
    ├── box_plot.png
    ├── heatmap.png
    └── pair_plot.png