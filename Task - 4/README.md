# Shopify Stock Analysis Using Python

## 1. Project Overview

This project analyzes the historical stock price data of **Shopify** using Python. The dataset contains daily stock information such as opening price, highest price, lowest price, closing price, adjusted closing price, and trading volume.

The main purpose of this project is to understand the movement of Shopify's stock price and analyze its daily returns using different visualizations.

## 2. Dataset

The dataset used in this project is:

`shopify_stock.csv`

It contains the following columns:

| Column    | Description                  |
| --------- | ---------------------------- |
| date      | Date of the stock record     |
| open      | Opening stock price          |
| high      | Highest price during the day |
| low       | Lowest price during the day  |
| close     | Closing stock price          |
| adj_close | Adjusted closing price       |
| volume    | Number of shares traded      |

## 3. Technologies Used

* Python
* Pandas
* Matplotlib
* Seaborn
* Google Colab

## 4. Libraries Used

The following Python libraries were used:

```python
import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns
```

## 5. Loading the Dataset

The Shopify stock dataset was loaded using Pandas.

```python
df = pd.read_csv("/content/shopify_stock.csv")
```

The `head()` function was used to display the first five records.

```python
df.head()
```

## 6. Data Preprocessing

The `date` column was converted into a proper datetime format.

```python
df['date'] = pd.to_datetime(df['date'], utc=True)
```

This makes it easier to use the date column for time-based analysis and visualization.

## 7. Closing Price Analysis

A line plot was created to observe how Shopify's closing stock price changed over time.

```python
plt.figure(figsize=(8, 5))
sns.lineplot(x='date', y='close', data=df)
plt.title('Shopify Closing Price Over Time')
plt.xlabel('Date')
plt.ylabel('Closing Price')
plt.grid(True)
plt.show()
```

### Observation

The line graph helps identify the overall movement of Shopify's stock price over the given period. It also shows periods where the stock price increased or decreased significantly.

## 8. Daily Return Calculation

Daily return was calculated using the percentage change in the closing price.

```python
df['Daily_Return'] = df['close'].pct_change()
```

The first value becomes `NaN` because there is no previous day's closing price available for comparison.

## 9. Daily Return Distribution

A histogram with KDE was created to understand the distribution of Shopify's daily returns.

```python
plt.figure(figsize=(6, 5))
sns.histplot(df['Daily_Return'].dropna(), bins=60, kde=True, color='darkred')
plt.title('Shopify Daily Returns')
plt.xlabel('Daily Return')
plt.ylabel('Frequency')
plt.grid(True)
plt.show()
```

### Observation

The histogram shows how frequently different daily return values occurred. Most daily returns are generally concentrated around zero, while larger positive or negative returns occur less frequently.

## 10. KDE Plot

A KDE (Kernel Density Estimate) plot was created to show the smooth distribution of daily returns.

```python
plt.figure(figsize=(10, 6))
sns.kdeplot(df['Daily_Return'].dropna(), fill=True, color='blue')
plt.title('KDE of Shopify Daily Returns')
plt.xlabel('Daily Return')
plt.ylabel('Density')
plt.grid(True)
plt.show()
```

### Observation

The KDE plot provides a smooth representation of the distribution of daily returns. It helps identify where daily returns are most concentrated and how widely they are spread.

## 11. Project Workflow

The analysis was performed using the following steps:

1. Import the required Python libraries.
2. Load the Shopify stock dataset.
3. Display the first few records.
4. Convert the date column into datetime format.
5. Visualize the closing stock price over time.
6. Calculate daily returns.
7. Plot the distribution of daily returns using a histogram.
8. Create a KDE plot for daily returns.
9. Observe the patterns in stock prices and returns.

## 12. Key Findings

* Shopify's closing price changes over time and shows different periods of growth and decline.
* Daily returns help measure the percentage change in stock price from one trading day to the next.
* Most daily returns are concentrated around a relatively small range.
* Large daily price changes occur less frequently.
* The KDE plot provides a clearer view of the overall distribution of daily returns.

## 13. Conclusion

This project demonstrates how Python can be used to perform basic stock market data analysis. Pandas was used for data loading and preprocessing, while Matplotlib and Seaborn were used for visualization.

The analysis of closing prices and daily returns provides a simple way to understand Shopify's historical stock behavior and return distribution.

## 14. How to Run the Project

1. Open **Google Colab**.
2. Upload `shopify_stock.csv`.
3. Make sure the file is available at:

```text
/content/shopify_stock.csv
```

4. Run the Python code cells.
5. View the generated graphs and observations.

## 15. Project Files

```text
Shopify-Stock-Analysis/
│
├── shopify_stock.csv
├── Shopify_Stock_Analysis.ipynb
└── README.md
```

##
