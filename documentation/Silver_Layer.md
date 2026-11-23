# Silver Layer — Cleaning and Data Quality

## Objective
Create a cleaned normal-sales dataset for analytics while documenting decisions about ambiguous or potentially meaningful records.

## Classification and reconciliation
- C-prefixed invoice records were classified separately.
- Normal positive-quantity sales were isolated.
- Negative quantity non-C records were investigated separately.
- Bad-debt adjustments were identified by StockCode `B` and Description `Adjust bad debt` (six records in the investigation).

The classification counts reconciled to the Bronze source during the project investigation.

## Cleaning and investigations
- Exact duplicates were removed from the normal-sales dataset.
- Reliable StockCode-to-description mappings were used to recover missing descriptions; unresolved values were retained.
- Missing Customer_ID values were retained. They were not fabricated.
- Zero-price records were investigated and retained.
- Large-quantity records were investigated using an IQR-based approach and retained where no defensible removal rule was established.
- Leading/trailing whitespace was trimmed from StockCode and Description.
- Quantity and Price business rules were validated for the normal-sales dataset.

## Persisted table
`workspace.ecommerce.silver_retail`

The persisted Silver table was verified at 1,010,533 rows and 8 columns in the project session. It does not include the Gold-derived `TotalAmount` column.

## Notebook
`notebooks/02_Silver_Retail_Cleaning.ipynb`
