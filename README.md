# Tech Layoffs: SQL Data Cleaning & Exploratory Analysis

Cleaning a global layoffs dataset in MySQL, then exploring trends by company, industry, country and time.

## Tools
MySQL: CTEs, window functions (ROW_NUMBER, DENSE_RANK, SUM OVER), self-joins

## 1. Data Cleaning (`01_data_cleaning.sql`)
- Worked on a staging copy so the raw table stays untouched
- Removed duplicates using ROW_NUMBER() over all columns
- Standardized text: trimmed company names, merged "Crypto" industry variants, fixed "United States." country values
- Converted the date column from text to DATE
- Filled missing industries using matching company rows (self-join)
- Deleted rows with no layoff data and dropped the helper column

## 2. Exploratory Analysis (`02_exploratory_analysis.sql`)
- Total layoffs by company, industry, country, year and funding stage
- Monthly totals with a rolling cumulative total
- Top 5 companies by layoffs for each year using DENSE_RANK()

## Key Findings
- [e.g. Industry with the most layoffs: ___]
- [e.g. Country with the most layoffs: ___]
- [e.g. Peak year/month: ___]
