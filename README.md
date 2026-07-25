# DSA3050A – Formula 1 Performance Intelligence Dashboard

## Group Name
Group 8

## Member Names and Student IDs
| Name | Student ID |
|------|-----------|
| Samuel Kasusya | 668694 |
| Kendi Nyaga | 671807 |
| Lisa Mbaire | 672034 |
| Adrian Munyua | 672056 |
| Michael Sifuna | 673982 |
| Ogutu Rufinas | 670827 |

## Dataset Source URL
https://www.kaggle.com/datasets/rohanrao/formula-1-world-championship-1950-2020

## Dataset Description
Formula 1 race data from the Ergast database (via Kaggle), covering every season from 1950 to 2024. The full set is 14 related tables; this project uses 10 of them — races, drivers, constructors, circuits, lap times, pit stops, results, status, driver standings and constructor standings — linked by shared ID columns. The largest table (lap times) records one row per driver per lap, at 589,081 rows. Because the data captures every lap rather than only final results, it can show how consistent drivers and teams are, and how grid position, pit stops, circuit and season affect results. 

## Business Problem
Formula 1 teams work under a strict budget cap, so management has to back big decisions, which drivers to run, how to plan race strategy, and where to spend limited development money with evidence. Our group acts as a business intelligence team hired by the management of an F1 team, our client. They hold decades of race data but have no single view that turns it into decisions.
Our goal is one clear dashboard that shows who performs well and how consistently, and how grid position, pit stops, circuits and seasons shape results so management can make better driver, strategy and investment calls.

**Key business questions**
1. Which drivers and teams are the most consistent across a season, and which are the most erratic?
2. Does a better starting position reliably lead to a better finish, and does that change from circuit to circuit?
3. How do pit stops (how many, how long) affect a driver's final result?
4. Which circuits show the biggest gap between top and mid-field teams?
5. How have the leading drivers' and teams' standings changed over the seasons?

## Power Query Transformations

The Formula 1 dataset was cleaned and transformed in Power Query before modeling. The following transformations were applied:

- Imported all selected CSV tables into Power BI.
- Renamed columns using a consistent naming convention.
- Corrected data types (Whole Number, Decimal Number, Text and Date).
- Replaced all "\N" values with null values.
- Removed unnecessary and redundant columns.
- Applied Column Quality, Column Distribution and Column Profile to assess data quality.
- Performed Merge Queries to enrich the main fact table with related descriptive information.
- Created Reference Queries for analytical purposes.
- Applied Group By transformations with multiple aggregations.
- Created summarized tables to support reporting and analysis.
- Created a Date Table to facilitate time-based analysis.

## Data Model Explanation

The Power BI data model was designed and refined to improve data organization and support efficient analysis of the Formula 1 dataset.

- Renamed tables using standard **Fact** and **Dimension** naming conventions.
- Organized the Power BI model to improve readability and maintainability.
- Identified and separated fact tables from dimension tables.
- Created and verified relationships between fact and dimension tables.
- Added and connected the **DimDate** table to **FactResults** using the **Race Date** field.
- Configured One-to-Many (1:*) relationships with single-direction filtering.
- Reviewed and refined the model to align with dimensional modelling best practices.
- Updated the Power BI project file (`PowerBI/GroupProject.pbix`) with the completed data model.
- Added screenshots documenting the data modelling process in the `Screenshots` folder.

## DAX Measures Created


## Dashboard Pages Explained


## Key Insights


## Recommendations


## Contribution Summary for Each Member
| Member | Contributions |
|--------|--------------|
| Samuel Kasusya | |
| Kendi Nyaga | Imported and cleaned the Formula 1 datasets in Power BI, standardized column names, corrected data types, replaced `\N` values with nulls, removed unnecessary columns, performed column profiling, applied Merge Queries, created Reference Queries, performed Group By transformations with multiple aggregations, created summarized tables and a Date Table, and prepared the dataset for data modeling. |
| Lisa Mbaire | |
| Adrian Munyua | |
| Michael Sifuna | Renamed fact and dimension tables using standard naming conventions, organized the Power BI model for improved readability, created and validated relationships between tables, connected the Date dimension (`DimDate`) to `FactResults` for time-based analysis, verified relationship cardinality and filter directions, documented the final data model with supporting screenshots, and prepared the dataset for DAX. |
| Ogutu Rufinas | |
