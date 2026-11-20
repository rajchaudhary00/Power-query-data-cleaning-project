# Power Query Data Cleaning & Restructuring

## Project Overview

This project focuses on cleaning and restructuring raw Excel data using Microsoft Excel Power Query.

The original dataset had records split across alternating rows, making it difficult to work with in its existing format. I used Power Query to separate, match, and combine these rows into a single structured dataset.

## Data Transformation Process

The following steps were performed in Power Query:

1. Imported the corrected raw Excel source file.
2. Promoted the first row as column headers.
3. Applied appropriate data types.
4. Removed unnecessary top rows.
5. Added an Index column to identify row positions.
6. Used Integer Division and Modulo to separate alternating rows.
7. Created two separate queries: `top` and `bottom`.
8. Merged both queries using a common pair key with an Inner Join.
9. Expanded the merged columns to reconstruct complete records.
10. Removed unnecessary helper and duplicate columns.
11. Renamed columns and organized the final structure.
12. Replaced missing values in selected text columns with `N/A`.
13. Applied the appropriate data type to the Shipped date column.

## Final Dataset

| Description | Result |
|---|---:|
| Total Records | 100 |
| Total Columns | 13 |
| Duplicate Order Numbers | 0 |
| Duplicate Job Numbers | 0 |

The final dataset is structured and ready for further analysis.

## Files Included

| File | Description |
|---|---|
| `Raw_Source_Data.xlsx` | Corrected raw source data |
| `Cleaned_Data.xlsx` | Final cleaned dataset with Power Query transformations |

## Tools & Techniques

- Microsoft Excel
- Power Query Editor
- Power Query M Language
- Index Column
- Integer Division & Modulo
- Merge Queries (Inner Join)
- Expand Columns
- Remove & Rename Columns
- Replace Values
- Data Type Transformation
- Query Parameters

## Refresh Instructions

The workbook uses a Power Query parameter named `pFilePath` to connect to the source file.

To refresh the queries on another computer:

1. Keep both Excel files accessible.
2. Open `Cleaned_Data.xlsx`.
3. Go to Data → Get Data → Launch Power Query Editor.
4. Open Manage Parameters and select `pFilePath`.
5. Update its Current Value with the local path of `Raw_Source_Data.xlsx`.
6. Select Close & Load, then use Refresh All.

## Project Outcome

The raw data was successfully restructured into 100 organized records with 13 columns using Power Query.

This project demonstrates practical experience in handling inconsistent data structures, combining related records, managing missing values, and preparing data for further analysis.
