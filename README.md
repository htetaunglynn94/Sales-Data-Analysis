#  Sales Data Analysis Dashboard (Basic Power BI Project)

## 📌 Project Overview

This project analyzes retail store sales data using **Power BI** to uncover key business insights related to sales performance, profitability, discount strategies, and customer behavior.

The dashboard provides interactive visualizations to help stakeholders make data-driven decisions.

The objective of this project is to build and strengthen core Power BI competencies, including data preparation, data modeling, interactive visualization, and business reporting.

---

## 🎯 Business Requirements

The dashboard answers the following business questions:

1. Identify **Top/Bottom 5 products** by:

   * Sales
   * Profit
   * Quantity Sold

2. Analyze **sales trends over time**:

   * Daily
   * Monthly
   * Quarterly
   * Yearly

3. Understand the **relationship between Sales and Profit**

4. Compare **Sales / Profit / Quantity** between two selected periods

5. Analyze **average discount by category**

6. Calculate **total number of orders**

7. Provide **detailed order-level insights** with filters:

   * Product
   * Date
   * Customer ID
   * Promotion Category

8. Visualize **sales distribution by city**

---

##  Tools & Technologies

* **Power BI Desktop**
* **DAX (Data Analysis Expressions)**
* **Power Query (M Language)**
* **Excel (Data Source)**

---

## 📂 Resources

* Dataset: [Store Data.xlsx](https://github.com/user-attachments/files/26787074/Store.Data.xlsx)
  * Customers Dimension including:
    * Customer ID
    * Customer Name
    * City
    * State
    * Pincode
    * EmailID
    * Phone Number

  * Product Dimension including:
    * ProductID
    * Product Name
    * Product Line
    * Price (INR)

  * Promotion Dimension including:
    * PromotionID
    * Promotion Name
    * Ad Type
    * Coupon Code
    * Price Reduction Type

  * Sheet3 including:
    * Date (dd/mm/yyyy)
    * CustomerID
    * PromotionID
    * Product ID
    * Units Sold
    * Price Per Unit
    * Total Sales
    * Discount Percentage
    * Discount Value
    * Net Sales
* PowerBI: [Sales Data Analysis.pbix](https://app.powerbi.com/links/52sO74jm2m?ctid=35ae1710-01c9-4681-aee5-aefcb73885b1&pbi_source=linkShare)
---

## 📊 Key Features of Dashboard

* Interactive time-based analysis (Year → Quarter → Month → Day)
* Dynamic filtering using slicers
* Top & Bottom product performance tracking
* KPI cards for:

  * Total Sales
  * Total Profit
  * Total Orders
* Period comparison analysis
* Geographic visualization (Sales by City)

---

## 📌 Key Insights

### 1. Top & Bottom Products

* A small group of products contributes the majority of total sales (Pareto principle).
* Bottom-performing products show low profitability despite sales volume.

---

### 2. Sales Trends

* Sales show **seasonal patterns**, with peaks in specific months/quarters.
* Growth trend observed over time, indicating business expansion.

---

### 3. Sales vs Profit Relationship

* Strong positive correlation overall.
* However, some high-sales products generate **low or negative profit** due to high discounts.

---

### 4. Discount Impact

* Higher discount categories tend to reduce profit margins.
* Moderate discounts appear to balance **sales growth and profitability**.

---

### 5. Regional Performance

* Certain cities dominate total sales contribution.
* Opportunities exist to improve performance in underperforming regions.

---

### 6. Order Analysis

* High number of small-value orders suggests potential for upselling strategies.
* Customer segmentation could improve targeting.

---

##  Learnings

* Importance of **data modeling (Star Schema)**
* Difference between **Power Query vs DAX**
* Use of **CALCULATE, SUMX, ALL, ALLSELECTED**
* Building **interactive dashboards**
* Handling **time intelligence (MTD, YTD)**
* Some useful DAX functions are as per following

    ```DAX
    Date Table 1 = CALENDARAUTO()

    Quantity Sold = CALCULATE(SUM('Fact Table'[Units Sold]), ALL('Date Table 1'), 
                                    USERELATIONSHIP('Date Table 2'[Date], 'Fact Table'[Date (dd/mm/yyyy)]))
                    
                                    
    Sum of Net Sales = CALCULATE(SUM('Fact Table'[Net Sales]), ALL('Date Table 1'), 
                    USERELATIONSHIP('Date Table 2'[Date],'Fact Table'[Date (dd/mm/yyyy)]))
                    

    Total Profit = CALCULATE(SUM('Fact Table'[Profit]), ALL('Date Table 1'), 
                                    USERELATIONSHIP('Date Table 2'[Date],'Fact Table'[Date (dd/mm/yyyy)]))

    Sum Dim = SUM('Fact Table'[Net Sales])
    ```
---

## 🚀 Future Improvements

* Add **forecasting (time series)**
* Implement **customer segmentation (RFM analysis)**
* Optimize performance using **aggregations**
* Deploy dashboard to Power BI Service

---

## 📬 Contact

If you have any feedback or opportunities, feel free to connect!

* [LinkedIn](https://www.linkedin.com/in/htet-aung-lynn-64ba06146/)
* [GitHub](https://github.com/htetaunglynn94)

---
