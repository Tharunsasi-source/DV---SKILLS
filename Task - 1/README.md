# Superstore Sales Data Understanding, Cleaning & Exploratory Analysis

##  Project Overview

This project focuses on understanding, cleaning, and performing Exploratory Data Analysis (EDA) on the **Superstore Sales Dataset** using **Python** and **Pandas**. The objective is to prepare the dataset for further analysis by handling date formats, cleaning categorical data, and generating descriptive statistics.

---

##  Objectives

* Load the Superstore Sales dataset using Pandas.
* Inspect the dataset structure and data types.
* Convert **Order Date** and **Ship Date** into proper datetime format.
* Clean and standardize categorical text columns.
* Generate summary statistics for numerical columns.
* Understand the dataset before advanced analysis.

---

##  Technologies Used

* Python 3.x
* Pandas
* Jupyter Notebook / VS Code

---

##  Dataset

The dataset contains information about customer orders from a retail superstore, including:

* Order ID
* Order Date
* Ship Date
* Customer Details
* Segment
* Category
* Sub-Category
* Sales
* Quantity
* Discount
* Profit
* Region
* State
* City

---

##  Project Workflow

### 1. Load the Dataset

* Import the dataset using Pandas.
* Display the first few rows using:

  ```python
  df.head()
  ```

---

### 2. Understand the Dataset

Inspect the dataset using:

* `df.info()`
* `df.describe()`
* `df.head()`

These functions help identify:

* Number of rows and columns
* Data types
* Missing values
* Statistical summary of numerical columns

---

### 3. Convert Date Columns

Convert the following columns into datetime format:

* Order Date
* Ship Date

Example:

```python
df["Order Date"] = pd.to_datetime(df["Order Date"])
df["Ship Date"] = pd.to_datetime(df["Ship Date"])
```

---

### 4. Clean Categorical Data

Standardize text formatting in columns such as:

* Category
* Sub-Category
* Segment

Cleaning includes:

* Removing leading/trailing spaces
* Standardizing capitalization
* Ensuring consistent formatting

Example:

```python
df["Category"] = df["Category"].str.strip().str.title()
```

---

### 5. Generate Summary Statistics

Calculate descriptive statistics for numerical columns using:

```python
df.describe()
```

Statistics include:

* Count
* Mean
* Standard Deviation
* Minimum
* Maximum
* Quartiles (25%, 50%, 75%)

---

##  Expected Output

After completing the analysis, the dataset will have:

* Proper datetime columns
* Clean and standardized categorical values
* Basic statistical summary of numerical data
* Better understanding of dataset quality and structure

---

##  Project Structure

```
Superstore-Sales-EDA/
│
├── Superstore_Sales.csv
├── Superstore_Sales_EDA.ipynb
├── README.md
```

---

## ▶️ How to Run

1. Clone the repository:

   ```bash
   git clone https://github.com/your-username/Superstore-Sales-EDA.git
   ```

2. Navigate to the project folder:

   ```bash
   cd Superstore-Sales-EDA
   ```

3. Install the required packages:

   ```bash
   pip install pandas
   ```

4. Open the Jupyter Notebook or run the Python script.

---

##  Learning Outcomes

By completing this project, you will learn how to:

* Import datasets using Pandas
* Explore dataset structure
* Convert string dates into datetime objects
* Clean categorical data
* Generate descriptive statistics
* Prepare datasets for further analysis and visualization

---

## Future Enhancements

* Handle missing values and duplicates
* Detect and treat outliers
* Perform advanced Exploratory Data Analysis (EDA)
* Create visualizations using Matplotlib and Seaborn
* Build sales dashboards
* Perform sales forecasting using Machine Learning

---

## 👨‍💻 Author

** S. Tharun Sas i**

BCA Student 
