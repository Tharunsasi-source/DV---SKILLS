# Students Performance Analysis Using Python

## 1. Project Overview

This project analyzes student performance data using Python.

The main purpose of this project is to understand students' performance in **Math, Reading, and Writing** and calculate their total score and percentage.

The project also examines basic statistical values such as mean, median, mode, standard deviation, and quartiles.

## 2. Dataset

The dataset used in this project is:

`StudentsPerformance.csv`

The dataset contains **1000 student records and 8 columns**.

The main columns are:

| Column                      | Description                                          |
| --------------------------- | ---------------------------------------------------- |
| gender                      | Gender of the student                                |
| race/ethnicity              | Student's race/ethnicity group                       |
| parental level of education | Education level of the student's parents             |
| lunch                       | Type of lunch received                               |
| test preparation course     | Whether the student completed the preparation course |
| math score                  | Student's math score                                 |
| reading score               | Student's reading score                              |
| writing score               | Student's writing score                              |

The dataset contains 5 categorical columns and 3 numerical score columns.

## 3. Technologies Used

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Google Colab

## 4. Libraries Used

```python
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns
```

## 5. Loading the Dataset

The dataset was loaded using Pandas.

```python
df = pd.read_csv("/content/StudentsPerformance.csv")
```

The first and last records were viewed using `head()` and `tail()`.

## 6. Dataset Information

The dataset contains:

* **1000 rows**
* **8 columns**
* **3 numerical columns**
* **5 categorical columns**

The dataset does not contain missing values. All 1000 records have values in every column.

## 7. Checking Missing Values

Missing values were checked using:

```python
print(df.isnull().sum())
```

The result showed **0 missing values in all columns**.

The `dropna()` function was also used:

```python
df = df.dropna()
```

Since there were no missing values, the dataset size remained unchanged.

## 8. Descriptive Statistics

The `describe()` function was used to understand the numerical columns.

```python
df.describe()
```

The average scores were:

| Subject | Mean Score |
| ------- | ---------: |
| Math    |     66.089 |
| Reading |     69.169 |
| Writing |     68.054 |

Reading has the highest average score among the three subjects.

## 9. Mean

The mean score was calculated using:

```python
df[score_columns].mean()
```

Results:

* Math: **66.089**
* Reading: **69.169**
* Writing: **68.054**

## 10. Median

The median was calculated using:

```python
df[score_columns].median()
```

Results:

* Math: **66**
* Reading: **70**
* Writing: **69**

## 11. Mode

The mode was calculated using:

```python
df[score_columns].mode()
```

The most common scores were:

* Math: **65**
* Reading: **72**
* Writing: **74**

## 12. Standard Deviation

Standard deviation was calculated using:

```python
df[score_columns].std()
```

Results:

* Math: **15.16**
* Reading: **14.60**
* Writing: **15.20**

This shows the amount of variation in the scores.

## 13. Quartile Analysis

The 25th, 50th, and 75th percentiles were calculated.

### 25th Percentile

* Math: **57**
* Reading: **59**
* Writing: **57.75**

### 50th Percentile

* Math: **66**
* Reading: **70**
* Writing: **69**

### 75th Percentile

* Math: **77**
* Reading: **79**
* Writing: **79**

## 14. Total Score Calculation

A new column called `Total Score` was created by adding the three subject scores.

```python
df['Total Score'] = (
    df['math score'] +
    df['reading score'] +
    df['writing score']
)
```

The maximum possible total score is **300**.

Example:

```text
Math = 72
Reading = 72
Writing = 74

Total Score = 218
```

## 15. Percentage Calculation

The percentage was calculated from the total score.

```python
df['Percentage'] = (df['Total Score'] / 300) * 100
```

For example, a student with a total score of 218 gets a percentage of approximately **72.67%**.

## 16. Key Findings

Based on the analysis:

* The dataset contains **1000 students**.
* There are **no missing values**.
* Reading has the highest average score at **69.169**.
* Writing has an average score of **68.054**.
* Math has an average score of **66.089**.
* The median scores are 66 for Math, 70 for Reading, and 69 for Writing.
* Total Score was calculated by adding Math, Reading, and Writing scores.
* Percentage was calculated using the total score out of 300.

## 17. Project Workflow

The project was completed using the following steps:

1. Import required Python libraries.
2. Load the student performance dataset.
3. Display the dataset.
4. Check the first and last records.
5. Check the dataset shape.
6. Check the data types and information.
7. Check for missing values.
8. Calculate descriptive statistics.
9. Calculate mean, median, and mode.
10. Calculate standard deviation.
11. Calculate quartiles.
12. Calculate Total Score.
13. Calculate Percentage.
14. Analyze the results.

## 18. Conclusion

This project demonstrates how Python can be used to perform basic data analysis on student performance data.

Pandas was used for data loading, cleaning, statistical calculations, and creating new columns. NumPy, Matplotlib, and Seaborn were imported for numerical analysis and visualization.

The analysis provides a basic understanding of students' performance in Math, Reading, and Writing and demonstrates important data analysis techniques using Python.

## 19. How to Run the Project

1. Open **Google Colab**.
2. Upload `StudentsPerformance.csv`.
3. Make sure the file is available at:

```text
/content/StudentsPerformance.csv
```

4. Run the Python code cells.
5. View the output tables and analysis results.

## 20. Project Files

```text
Students-Performance-Analysis/
│
├── StudentsPerformance.csv
├── Students_Performance_Analysis.ipynb
└── README.md
```

## 21. Author

**Name:** S. Tharun Sasi

**Project:** Students Performance Analysis Using Python
