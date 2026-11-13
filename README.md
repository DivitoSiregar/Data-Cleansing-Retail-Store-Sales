# Data Cleansing – Retail Store Sales Using Microsoft Excel

## Project Overview

This project focuses on cleaning and improving the quality of a retail store sales dataset using Microsoft Excel. The dataset contains several data quality issues, particularly missing values and inconsistent text formatting caused by extra spaces.

The main objective of this project is to identify data quality problems, apply appropriate cleaning techniques, and produce a cleaner and more structured dataset that is ready for further analysis.

This project also serves as a practical exercise to develop data cleaning and data preparation skills using Microsoft Excel.

## Dataset Information

- **Dataset Name:** Dirty Retail Store Sales Dataset
- **Source:** Kaggle
- **Initial Rows:** 12,575
- **Columns:** 11
- **Product Categories:** 8
- **Unique Items:** 200
- **Data Type:** Synthetic Data

The dataset represents retail store transactions and contains the following columns:

| Column | Description |
|---|---|
| Transaction ID | Unique transaction identifier |
| Customer ID | Customer identifier |
| Category | Product category |
| Item | Product name |
| Price Per Unit | Unit price |
| Quantity | Number of items purchased |
| Total Spent | Total transaction amount |
| Payment Method | Payment method |
| Location | Transaction location |
| Transaction Date | Transaction date |
| Discount Applied | Indicates whether a discount was applied |

## Project Objectives

1. Identify data quality issues in the original dataset.
2. Clean inconsistent text formatting.
3. Examine unique values and their frequencies.
4. Investigate relationships between product categories, item names, and unit prices.
5. Handle missing values in the Item column using reference-based imputation.
6. Produce a cleaned dataset for further exploratory data analysis (EDA).

## Tools & Functions

**Tool:**
- Microsoft Excel

**Excel Functions Used:**

| Function | Purpose |
|---|---|
| TRIM | Remove unnecessary spaces |
| UNIQUE | Extract unique values |
| COUNTA | Count non-empty cells |
| COUNTIF | Count cells based on a criterion |
| SUM | Calculate total values |
| VLOOKUP | Retrieve reference data |
| TRANSPOSE | Change data orientation |
| SORT | Sort data |
| FILTER | Filter data based on conditions |
| INDEX | Retrieve values based on position |
| MATCH | Find the position of a value |
| IF | Apply logical conditions |
| IFERROR | Handle formula errors |
| AND | Evaluate multiple conditions |
| OR | Evaluate alternative conditions |

## Data Cleaning Process

The project consists of several cleaning stages:

### 1. Data Inspection

Examined the dataset structure, column names, data types, unique values, missing values, and potential duplicate records.

### 2. Text Cleaning

Applied the TRIM function to remove leading spaces, trailing spaces, and unnecessary repeated spaces from text columns.

This step helps ensure consistent text formatting and prevents mismatches during data lookup and categorization.

### 3. Column Identification

Identified unique values and their frequencies in several columns:

- Transaction ID
- Customer ID
- Category
- Item
- Payment Method
- Location

This process helped understand the dataset characteristics and identify missing values, particularly in the Item column.

### 4. Category and Item Relationship Analysis

Created a reference table to identify which items belong to each product category.

The process involved filtering items by category, removing duplicates, and sorting the results alphabetically.

The frequency of each item was also calculated to identify missing Item values within each category.

### 5. Item and Price Per Unit Validation

Examined the relationship between Item and Price Per Unit to ensure that each product name corresponds to a consistent unit price.

### 6. Missing Value Imputation

The Item column was identified as the main column containing missing values.

To recover missing item names, a reference table was created using three attributes:

- Category
- Item
- Price Per Unit

The Price Per Unit column was recalculated using the relationship:

**Total Spent = Price Per Unit × Quantity**

Therefore:

**Price Per Unit = Total Spent / Quantity**

The combination of Category and Price Per Unit was then used as the matching key to identify missing Item values.

Excel functions such as INDEX, MATCH, TRIM, IF, OR, and IFERROR were used in this process.

### 7. Removing Unidentified Records

After the imputation process, 604 rows still contained blank values in the Item column.

These records were removed because their product identities could not be determined using the available reference information.

The removed records represented approximately 4.8% of the original dataset.

### 8. Final Dataset

After completing the cleaning process, the resulting dataset contained 11,971 rows.

## Project Results

| Description | Number of Rows |
|---|---:|
| Initial Dataset | 12,575 |
| Rows Removed | 604 |
| Final Cleaned Dataset | 11,971 |

<sub>Approximately 95.2% of the original records were retained.</sub>

The final dataset is more structured and has undergone the cleaning and missing-value handling procedures described in this project.

## Repository Structure

```text
Retail-Store-Sales-Data-Cleansing/
│
├── README.md
│
├── Data/
│   └── cleaned_retail_store_sales.xlsx
│
├── Documentation/
   └── Data Cleansing Retail Store Sales - Tumpal Divito Siregar.pdf
```

## Key Learnings

Through this project, I gained practical experience in:

- Understanding data quality issues.
- Performing data inspection and validation.
- Cleaning inconsistent text data using Excel.
- Working with lookup and reference tables.
- Applying logical conditions and lookup functions.
- Handling missing values through reference-based imputation.
- Making data cleaning decisions based on relationships between variables.

## Author

**Tumpal Divito Siregar**

Mathematics Student | Aspiring Data Analyst

This project is part of my learning journey in Data Analytics.

## Acknowledgement

Dataset source: Kaggle – Dirty Retail Store Sales Dataset.

