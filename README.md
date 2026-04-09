# RetailChain Big Data Analytics Pipeline

A complete end-to-end big data analytics pipeline built for **RetailChain**, a national UK retailer,
using **PySpark** and **Plotly** in **Google Colab**. 
This project covers data ingestion, governance, KPI computation, interactive visualisation, drill-down analytics, and a self-contained HTML dashboard.


## Project Overview

This project was developed for the **COM7020 – Big Data and Cloud Computing** module.
It demonstrates how a cloud-style analytics workflow can be implemented for a retail business using distributed data processing and interactive business intelligence visualisations.

The pipeline simulates a real-world retail analytics environment by processing an **unbalanced synthetic UK retail dataset** and transforming it into meaningful insights for decision-makers.
## Objectives

The main objectives of this project are to:
- Build a complete **big data analytics pipeline**
- Process retail transaction data using **Apache Spark**
- Apply **data governance and quality checks**
- Compute business **KPIs**
- Generate **interactive dashboard visualisations**
- Create a **self-contained HTML dashboard**
- Support **drill-down analysis** from region to city level

## Tech Stack

- **Python**
- **PySpark**
- **Pandas**
- **Plotly**
- **ipywidgets**
- **Google Colab**

## Pipeline Architecture

The code is structured into multiple stages representing a modern analytics pipeline:

### Stage 1 – Installation and Imports
All required libraries are imported, including PySpark, Plotly, Pandas, and widget support for Colab.

### Stage 2 – Spark Session Initialisation
A Spark session is created to enable distributed data processing in local Colab mode.

### Stage 3 – Data Ingestion
The raw CSV dataset is loaded into Spark as the **Bronze Layer**, preserving the source data for auditability.

### Stage 4 – Data Quality and Standardisation
The governance layer transforms raw data into a cleaner **Silver Layer** by:

- Standardising column names
- Converting timestamps
- Cleaning numeric fields
- Creating derived fields
- Normalising discount flags
- Filtering invalid records
- Adding temporal columns
- Caching the clean dataset

### Stage 5 – KPI Computation
The analytics layer generates key business metrics including:

- Sales by customer segment
- Monthly sales trend
- Yearly sales trend
- Discount impact
- Channel performance
- Product category sales
- Regional sales
- Loyalty tier analysis
- Payment method analysis
- Channel-region cross analysis
- Price relationship sample
- Premium customer category deep-dive
- City-level sales aggregation

### Stage 6 – Interactive Dashboard Visualisations
The pipeline generates **12 interactive Plotly charts** such as:

- Sales by customer segment
- Monthly and yearly sales trends
- Discounted vs undiscounted sales
- Sales by channel
- Top product categories
- Regional sales distribution
- Loyalty tier performance
- Payment method analysis
- Channel-region comparison
- Scatter plot of unit price vs total price
- Premium customer category analysis

### Stage 7a – KPI Summary
Headline performance metrics are calculated and displayed, including:

- Total sales
- Total transactions
- Average transaction value
- Best customer segment
- Best region
- Best product category
- Discount sales share

### Stage 7b – Gauge Chart
A Plotly gauge chart is used to show total sales against a business revenue target.

### Stage 8 – Interactive Drill-Down
A dropdown widget allows users to select a region and drill down to city-level sales.

### Stage 9 – HTML Dashboard
A complete interactive HTML dashboard is generated and saved as a standalone file for sharing with stakeholders.

## Features

- End-to-end analytics workflow
- Big data processing using PySpark
- Data cleaning and governance layer
- Time-based partitioning
- Multiple KPI aggregations
- 15 total visual outputs
- Interactive region-to-city drill-down
- Professional self-contained HTML dashboard
- Business-friendly reporting structure

## Dataset

**Dataset Used:**  
`UK Retail Un-balance Synthetic Data Set.csv`

This dataset represents a synthetic UK retail environment with unbalanced data 
suitable for demonstrating the **5 Vs of Big Data** and real-world business analytics workflows.

## Key Business Insights Generated

The pipeline helps answer important business questions such as:

- Which customer segment drives the most revenue?
- How do monthly and yearly sales trends change over time?
- What share of revenue comes from discounted sales?
- Which product categories perform best?
- Which UK regions generate the highest sales?
- How do payment methods differ by sales contribution?
- Which cities are top performers within each region?
- How do premium customers behave compared to other segments?

## Output

The project produces:

- Cleaned Spark DataFrame
- Multiple KPI summary tables
- 12 interactive Plotly charts
- 1 gauge indicator chart
- 1 regional overview chart
- 1 city-level drill-down chart
- 1 integrated HTML dashboard

**Final HTML Output File:**  
`uk_retail_dashboard_COM7020.html`
