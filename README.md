
Near-Earth Object (NEO) Data Pipeline — Databricks + Medallion Architecture
---------------------------------------------------------------------------

Overview
--------

This repository contains a modular, Databricks notebook solution for ingesting, transforming, and analyzing NASA's Near-Earth Object (NEO) data.
The pipeline is built using the Medallion architecture (Bronze → Silver → Gold).

🔧 Architecture Highlights
---------------------------

| Layer        | Purpose | 
|--------------|---------|
| Bronze       | Raw ingestion from NASA's NEO API |
| Silver       | Cleaned, normalized data with orbital calculations and error handling |
| Gold         | Aggregated insights, visualizations, and dashboard-ready datasets     |


Files:
------

1. neo_ingest_brz.ipynb      — Parameterized ingestion from NASA API with logging
2. neo_transform_slv.ipynb   — Cleansing, orbital period calculations, and schema validation
3. neo_aggr_gld.ipynb        — threat level, size, and proximity
4. neo_visualization.ipynb   — Verify Acceptance criteria (SQL, visualization)


Tables:
-------

1. Bronze layer:
   | Table        | Purpose        |
   |--------------|----------------|
   | neos         | store neo data |
   | approaches   |store close approaches data|

2. Silver layer:

   | Table          | Purpose        |
   |----------------|----------------|
   | neo_approaches | store cleaned, enriched data |

4. Gold layer:

   | Table          | Purpose        |
   |----------------|----------------|
   | neo_analysis   | store dashboard and visualization ready data |


*  Log table:

   | Table          | Purpose        |
   |----------------|----------------|
   | neo_logs       | Store 'timestamp' level' and 'message text' |






