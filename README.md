# 📊 Data Warehouse Design for Reporting & OLAP

## 📌 Project Overview
This project demonstrates the design and implementation of a **Data Warehouse (DWH)** for analytical reporting and OLAP (Online Analytical Processing).

It follows a complete end-to-end data pipeline:

**Staging → Operational Data Store (ODS) → Data Warehouse (DWH) → Reporting Layer**

The project integrates **Yelp business datasets** with **climate data (temperature and precipitation)** to generate analytical insights such as correlations between weather conditions and business performance.

---

## 🏗 Architecture Overview

- **Staging Layer**: Raw ingestion of JSON/CSV files  
- **ODS (Operational Data Store)**: Cleaned and structured data  
- **DWH (Data Warehouse)**: Star schema for analytics  
- **Reporting Layer**: Business insights and OLAP queries  

---

## 📁 Project Structure

```

data-warehouse-project/
│
├── README.md                # Project overview and documentation
├── docs/
│   ├── Submission_Document.md   # Detailed submission document
│   ├── diagrams/                # Architecture, ER, and star schema diagrams
│   └── screenshots/             # Evidence screenshots
│
├── sql/
│   ├── staging_to_ods.sql       # Transform staging → ODS
│   ├── json_transform.sql       # JSON flattening queries
│   ├── ods_to_dwh.sql           # Load ODS → DWH
│   ├── integration_queries.sql  # Climate + Yelp integration
│   └── reporting_queries.sql    # Reporting queries

```




---

## 📂 Data Sources

### Yelp Dataset
- Business data  
- Reviews  
- Check-ins  
- Tips  
- Customer data  
- COVID impact data  

### Climate Dataset
- Temperature data  
- Precipitation data  

---

## 🔄 Data Pipeline

### 1. Staging Layer
Raw data ingestion from multiple sources (Yelp + Climate).

### 2. Operational Data Store (ODS)
- Data cleaning and normalization  
- JSON flattening into structured columns  
- Relationship mapping  

### 3. Data Warehouse (DWH)
Star schema design:

- **Fact Table**: Business performance metrics  
- **Dimensions**:
  - Business
  - Time
  - Weather
  - Location
  - Customer  

### 4. Reporting Layer
Analytical insights such as:
- Business performance vs temperature  
- Business performance vs precipitation  
- Rating trends under weather conditions  

---

## 🚀 How to Run

### 1. Clone Repository
```bash
git clone https://github.com/your-username/data-warehouse-reporting-OLAP.git
```

## 2. Navigate to Project

```
cd data-warehouse-reporting-OLAP
```

## 3. Run SQL Scripts (Snowflake)
```
`snowsql -f sql/staging_to_ods.sql
snowsql -f sql/json_transform.sql
snowsql -f sql/ods_to_dwh.sql
snowsql -f sql/integration_queries.sql
snowsql -f sql/reporting_queries.sql
```
# 🛠 Tools & Technologies
- ❄️ Snowflake – Cloud Data Warehouse
- 🖥 SnowSQL – SQL execution CLI
- 📊 Draw.io / Lucidchart – Data modeling
- 🐙 GitHub – Version control

# 📈 Key Features
- End-to-end ETL pipeline
- JSON data transformation
- Star schema design for OLAP
- Integration of Yelp + Climate datasets
- Analytical reporting layer

# 🎯 Learning Outcomes
- Data warehouse architecture design
- ETL pipeline implementation
- JSON parsing and transformation
- Star schema modeling
- OLAP reporting and analytics
# 📸 Evidence
- Screenshots: docs/screenshots/
- Diagrams: docs/diagrams/



