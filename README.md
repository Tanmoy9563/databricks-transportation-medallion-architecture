🚍 Databricks Medallion Architecture – Transportation Domain

A production-grade Data Engineering project built using Databricks Delta Live Tables (DLT) demonstrating a full Medallion Architecture (Bronze → Silver → Gold) for a Transportation use case.

This repository is resume-ready and mirrors how modern data platforms are designed in real enterprise environments.

📌 Project Overview

This project processes batch and streaming transportation data on Databricks + AWS S3, applying:

Delta Lake best practices

Auto Loader for streaming ingestion

Data quality expectations

CDC upserts (SCD Type 1)

Calendar & City dimensions

Secure, analytics-ready Gold views

Final outputs are city-level analytical views consumable by City Managers with RBAC.

🧱 Medallion Architecture Layers
🥉 Bronze Layer – Raw Ingestion

Purpose: Capture raw data exactly as received.

Sources:

Batch CSV → City master data

Streaming CSV → Trips data (Auto Loader)

Key Features:

Schema inference & evolution

Metadata capture (file path, ingest time)

Change Data Feed enabled

🥈 Silver Layer – Clean & Standardized

Purpose: Business-ready, validated data.

Key Features:

Data quality checks (@dp.expect)

Type casting & standardization

CDC upserts (SCD Type 1)

Enrichment with City & Calendar dimensions

🥇 Gold Layer – Business Analytics

Purpose: Serve analytics & BI use cases.

Outputs:

Fact table with city, calendar & trip metrics

Materialized SQL views

Optimized for reporting & dashboards
