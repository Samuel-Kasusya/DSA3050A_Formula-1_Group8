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
| Ogutu Rufinus | 670827 |

## Dataset Source URL
https://www.kaggle.com/datasets/rohanrao/formula-1-world-championship-1950-2020

## Dataset Description
Formula 1 race data from the Ergast database (via Kaggle), covering every season from 1950 to 2024. The dataset is made up of 14 related tables — races, drivers, constructors, circuits, seasons, status, lap times, pit stops, qualifying, results, sprint results, and driver and constructor standings — linked by shared ID columns. The largest table (lap times) records one row per driver per lap, at 589,081 rows. Because the data captures every lap rather than only final results, it can show how consistent drivers and teams are, and how grid position, pit stops, circuit and season affect results.

## Business Problem
Formula 1 teams work under a strict budget cap, so management has to back big decisions, which drivers to run, how to plan race strategy, and where to spend limited development money with evidence. Our group acts as a business intelligence team hired by the management of an F1 team, our client. They hold decades of race data but have no single view that turns it into decisions.
Our goal is one clear dashboard that shows who performs well and how consistently, and how grid position, pit stops, circuits and seasons shape results so management can make better driver, strategy and investment calls.

**Key business questions**
1. Which drivers and constructors have the most race wins, and how has that trend changed by season?
2. Which circuits show the biggest gap in points scored between top and mid-field constructors?
3. Which drivers have made the most pit stops across their careers?
4. Where geographically has the sport generated the most points, by country?
5. How have the leading drivers' and constructors' standings changed across seasons?

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
- Identified and separated fact tables from the dimension tables.
- Created and verified relationships between the fact and dimension tables.
- Added and connected the **DimDate** table to **FactResults** using the **Race Date** field.
- Configured One-to-Many (1:*) relationships with single-direction filtering.
- Reviewed and refined the model to align with dimensional modelling best practices.
- Updated the Power BI project file (`PowerBI/GroupProject.pbix`) with the completed data model.
- Added screenshots documenting the data modelling process in the `Screenshots` folder.

## DAX Measures Created
The following DAX measures were created to support analysis and improve decision-making in the dashboard:
- Created basic aggregation measures such as Total Races, Total Wins, Total Drivers, and Total Points.
- Developed ratio and percentage measures including Win Rate, Podium Rate, and Average Points per Race.
- Implemented time intelligence measures such as Points YTD, Previous Year Points, and Points Growth %.
- Created ranking measures including Driver Rank by Wins and Constructor Rank by Points.
- Built KPI and conditional measures such as Driver Performance Status and Win Category.
- Developed dynamic measures like Selected Driver Title and Selected Season Title for interactive reporting.
- Used DAX functions including CALCULATE, DIVIDE, RANKX, TOTALYTD, and SELECTEDVALUE.
- Organised all measures into a dedicated _Measures table for better structure and maintainability.
- Applied appropriate formatting (percentages, whole numbers) to ensure clarity and professionalism.

## Dashboard Pages Explained
The dashboard is made up of four pages, with a page navigator and a synced Year slicer available across all of them.

**Executive Summary** — a high-level view for management. Five KPI cards show Total Races, Total Drivers, Total Constructors, Total Wins and Total Points. A bar chart ranks the top 10 constructors by all-time wins, a line chart shows the win trend by year, and a treemap shows how wins are distributed across drivers.

**Trend Analysis** — season-by-season performance. A line chart tracks points over time for the top 5 constructors, and a second line chart tracks wins over time for the top 5 drivers, showing how leading teams and drivers have risen and fallen across seasons.

**Geographic Analysis** — where racing happens and how competitive it is. A map plots circuits by location with bubble size showing points scored, a bar chart ranks countries by total points, and a matrix with conditional formatting compares points scored by top constructors at each circuit.

**Detailed Drill-through** — driver-level detail. Reached by right-clicking a driver on another page, this page filters to that driver and shows a performance table (wins, points, races, nationality, performance status) alongside a chart of total pit stops by driver.

## Key Insights


## Recommendations


## Contribution Summary for Each Member
| Member | Contributions |
|--------|--------------|
| Samuel Kasusya | Set up the GitHub repository and folder structure, wrote Part 1 (business problem, dataset description, key business questions), and uploaded the raw dataset. Delegated and reviewed work across the group, coordinating handovers between stages. Built the initial Power BI dashboard (Part 5) — all four pages with required visuals, drill-through, synced slicers and navigation — then handed it over for theming, tooltip page and final polish. |
| Kendi Nyaga | Imported and cleaned the Formula 1 datasets in Power BI, standardized column names, corrected data types, replaced `\N` values with nulls, removed unnecessary columns, performed column profiling, applied Merge Queries, created Reference Queries, performed Group By transformations with multiple aggregations, created summarized tables and a Date Table, and prepared the dataset for data modeling. |
| Lisa Mbaire | Designed and structured the Power BI data model using fact and dimension tables, created and validated table relationships, developed DAX measures for KPIs and analysis, implemented time intelligence calculations, built interactive dashboard visuals, and documented the data model and measures in the README. | 
| Adrian Munyua | |
| Michael Sifuna | Renamed fact and dimension tables using standard naming conventions, organized the Power BI model for improved readability, created and validated relationships between tables, connected the Date dimension (`DimDate`) to `FactResults` for time-based analysis, verified relationship cardinality and filter directions, documented the final data model with supporting screenshots, and prepared the dataset for DAX. |
| Ogutu Rufinas | |
