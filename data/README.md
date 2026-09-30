# Local data setup

The original source for this project is **Online Retail II** from the UCI Machine Learning Repository.

- Source: https://archive.ics.uci.edu/dataset/502/online%2Bretail
- DOI: https://doi.org/10.24432/C5CG6D
- Original file: `online_retail_II.xlsx`
- License: CC BY 4.0

Python was used upstream for data inspection and preparation, with the analytical input exported to Parquet. Power Query then applies the final source-specific preparation required by the validated Power BI report.

The public repository intentionally does **not** include:

- the raw Excel workbook;
- the prepared `fact_sales.parquet` file;
- the upstream preprocessing notebook;
- Power BI Desktop cache or local runtime files.

The repository focuses on the validated Power BI implementation.

## Refreshing locally

To refresh the semantic model, provide a compatible `fact_sales.parquet` file matching the schema expected by:

`Retail.SemanticModel/definition/tables/fact_sales.tmdl`

Then update the placeholder source path in that file.

The public copy intentionally uses:

`C:\REPLACE_WITH_YOUR_LOCAL_PATH\fact_sales.parquet`

This keeps machine-specific usernames and folders out of source control while preserving the report pages, semantic model, DAX measures, relationships, navigation and formatting used in the validated portfolio version.
