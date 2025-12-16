# E-Commerce Sales & Customer Analysis

## 🎯 Project Objective

Analyze real-world e-commerce data to uncover **revenue drivers, customer behavior, and growth opportunities** using Python and pandas. This project simulates a realistic analytics task commonly assigned to **data analysts, product analysts, and business intelligence roles**.

---

## 🧠 Business Questions

This analysis answers the following real-world questions:

1. What are the **total revenue and order volume trends** over time?
2. Which **products and categories** generate the most revenue?
3. Who are the **most valuable customers**?
4. What is the **repeat customer rate**?
5. How does **average order value (AOV)** change month over month?
6. When do sales **peak or drop**?

---

## 📊 Dataset Design

The project uses **multiple related datasets**, just like in real companies.

### 1️⃣ Customers (`customers.csv`)

| Column      | Description           |
| ----------- | --------------------- |
| customer_id | Unique customer ID    |
| signup_date | Account creation date |
| country     | Customer country      |

---

### 2️⃣ Orders (`orders.csv`)

| Column       | Description           |
| ------------ | --------------------- |
| order_id     | Unique order ID       |
| customer_id  | Links to customers    |
| order_date   | Date of purchase      |
| order_status | completed / cancelled |

---

### 3️⃣ Order Items (`order_items.csv`)

| Column     | Description       |
| ---------- | ----------------- |
| order_id   | Links to orders   |
| product_id | Product purchased |
| quantity   | Units bought      |
| price      | Price per unit    |

---

### 4️⃣ Products (`products.csv`)

| Column       | Description |
| ------------ | ----------- |
| product_id   | Product ID  |
| product_name | Name        |
| category     | Category    |

---

## 🛠️ Tools & Skills Used

* Python
* pandas
* numpy
* matplotlib / seaborn
* Jupyter Notebook
* Data cleaning & preprocessing
* Exploratory Data Analysis (EDA)
* Business insight generation

---

## 🧹 Data Cleaning Tasks

Realistic issues intentionally included:

* Missing customer countries
* Duplicate orders
* Inconsistent date formats
* Cancelled orders

Cleaning steps:

* Remove duplicates
* Parse and standardize dates
* Filter out cancelled orders
* Handle missing values

---

## 📈 Key Metrics Calculated

* Total Revenue
* Monthly Revenue
* Average Order Value (AOV)
* Orders per Customer
* Repeat Customer Rate
* Revenue by Product & Category

---

## 📊 Analysis Steps

### 1️⃣ Load & Inspect Data

* Check shapes, data types, missing values

### 2️⃣ Data Cleaning

* Fix dates
* Remove invalid records
* Create revenue column

### 3️⃣ Merge Datasets

* Join orders, customers, products, and order items

### 4️⃣ Exploratory Analysis

* Revenue trends
* Top products
* Customer segmentation

### 5️⃣ Visualization

* Monthly revenue line chart
* Top 10 products bar chart
* Revenue by category

---

## 📌 Sample Pandas Operations

```python
# Monthly revenue
monthly_revenue = df.groupby(df['order_date'].dt.to_period('M'))['revenue'].sum()

# Repeat customers
repeat_customers = df.groupby('customer_id')['order_id'].nunique()
repeat_rate = (repeat_customers > 1).mean()
```

---

## 📁 Project Structure

```
ecommerce-analysis/
 ├ data/
 │   ├ raw/
 │   └ cleaned/
 ├ notebooks/
 │   └ ecommerce_analysis.ipynb
 ├ reports/
 │   └ insights.md
 ├ README.md
```

---

## 📝 Final Deliverables

* Cleaned datasets
* Jupyter notebook with full analysis
* Business insights report
* Visualizations

---

## 💡 Key Insights (Example)

* 20% of customers generate 60% of revenue
* Repeat customers spend 2.3x more than one-time buyers
* Sales peak in Q4, suggesting seasonal demand

---

## 🚀 Business Recommendations

* Focus marketing on repeat customers
* Promote high-margin categories
* Prepare inventory ahead of peak months

---

## 🔮 Future Improvements

* Customer lifetime value (CLV)
* Predictive sales modeling
* Dashboard in Tableau or Power BI
* Cohort retention analysis

---

## 📄 License

MIT License
