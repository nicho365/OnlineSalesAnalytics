#  Online Sales Performance Analysis

[![Tableau Dashboard](https://img.shields.io/badge/Tableau-Interactive_Dashboard-E97627?style=for-the-badge&logo=tableau)](https://public.tableau.com/app/profile/nicholas.calvin7573/viz/P0M1_nicholas_calvin/Dashboard1?publish=yes)
[![Python](https://img.shields.io/badge/Python-Data_Analysis-3776AB?style=for-the-badge&logo=python)](https://github.com/nicho365/OnlineSalesAnalytics/blob/main/P0M1_nicholas_calvin.ipynb)

---

##  Project Background
This project was developed to help a client resolve inconsistencies in their online sales performance across various product categories, regions, and payment methods. 

**SMART Goal:**
Optimize sales strategies in underperforming payment types and untapped regional markets to achieve a more equalized sales distribution and an overall revenue increase of **>1%** over the next year.

**Business Questions (5W+1H):**
* What causes the performance gap between regions, payment methods, and categories?
* Where are the data disparities located?
* When did the uneven sales distribution occur?
* How can we optimize the current strategy to resolve this?

---

##  Dataset Overview
The dataset contains 240 transactions from 2024 with zero missing values and no duplicates. Dataset provides comprehensive overview of online sales transactions across different product categories. Each row represents a single transaction with detailed information such as the order ID, date, category, product name, quantity sold, unit price, total price, region, and payment method. 
* **Source:** [Online Sales Dataset - Kaggle](https://www.kaggle.com/datasets/shreyanshverma27/online-sales-dataset-popular-marketplace-data?resource=download)
* **Key Columns:**
  1. `Order ID`: Unique identifier for each sales order.
  2. `Date`    :Date of the sales transaction.
  3. `Category`:Broad category of the product sold (e.g., Electronics, Home Appliances, Clothing, Books, Beauty Products, Sports).
  4. `Product Name` :Specific name or model of the product sold.
  5. `Quantity`:Number of units of the product sold in the transaction.
  6. `Unit Price`:Price of one unit of the product.
  7. `Total Price`: Total revenue generated from the sales transaction (Quantity * Unit Price).
  8. `Region`  :Geographic region where the transaction occurred (e.g., North America, Europe, Asia).
  9. `Payment Method`: Method used for payment (e.g., Credit Card, PayPal, Debit Card).

---

##  Tools & Technologies
* **Data Manipulation:** Python (Pandas, NumPy)
* **Data Visualization:** Matplotlib, Seaborn, Tableau
* **Statistical Analysis:** SciPy (Chi-Square Contingency Test)

---

##  Key Insights & Exploratory Data Analysis (EDA)

###  1. Revenue Trends
* Total revenue saw a downward trend from **January to July 2024**, followed by a slight recovery in August.

###  2. Regional Performance
* **Transaction Volume:** North America, Europe, and Asia all recorded the exact same number of transactions (**80 transactions each**).
* **Revenue Disparity:** Despite equal transaction volumes, **North America** generated the highest average revenue (**$460.55**), driven heavily by high-value electronics. Asia ($280.69) and Europe ($265.85) followed with much lower averages.

###  3. Product Category Distribution
* **Top Revenue Generator:** `Electronics` dominates the market with a massive average revenue of **$874.56** and high variance (prices ranging from $99.99 to $3,899.99).
* **Underperformers:** `Beauty Products` ($65.55) and `Books` ($46.55) showed the lowest revenue contributions.

###  4. Payment Method Preferences
* **Credit Cards** are the primary choice for high-value transactions (average **$426.42**).
* **Debit Cards** are used for smaller, routine purchases (average **$203.22**).

---

##  Statistical Hypothesis Testing
To find the root cause of the regional revenue disparity, a **Chi-Square Contingency Test** was performed between `Product Category` and `Region`.

* **Null Hypothesis (H0):** There is NO relationship between Product Category and Region.
* **Alternative Hypothesis (H1):** There IS a relationship between Product Category and Region.
* **Result:** `P-value = 8.26e-97`
* **Conclusion:** Because the P-value is significantly lower than 0.05, we successfully reject H0. There is a strong dependency between the product category and the region it is sold in (e.g., certain categories are heavily region-locked), which is the primary cause of the revenue inequality.

---

##  Interactive Dashboard
You can explore the interactive data visualizations on Tableau Public:

**[🔗 Click Here to View the Tableau Dashboard](https://public.tableau.com/app/profile/nicholas.calvin7573/viz/P0M1_nicholas_calvin/Dashboard1?publish=yes)**

---

##  Business Recommendations
1. **Unlock Region-Locked Products:** The statistical test proved that the massive revenue gap is caused by region-specific product offerings. To hit the >1% growth target, high-value products like *Electronics* and *Home Appliances* must be expanded into the European and Asian markets.
2. **Promote Daily-Use Items:** Simultaneously, push marketing campaigns for *Books* and *Clothing* in North America to balance the transaction spread.
3. **Payment Method Promos:** Offer localized Credit Card installment promos in Asia and Europe to encourage customers to purchase higher-value items.
