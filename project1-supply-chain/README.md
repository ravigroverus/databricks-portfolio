# Project 1 — Supply Chain Event Sourcing System

## Overview
Real-time shipment tracking pipeline ingesting carrier JSON event feeds into a medallion lakehouse on Databricks.

## Notebooks — Run in Order
| Step | Notebook | Purpose |
|---|---|---|
| 1 | SC_Step1_Setup.ipynb | Environment setup + synthetic carrier data generation |
| 2 | SC_Step2_Bronze.ipynb | Auto Loader ingestion into Bronze Delta table |
| 3 | SC_Step3_Silver.ipynb | Cleanse, quarantine bad records, MERGE upsert |
| 4 | SC_Step5_Gold.ipynb | Gold aggregations + Delta time travel audit |

## Architecture
