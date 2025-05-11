# Marketing Analytics

## Project Overview

This project focuses on analyzing marketing data using SQL queries and Python scripts. It is designed to extract, transform, and analyze customer and product data from a SQL Server database. Future iterations of this project will incorporate Power BI for detailed data visualization (planned for Review 2).

This documentation is for **Review 1**, which includes SQL Server Management Studio, SQL queries, and Python for data analysis.

---

## Project Setup

### Requirements

1. **Database**
   - SQL Server Management Studio (SSMS) is used for running SQL queries.
   - You need a database named `MarketingAnalytics` with the following tables:
     - `dbo.products`
     - `dbo.customers`
     - `dbo.geography`
     - `dbo.engagement_data`
     - `dbo.customer_journey`
     - `dbo.customer_reviews`

2. **Python Environment**
   - Python 3.x
   - Libraries:
     - `pandas`
     - `pyodbc`
     - `nltk`
     - `sqlalchemy`

3. **Others**
   - Ensure that your SQL Server is configured to allow trusted connections.
   - Install the `VADER` SentimentIntensityAnalyzer for sentiment analysis (provided by the `nltk` library).

---

## How to Run the Project

### Step 1: Database Setup

1. Install SQL Server and SQL Server Management Studio (SSMS).
2. Create the `MarketingAnalytics` database and populate the following tables:
   - `products`
   - `customers`
   - `geography`
   - `engagement_data`
   - `customer_journey`
   - `customer_reviews`
3. Execute the SQL scripts in the following order:
   - `dim_products.sql` - Categorizes products based on price.
   - `dim_customers.sql` - Enriches customer data with geographic information.
   - `fact_engagement_data.sql` - Cleans and normalizes engagement data.
   - `fact_customer_journey.sql` - Identifies and removes duplicate customer journey records.
   - `fact_customer_reviews.sql` - Cleans customer reviews by standardizing text.

### Step 2: Python Script Execution

1. Clone the repository:
   ```bash
   git clone https://github.com/Aafi04/Marketing-Analytics.git
   cd Marketing-Analytics
   ```
2. Install the required Python libraries:
   ```bash
   pip install pandas pyodbc nltk sqlalchemy
   ```
3. Run the Python script:
   ```bash
   python customer_reviews_enrichment.py
   ```
   - This script connects to the `MarketingAnalytics` database, fetches customer reviews data, performs sentiment analysis, and saves the results as `fact_customer_reviews_with_sentiment.csv`.

---

## Future Enhancements (Review 2)

- **Power BI Integration**: Visualize the cleaned and enriched data using Power BI dashboards.
- Additional data sources and advanced analytics.

---

I will now finalize this README by analyzing the code in detail to ensure completeness. Let me know if you would like any modifications.