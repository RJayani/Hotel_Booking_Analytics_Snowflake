# Hotel Booking Analytics Pipeline using Snowflake & Power BI

This project demonstrates an end-to-end data analytics pipeline built using Snowflake for data processing and Power BI for visualization. The goal of this project is to simulate a real-world data engineering workflow using the Medallion Architecture (Bronze → Silver → Gold) and create business-ready dashboards.

## Project Overview

Raw hotel booking data was ingested into Snowflake, cleaned and transformed using SQL, and then aggregated into analytical tables. These Gold-layer tables were finally connected to Power BI to create an interactive dashboard showing key business metrics.

## Architecture Used: Medallion Pattern:

### Bronze Layer (Raw Ingestion):
- **Raw CSV loaded into Snowflake using File Formats, Internal Stages, COPY INTO**
- **No transformations applied**
- **All columns stored as STRING**

### Silver Layer (Cleaned & Standardized):
- **Data cleaning and transformation logic**
         - *  Trimmed and standardized text fields
         - *  Fixed invalid or missing emails
         - *  Converted string dates to DATE format
         - *  Removed invalid date ranges
         - *  Converted numeric fields to proper types
         - *  Corrected typos in booking status
         - *  Removed negative values from revenue

### Gold Layer (Analytics & KPIs):
- ** Aggregated tables created for analytics and dashboards**:
           - *  Daily Booking Revenue
           - *  Revenue by City
           - *  Monthly Revenue & Bookings
           - *  Bookings by Status
           - *  Bookings by Room Type
           - *  These tables are optimized for BI tools and business consumption.
