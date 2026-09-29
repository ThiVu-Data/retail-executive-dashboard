# Local data setup

The original source for this project is the **Online Retail II Excel workbook**.

Python was used upstream to prepare the analytical input and export it to Parquet. Power Query then applies the final source-specific preparation required by the Power BI model.

The public repository does not include the raw Excel workbook, the local Parquet data file, or Power BI Desktop cache files.

Before refreshing the semantic model:

1. Place your local `fact_sales.parquet` file on your machine.
2. Update the file path used by the `fact_sales` query in:

   `Retail.SemanticModel/definition/tables/fact_sales.tmdl`

The public copy intentionally uses this placeholder:

`C:\REPLACE_WITH_YOUR_LOCAL_PATH\fact_sales.parquet`

This keeps machine-specific usernames and local folders out of source control. The validated report pages, semantic model, DAX measures, relationships, navigation and formatting are otherwise unchanged.
