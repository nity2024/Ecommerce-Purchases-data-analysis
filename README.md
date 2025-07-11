﻿# Ecommerce-Purchases-data-analysis
# 📊 Ecommerce Purchases Data Analysis

This project performs an exploratory data analysis (EDA) on an ecommerce dataset of 10,000 customers. It extracts meaningful insights such as purchase behaviors, preferred payment methods, job titles, and more using Python libraries like Pandas, NumPy, and Matplotlib.

## 📁 Dataset Details

- **Rows:** 10,000
- **Columns:** 14
- **File Name:** `Ecommerce Purchases.csv`
- The dataset contains information such as:
  - Customer Address
  - Purchase Time (AM/PM)
  - Browser Info
  - Credit Card Details
  - Email and IP Address
  - Job Titles
  - Purchase Price

## 🛠️ Technologies Used

- **Python 3**
- **Pandas**
- **NumPy**
- **Matplotlib**

## ✅ Analysis Performed

- Displayed first and last 10 rows of the dataset
- Checked null values and datatypes
- Found:
  - Highest, lowest, and average purchase price
  - Number of French-speaking users
  - Number of customers with job title containing "engineer"
  - Email of a customer with specific IP and Credit Card number
  - Customers using Mastercard with purchases above $50
  - Number of purchases made in AM vs PM
  - Number of credit cards expiring in the year 2020
  - Top 5 most popular email domains

## 📈 Visualization

- Bar chart of the **Top 5 Email Providers** used by the customers.

## 📌 Sample Code Snippet

```python
# Top 5 email domains
top_providers = data['Email'].apply(lambda x: x.split('@')[1]).value_counts().head()
top_providers.plot(kind='bar', color='skyblue')
plt.title('Top 5 Email Providers')
plt.xlabel('Email Provider')
plt.ylabel('Number of Users')
plt.grid(True, axis='y')
plt.show()
