# E-Commerce Sales Dashboard (Power BI)

This project is a comprehensive sales analysis of an e-commerce dataset. An interactive dashboard was built from scratch using Power BI to visualize key performance indicators (KPIs) and derive actionable insights.

The dashboard provides a high-level overview of sales, profit, and quantity sold, and allows for deeper analysis by category, location, and payment method.

## Dashboard Preview

Here is a look at the final sales dashboard:

<img width="1438" height="807" alt="Screenshot 2025-10-26 072728" src="https://github.com/user-attachments/assets/b5971fde-04e3-430a-90a5-7945d7846782" />


### Key Insights from the Dashboard:
* **Overall Performance:** The store achieved **$4.17M in Sales** and **$0.19M in Profit** from **10,000 orders**.
* **Category Analysis:**
    * **Furniture** is the most profitable category.
    * **Clothing** is operating at a loss (negative profit), indicating a need for a price or cost review.
    * **Electronics** drives significant sales but has a relatively low profit margin.
* **Geographical Sales:** **Maharashtra** is the top-performing state, generating the most sales.
* **Payment Methods:** **Cash on Delivery (COD)** is the most popular payment mode, followed by UPI and Credit Card.

---

## Process & Key Learnings

This project was built following a standard data analysis workflow:

### 1. Data Source

The dataset was provided in two separate CSV files:
* `Orders.csv`: Contains order-level information, including `Order ID`, `Order Date`, and customer location (`State`, `City`).
* `Details.csv`: Contains transaction-level details, including `Order ID`, `Amount` (Sales), `Profit`, `Quantity`, `Category`, and `PaymentMode`.

### 2. Data Transformation and Modeling (Power Query)

The data was loaded into Power BI and processed using the Power Query Editor.

* **Merging Queries:** The primary transformation step was to **merge** the `Orders` and `Details` tables. This was done using the common `Order ID` column to create a single, unified table for analysis. This step combined the customer's location data with their purchase details.
* **Data Cleaning:** Checked for and handled any null values or inconsistencies (though not explicitly shown, this is a standard step).


### 3. DAX Calculations

Data Analysis Expressions (DAX) were used to create the key measures for the dashboard's KPI cards and visuals:
* `Total Sales = SUM(Merge1[Amount])`
* `Total Profit = SUM(Merge1[Profit])`
* `Total Quantity = SUM(Merge1[Quantity])`
* `Total Orders = DISTINCTCOUNT(Merge1[Order ID])`

### 4. Data Visualization

A variety of visuals were used to tell a clear story:
* **KPI Cards:** For at-a-glance metrics (Sales, Profit, Quantity, Orders).
* **Bar Chart:** To compare Sales, Profit, and Quantity by `Category`.
* **Treemap:** To visualize the contribution of different `Sub-Category` items to sales.
* **Donut Chart:** To show the breakdown of `PaymentMode` usage.
* **Map:** To display `Sales by State` geographically.

### Summary of Skills
Through this project, I gained hands-on experience in:
* **ETL Process:** Using **Power Query** to extract, transform (merge, clean), and load data.
* **Data Modeling:** Creating relationships between tables (in this case, by merging them into a single fact table).
* **DAX Formulas:** Writing measures to create powerful, dynamic calculations.
* **Data Visualization:** Selecting the appropriate charts to answer specific business questions.
* **Dashboard Design:** Creating an interactive and easy-to-understand dashboard using filters and slicers.
