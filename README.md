# IPL Cricket Analytics Pipeline (2008–2024)

## Overview
This project showcases an end-to-end cricket analytics workflow built using publicly available match data from ESPN Cricinfo.

The pipeline collects match-level scorecard and commentary data, transforms nested JSON into a structured ball-by-ball dataset, and generates analytical outputs for cricket performance analysis and dashboarding.

It was built to solve a real problem I faced in my earlier cricket analytics work: manually maintaining and updating ball-by-ball data was time-consuming and difficult to scale. This version rebuilds that workflow in a more automated and analysis-ready way.

## Project Evolution
This project builds on an earlier version of my cricket analytics work.

### Phase 1: Manual workflow
Before my degree began, I built my own IPL ball-by-ball master dataset manually using CSV files from Cricsheet. I compiled season data into a central spreadsheet, updated it match by match, and used it for Tableau dashboards published to a website.

That process gave me strong familiarity with:
- cricket data structures
- match-level and ball-by-ball logic
- manual cleaning and consolidation
- dashboarding and cricket insight generation

### Phase 2: Automated pipeline
In 2025, I rebuilt the workflow using Python as part of a university project. The goal was to remove the limitations of manual updates and automate the full pipeline from raw data collection to analysis-ready output.

This version uses Python-based scraping, JSON transformation, and analytical scripting to generate a large structured dataset for deeper analysis.

## Problem Statement
ESPN Cricinfo is one of the richest public sources of cricket data, but it does not provide a simple open API for structured large-scale extraction. Its pages are dynamic, commentary loads progressively, and the underlying data is embedded in nested response structures.

The objective of this project was to create a scalable workflow for analyzing IPL ball-by-ball data from 2008 to 2024. The approach was to scrape match-level scorecard and commentary data, store it as JSON, and transform it into a single structured dataset suitable for analysis and visualization. This project analyzed IPL ball-by-ball data from 2008 to 2024 and used a match-by-match scraping approach to extract commentary and scorecard data.  [oai_citation:0‡Social Web Analytics PPT.pptx](sediment://file_0000000014f071fa958143bf5dd6dbbf)

## Tech Stack
- Python
- Playwright
- Pandas
- ujson
- Plotly
- Matplotlib
- Excel
- Tableau

The project used Playwright for dynamic scraping, Python for core logic, Pandas for transformation, ujson for fast JSON parsing, Plotly and Matplotlib for visualizations, and Excel to store and loop through 1000+ match IDs.  [oai_citation:1‡Social Web Analytics PPT.pptx](sediment://file_0000000014f071fa958143bf5dd6dbbf)

## Pipeline Workflow
1. Match IDs for IPL games from 2008 to 2024 are stored in Excel.
2. A Playwright scraper collects scorecard and commentary data for one match at a time.
3. Each match is saved as a structured JSON file.
4. A transformation script converts all JSON files into a single master DataFrame.
5. The final dataset is used for analysis and dashboarding.

This workflow matches the project design described in the project presentation: match IDs were stored in Excel, each match was scraped into structured JSON, and all JSON files were transformed into a single master DataFrame for analysis.  [oai_citation:2‡Social Web Analytics PPT.pptx](sediment://file_0000000014f071fa958143bf5dd6dbbf)

## Dataset Summary
- Matches processed: 1000+
- Total deliveries analyzed: ~3 million
- Unique players: 800+
- Venues covered: 40+
- Features per delivery: 60+

The project presentation reports 1000+ matches processed, around 3 million deliveries, 800+ unique players, 40+ venues, and 60+ features in the final DataFrame.  [oai_citation:3‡Social Web Analytics PPT.pptx](sediment://file_0000000014f071fa958143bf5dd6dbbf)

## Example Analysis Areas
This dataset supports analysis such as:
- top run scorers across seasons
- run rate trends over time
- bowling type distribution by over
- team scoring patterns by season
- wagon wheel analysis for individual batters

The presentation highlights analyses including top 20 run scorers, season-wise run rate, bowling type distribution by over, over-wise run rate by team and season, and wagon wheel analysis for Virat Kohli in 2024.  [oai_citation:4‡Social Web Analytics PPT.pptx](sediment://file_0000000014f071fa958143bf5dd6dbbf)

## Repository Structure
```text
scraping/     -> scripts for collecting match data
processing/   -> JSON to DataFrame / CSV transformation
analysis/     -> Python-based analysis scripts
data/
  raw/        -> sample raw files and match input files
  processed/  -> processed dataset or sample dataset
tableau/      -> dashboard screenshots and assets
