📊 Data Warehouse Design for Reporting & OLAP
📌 Project Overview

This project demonstrates the design and implementation of a Data Warehouse (DWH) for analytical reporting and OLAP (Online Analytical Processing).

It follows a complete end-to-end data pipeline:

Staging → Operational Data Store (ODS) → Data Warehouse (DWH) → Reporting Layer

The project integrates Yelp business datasets with climate data (temperature & precipitation) to generate analytical insights such as correlations between weather conditions and business performance.

🏗 Architecture Overview

The data pipeline is structured as follows:

Staging Layer: Raw ingestion of JSON/CSV files
ODS (Operational Data Store): Cleaned, structured, and normalized data
DWH (Data Warehouse): Dimensional model (Star Schema)
Reporting Layer: Aggregated analytical queries and insights
📁 Project Structure
data-warehouse-project/
│
├── README.md                      # Project documentation
├── docs/
│   ├── Submission_Document.md     # Full project report
│   ├── diagrams/                  # Architecture & schema diagrams
│   └── screenshots/              # Execution evidence
│
├── sql/
│   ├── staging_to_ods.sql        # ETL: Staging → ODS
│   ├── json_transform.sql        # JSON flattening queries
│   ├── ods_to_dwh.sql            # ETL: ODS → DWH
│   ├── integration_queries.sql   # Yelp + Climate integration
│   └── reporting_queries.sql     # Analytical reporting queries
📂 Data Sources
Yelp Dataset
Business data
Reviews
Check-ins
Tips
Customer data
COVID-related business impact data
Climate Dataset
Temperature records
Precipitation data
🔄 Data Pipeline
1. Staging Layer
Raw ingestion of 8 datasets (Yelp + Climate)
Data stored without transformation
2. Operational Data Store (ODS)
Data cleaning and normalization
JSON flattening into structured columns
Relationship mapping between entities
3. Data Warehouse (DWH)
Star schema design:
Fact Table: Business Performance Metrics
Dimensions: Business, Time, Weather, Location, Customer
Optimized for OLAP queries
4. Reporting Layer
Analytical queries for insights such as:
Business performance vs temperature
Business performance vs precipitation
Rating trends under different climate conditions
🧱 Schema Design
Star Schema Components
Fact Table
Business performance metrics (ratings, check-ins, reviews)
Dimension Tables
Business Dimension
Time Dimension
Weather Dimension
Location Dimension
Customer Dimension
🚀 How to Run
1. Clone Repository
git clone https://github.com/your-username/data-warehouse-reporting-OLAP.git
2. Navigate to Project
cd data-warehouse-reporting-OLAP
3. Execute SQL Scripts (Snowflake)
snowsql -f sql/staging_to_ods.sql
snowsql -f sql/json_transform.sql
snowsql -f sql/ods_to_dwh.sql
snowsql -f sql/integration_queries.sql
snowsql -f sql/reporting_queries.sql
🛠 Tools & Technologies
❄️ Snowflake – Cloud Data Warehouse
🖥 SnowSQL – CLI for executing SQL scripts
📊 Draw.io / Lucidchart – Data modeling & architecture diagrams
🐙 GitHub – Version control
📈 Key Features
End-to-end ETL pipeline (Staging → ODS → DWH)
JSON data flattening and transformation
Integration of structured + semi-structured datasets
Star schema design for OLAP optimization
Cross-domain analytics (Yelp + Climate data)
🎯 Learning Outcomes
Designing scalable data warehouse architectures
Implementing ETL pipelines in SQL
Working with semi-structured JSON data
Building star schemas for OLAP systems
Performing cross-domain analytical integration
📸 Evidence & Screenshots

All execution outputs and diagrams are available in:

docs/screenshots/
docs/diagrams/
