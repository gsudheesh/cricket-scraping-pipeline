
---

# What to put in the folder READMEs

## `scraping/README.md`

```md
# Scraping

This folder contains the Python scripts used to collect cricket match data from ESPN Cricinfo.

## Files
- `espn_scraper.py`  
  Scrapes scorecard and commentary data for a single match.

- `espn_scraper_loop.py`  
  Reads match IDs from an Excel file and runs the scraper across multiple matches.

## Output
Each scraped match is saved as a JSON file in the raw data folder.
