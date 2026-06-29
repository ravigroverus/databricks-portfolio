# 🏗️ Databricks Data Engineering Portfolio
**Ravi Grover | Cloud Data Engineer | Databricks Certified Data Engineer Associate (2026)**

![Databricks](https://img.shields.io/badge/Databricks-FF3621?style=flat&logo=databricks&logoColor=white)
![Delta Lake](https://img.shields.io/badge/Delta_Lake-003366?style=flat&logo=delta&logoColor=white)
![PySpark](https://img.shields.io/badge/PySpark-E25A1C?style=flat&logo=apachespark&logoColor=white)
![AWS](https://img.shields.io/badge/AWS-232F3E?style=flat&logo=amazonaws&logoColor=white)
![Unity Catalog](https://img.shields.io/badge/Unity_Catalog-1B3A57?style=flat&logo=databricks&logoColor=white)

10+ years IT and data experience | 6+ years Data Engineering on Databricks Lakehouse  
Currently: Cloud Data Engineer @ eSyber Solutions | Previously: CMA CGM, Hapag-Lloyd, CSAV/Norgistics  
📧 ravigroverus@gmail.com | 📍 Tomball/Spring, TX | 🇺🇸 US Citizen

---

## 🎓 Certifications

<a href="https://credentials.databricks.com/28398be2-c157-45b2-82e4-42872de7e178" target="_blank">
  <img src="https://api.accredible.com/v1/frontend/credential_website_embed_image/badge/28398be2-c157-45b2-82e4-42872de7e178" 
       alt="Databricks Certified Data Engineer Associate (2026)" 
       width="120"/>
</a>

| Badge | Certification | Year |
|-------|--------------|------|
| 🏆 | [Databricks Certified Data Engineer Associate](https://credentials.databricks.com/28398be2-c157-45b2-82e4-42872de7e178) | 2026 |
| ☁️ | Salesforce Certified Administrator | 2025 |
| 📊 | Lean Six Sigma Foundations | — |

---

## 📁 Portfolio Projects

### Project 1 — [Supply Chain Event Sourcing System](./project1-supply-chain)
> Real-time shipment tracking pipeline — carrier event feeds into a medallion lakehouse

| Item | Detail |
|------|--------|
| Industry | Ocean Freight / 3PL / NVOCC |
| Source Data | Carrier JSON event feeds simulating CMA CGM, Hapag-Lloyd, MSC, Evergreen, COSCO |
| Pipeline | Auto Loader → Bronze Delta → Silver (MERGE + Quarantine) → CDC → Gold |
| Scale | 466 events, 80 shipments, 5 Delta tables, 35 quarantined records |
| Orchestration | Databricks Jobs — 3 chained tasks, daily schedule, email alerting |
| Runtime | 3 minutes 31 seconds end-to-end |

**Key concepts demonstrated:**
- `cloudFiles` Auto Loader with checkpoint locations and `trigger(availableNow=True)`
- Delta Lake MERGE upsert (`whenMatchedUpdateAll` / `whenNotMatchedInsertAll`)
- CDC via window functions — `row_number().over(partitionBy)` for current shipment state
- Data quality quarantine pattern — 35 corrupt records isolated with labeled defect reasons
- Delta time travel — `versionAsOf` audit queries proving pre/post MERGE state
- Unity Catalog 3-level namespace — `supply_chain_dev.shipments.bronze_shipment_events`
- Databricks Jobs task chaining with automatic retry (3x) and email notifications

**Business output:** Carrier performance Gold table showing on-time %, customs holds, and revenue per carrier — directly applicable to 3PL quarterly business reviews.

---

### Project 2 — [3PL Unified Analytics Lakehouse](./project2-3pl-lakehouse)
> Enterprise multi-source analytics joining SAP ERP + Salesforce CRM + CargoWise TMS

| Item | Detail |
|------|--------|
| Industry | 3PL / Freight Forwarding / NVOCC |
| Sources | SAP ERP (CSV batch), Salesforce CRM (JSON export), CargoWise TMS (JSON API) |
| Pipeline | 5 Auto Loader streams → 5 Bronze tables → 4 Silver tables → 3 Gold tables → SQL Dashboard |
| Scale | 994 records ingested, 12 Delta tables, $2.47M revenue modeled |
| Join | 3-way cross-system join on `customer_id` — Customer 360 view |
| Dashboard | Databricks SQL — KPI counters, customer scorecard, carrier bar chart |

**Key concepts demonstrated:**
- Multi-source Auto Loader ingestion — CSV (SAP) and JSON (Salesforce, TMS) in same pipeline
- Source isolation pattern — separate Volume folders, checkpoints, and streams per system
- 3-way DataFrame LEFT JOIN across SAP + Salesforce + TMS on `customer_id`
- Window function for best contract selection per customer
- Composite customer scoring — 4-dimension weighted score (revenue 40% + service 30% + NPS 20% + contract 10%)
- Carrier performance grading A–D based on on-time delivery percentage
- Databricks SQL dashboard with Genie AI — published organization-wide

**Business output:** Customer 360 revealing Amazon Logistics as simultaneously highest-revenue ($265K) and highest churn-risk — a connection invisible when SAP, Salesforce, and CargoWise operated in silos.

---

## 🛠️ Technical Stack

| Category | Technologies |
|----------|-------------|
| Databricks | DBR 14.x/17.x, Delta Lake, Spark Declarative Pipelines (SDP), Workflows, Lakeflow, Unity Catalog, Databricks Apps, Genie, Asset Bundles (DABs) |
| Big Data | Spark 3.x/4.x, PySpark, Spark SQL, Kafka, Auto Loader |
| Cloud | AWS (S3, Glue, Lambda, EMR), Azure (ADLS Gen2) |
| Databases | Snowflake, Oracle, SQL Server, DynamoDB, SAP (source) |
| Languages | Python 3.x, SQL, Scala (working knowledge) |
| DevOps | Git, Databricks Asset Bundles (DABs), CI/CD pipelines |
| BI / Reporting | Power BI, QlikView, Databricks SQL Dashboards |

---

## 📊 Exam Concepts Covered Across Both Projects

| Category | Concepts |
|----------|---------|
| Lakehouse Platform (LP) | Unity Catalog 3-level namespace, Managed Delta tables, UC Volumes, Delta ACID, Time Travel, DESCRIBE HISTORY |
| ETL | Explicit schema enforcement, MERGE upsert, `to_date` casting, Multi-source JOINs, Window functions, CASE/WHEN, Composite scoring |
| Incremental (INC) | Auto Loader `cloudFiles`, CSV + JSON ingestion, Checkpoint locations, `cloudFiles.schemaLocation`, `trigger(availableNow)`, Source isolation, CDC patterns |
| Production (PROD) | Medallion architecture, Databricks Jobs, Task chaining, Retries, Scheduling, Email alerting, Databricks SQL dashboards, SQL Warehouses |

---

## 💼 Professional Background

| Role | Company | Period |
|------|---------|--------|
| Cloud Data Engineer | eSyber Solutions, Houston TX | Mar 2025 – Present |
| Data Analytics & Data Engineer | CMA CGM (World's 3rd Largest Shipping Line) | Aug 2019 – Feb 2025 |
| Data Analytics / Operations | Hapag-Lloyd (Gulf & Pacific), Houston TX | Jul 2015 – Aug 2019 |
| Operations Manager | CSAV / Norgistics North America | Aug 2011 – Jun 2015 |
| Manager, Operations & Sales | Global American Line | Aug 2005 – Aug 2011 |

Domain expertise: Ocean freight, 3PL/NVOCC operations, freight forwarding, carrier contracts, SAP TM/ERP, Salesforce CRM, CargoWise — enabling data pipelines that reflect real business logic, not just technical patterns.
