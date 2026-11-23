# Bronze Layer — Ingestion and Source Exploration

## Purpose
Ingest the raw Online Retail II CSV into Delta and inspect the source without prematurely applying business cleaning.

## Implemented
- CSV ingestion from a Databricks Volume.
- Schema and sample exploration.
- Null profiling.
- Duplicate investigation.
- Negative-quantity investigation.
- Rename `Customer ID` to `Customer_ID`.
- Persist to `workspace.ecommerce.bronze_retail`.

## Source observations
The original source had 1,067,371 rows. Initial profiling identified missing Description and Customer ID values, duplicate records, and negative quantities requiring investigation in downstream processing.

## Notebook
`notebooks/01_Bronze_Source_Exploration.ipynb`

## Environment note
The notebook references `/Volumes/workspace/ecommerce/raw_data/online_retail_II.csv`. Adapt the path to your workspace and Volume setup.
