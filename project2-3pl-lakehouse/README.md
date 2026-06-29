# Project 2 — 3PL Unified Analytics Lakehouse

## Overview
Enterprise multi-source analytics platform joining SAP ERP + Salesforce CRM + CargoWise TMS into a unified Delta Lake lakehouse on Databricks.

## Notebooks — Run in Order
| Step | Notebook | Purpose |
|---|---|---|
| 1 | LP_Step1_Setup.ipynb | Environment setup + synthetic data generation |
| 2 | LP_Step2_Bronze.ipynb | Auto Loader ingestion — 5 streams (CSV + JSON) |
| 3 | LP_Step3_Silver.ipynb | Clean, cast, join — Customer 360 unified view |
| 4 | LP_Step4_Gold.ipynb | Executive KPIs + Customer Scorecard + Carrier Performance |

## Architecture
