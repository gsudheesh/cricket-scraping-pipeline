# Cricket Analytics Pipeline: ESPN Cricinfo to Dashboard Insights

## Overview
This project showcases an end-to-end cricket analytics workflow built for data analysis and dashboarding. Match data was sourced from ESPN Cricinfo, transformed from nested JSON into a structured ball-by-ball dataset, and used to generate analytical outputs and dashboard-ready insights.

The goal of this project was to build a reusable pipeline that could take raw match-level data and convert it into a format suitable for exploratory analysis, trend discovery, and visual storytelling.

## Project Objective
Cricket data on public websites is often available in raw or semi-structured formats, which makes direct analysis difficult. This project was built to solve that problem by:

- collecting scorecard and commentary-level match data
- converting nested raw outputs into tabular ball-by-ball data
- preparing a clean dataset for analysis and dashboard creation
- generating insights on batting, scoring patterns, and match trends

## Tools and Technologies
- **Python**
- **Playwright**
- **Pandas**
- **JSON / CSV data processing**
- **Matplotlib / Plotly**
- **Tableau**

## Pipeline Workflow
1. **Data collection**  
   Match scorecard and commentary data are scraped from ESPN Cricinfo.

2. **Raw storage**  
   Each match is stored as a JSON file.

3. **Data transformation**  
   Raw nested JSON is flattened into a structured ball-by-ball dataset.

4. **Analysis**  
   Python scripts are used to explore trends and generate supporting outputs.

5. **Dashboarding**  
   The processed dataset is used for visual analysis and dashboard creation in Tableau.

## Repository Structure
```text
scraping/     -> scripts for collecting ESPN Cricinfo match data
processing/   -> JSON to DataFrame / CSV transformation logic
analysis/     -> Python-based analysis and chart generation
data/
  raw/        -> sample raw JSON and match input files
  processed/  -> processed dataset for analysis and dashboards
tableau/      -> dashboard assets and screenshots
