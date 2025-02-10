##  Data Cleaning and Standardization

The dataset was cleaned and standardized using SQL to ensure consistency, remove duplicates, and improve data quality. The following steps were undertaken:

## 1. Database and Table Setup

Created a new database (amazon) and structured tables (sales and sales2).

Defined appropriate data types for each column.

Checked table structures using DESCRIBE.

## 2. Data Loading and Duplicate Removal

Loaded data from a CSV file into sales2.

Used ROW_NUMBER() to identify duplicate records based on order_id, sku, date, and status.

Deleted duplicate records from the sales table.

## 3. Date Formatting

Identified inconsistent date formats (%m-%d-%y and %m/%d/%Y).

Standardized the date column using STR_TO_DATE() and modified the column type to DATE.

Filtered the dataset to include only Q4 data (dates after 2022-04-01).

## 4. Handling Missing Values

Checked for NULL values across key columns.

Updated missing currency values to 'INR'.

Converted amount values from INR to AUD by multiplying by 0.018.

## 5. Standardizing Categorical Columns

Recategorized status values:

Merged various shipped statuses into 'Shipped'.

Grouped shipping-related issues under 'Shipping Issues'.

Consolidated pending statuses under 'Pending'.

Standardized b2b values: 'TRUE' → 'Business', else 'Consumer'.

Simplified category values by grouping ethnic wear into 'Ethnic Dress'.

## 6. Removing Unnecessary Columns

Dropped columns that were not useful for analysis, including courier_status, asin, fulfilled_by, and sales_channel (since over 99% of transactions occurred through the same channel).

## 7. Final Data Validation

Verified data integrity by checking value distributions across key columns.

Ensured that no missing or erroneous data remained.

The final dataset is now standardized and optimized for further analysis.
