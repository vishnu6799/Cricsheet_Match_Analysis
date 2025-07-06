#  Cricsheet Match Data Analysis Project

An end-to-end data analytics pipeline using real-world cricket match data from [Cricsheet](https://cricsheet.org). This project automates scraping, transforms match data into a structured SQL format, performs SQL-based analysis, and visualizes insights using Python and Power BI.

---

##  Project Flow

### 1.  Data Scraping Using Selenium
- Website: [https://cricsheet.org/matches/](https://cricsheet.org/matches/)
- Technologies: Selenium + Python
- Objective: Automate navigation and scrape download links for JSON match data.
- Match Types Extracted:
  - Test Matches
  - One Day Internationals (ODI)
  - T20 Internationals
  - Indian Premier League (IPL)

### 2.  Data Transformation
- Library: pandas
- Process:
  - Parse JSON files
  - Create structured DataFrames for each format
  - Standardize schema across match types
  - Extract and clean relevant fields like player, team, runs, wickets, format, etc.

### 3.  Database Management
- DBMS: SQLite
- Tables Created:
  - test_matches
  - odi_matches
  - t20_matches
  - ipl_matches
- Tools Used: SQLAlchemy + sqlite3
- Task: Insert cleaned DataFrames into respective tables.

### 4. SQL Queries for Data Analysis
- SQL queries were written to extract insights such as:
  - Top 10 run-scorers by format
  - Leading wicket-takers by format
  - Team with highest win percentage in Test matches
  - Count of centuries across all formats
  - Closest wins (smallest victory margins)
- Total queries written: **20**

### 5.  Exploratory Data Analysis (Python)
- Libraries Used: matplotlib, seaborn, plotly
- Created 10+ visualizations:
  - Most runs by players
  - Most wickets by players
  - Format-wise run distributions
  - Team-based performance plots
- Output exported as .pptx (presentation)

### 6.  Power BI Dashboard
- Connected Power BI to the SQLite database.
- Created 3 separate interactive dashboard pages:
  - **Player Stats** – Top scorers, most matches, averages
  - **Format Analysis** – Total/average runs, wickets, match count by format
  - **Team Insights** – Team-based performance comparisons, match count
- Features:
  - Page navigation buttons
  - Dynamic filtering by format
  - Pie charts, bar charts, line charts, stacked visuals

---



