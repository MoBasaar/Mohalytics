##  1. Data Cleaning and Standardization

The dataset was cleaned and standardized using SQL to ensure consistency, remove duplicates, and improve data quality. The following steps were undertaken:

## 1.1. Database and Table Setup

Created a new database (amazon) and structured tables (sales and sales2).

Defined appropriate data types for each column.

Checked table structures using DESCRIBE.

## 1.2. Data Loading and Duplicate Removal

Loaded data from a CSV file into sales2.

Used ROW_NUMBER() to identify duplicate records based on order_id, sku, date, and status.

Deleted duplicate records from the sales table.

## 1.3. Date Formatting

Identified inconsistent date formats (%m-%d-%y and %m/%d/%Y).

Standardized the date column using STR_TO_DATE() and modified the column type to DATE.

Filtered the dataset to include only Q4 data (dates after 2022-04-01).

## 1.4. Handling Missing Values

Checked for NULL values across key columns.

Updated missing currency values to 'INR'.

Converted amount values from INR to AUD by multiplying by 0.018.

## 1.5. Standardizing Categorical Columns

Recategorized status values:

Merged various shipped statuses into 'Shipped'.

Grouped shipping-related issues under 'Shipping Issues'.

Consolidated pending statuses under 'Pending'.

Standardized b2b values: 'TRUE' → 'Business', else 'Consumer'.

Simplified category values by grouping ethnic wear into 'Ethnic Dress'.

## 1.6. Removing Unnecessary Columns

Dropped columns that were not useful for analysis, including courier_status, asin, fulfilled_by, and sales_channel (since over 99% of transactions occurred through the same channel).

## 1.7. Final Data Validation

Verified data integrity by checking value distributions across key columns.

Ensured that no missing or erroneous data remained.

The final dataset is now standardized and optimized for further analysis.



## 2. E-Commerce Sales Dashboard
### 2.1. Overview
This E-Commerce Sales Dashboard provides valuable insights into revenue performance, product trends, and customer order behavior. It analyzes sales data across different product categories, fulfillment types, and service levels to help businesses make data-driven decisions.
### 2.2. Problem Statement
Managing e-commerce sales efficiently requires continuous monitoring of key metrics like total revenue, order cancellations, and returns. Without a clear view of these insights, businesses may struggle with inventory management, profitability, and customer satisfaction. This dashboard addresses these challenges by offering an interactive, real-time visualization of sales performance.
### 2.3. Features
•	Total Revenue Overview: Displays total revenue generated within a specific timeframe.
•	Revenue Breakdown by Category: Helps businesses understand which product categories contribute the most to sales.
•	Top 10 Products by Revenue: Identifies best-selling products to optimize stock levels and marketing efforts.
•	Revenue Trend Analysis: Tracks revenue fluctuations over time to detect seasonal trends and performance shifts.
•	Service Type & Fulfillment Analysis: Compares sales based on shipping methods and fulfillment sources.
•	Cancellation & Return KPIs: Monitors the percentage of cancelled and returned orders, highlighting potential loss.
•	Geographical Revenue Distribution: Visualizes sales performance by state using a dynamic map.
•	Interactive Filters: Users can filter data based on business type, promotion, state, and style preferences.

### 2.4. Data Insights
•	Sales Performance: The majority of revenue comes from "Set" and "Ethnic Dress" categories, with "Western Dress" following.
•	Product Demand: The highest-selling product (JNE3797) significantly outperforms others, indicating strong demand.
•	Order Cancellations: Cancellation rates are 14.22%, leading to a loss of over $214K, which requires further investigation.
•	Returns Impact: The return rate is 1.63%, resulting in a $24.78K loss, showing that most orders are successfully completed.
•	Regional Performance: Certain regions, such as New Delhi, contribute significantly to revenue, while others show lower engagement.

### 2.5. How to Use
1.	Explore Key Metrics: Review total revenue, top product categories, and cancellation trends.
2.	Use Filters for Custom Views: Adjust filters for business type, promotions, and location to get a focused analysis.
3.	Monitor Trends Over Time: Use the revenue trend graph to identify sales peaks and dips.
4.	Investigate High Cancellation & Return Rates: Track patterns to reduce revenue loss and improve fulfillment processes.
5.	Analyze Geographic Performance: Assess which states contribute the most to sales and adjust marketing strategies accordingly.

### 2.6. How It Helps Stakeholders
•	Sales & Marketing Teams: Identify top-performing products and regions to optimize promotions and campaigns.
•	Inventory Managers: Monitor demand trends and reduce stock shortages or overstocking.
•	Operations & Fulfillment Teams: Improve shipping and fulfillment strategies based on customer preferences.
•	Finance & Strategy Leaders: Track revenue growth, losses due to cancellations/returns, and make data-driven decisions.

### 2.7. Technical Details
•	Built with: Power BI
•	Data Sources: SQL/Excel/API (depending on setup)
•	Data Refresh: Real-time or scheduled updates

### 2.8. Contact
For any inquiries, reach out via m.basaar@gmail.com


