
# 📘 PROJECT LOG — Formula 1 Performance Analytics  
**Author:** Ammar Haider  
**Goal:** Build an end-to-end data analytics project based on real Formula 1 data, demonstrating skills in data engineering, SQL, visualization, telemetry, strategy analysis, and performance insights similar to the work of a real F1 data/performance engineer.

---

## 🗓️ Log Start Date: November 2025

---

## 1. Initial Project Setup  
**Completed**
- Defined full project vision  
- Decided project will include:  
  - Data acquisition (FastF1 + SQL + CSV)  
  - Data cleaning  
  - Exploratory Data Analysis  
  - SQL database  
  - Python visualizations  
  - Power BI dashboard  
  - Final insights for stakeholders  
- Created initial GitHub repo structure  
- Added README  
- Added Power BI layout brief  
- Added sample notebooks (`01_data_import_and_cleaning`, `02_exploratory_analysis`)  
- Confirmed project direction:  
  > Build a real F1 analytics system to help stakeholders decide which driver to “buy” using real performance data.

---

## 2. SQL + Python Prototype  
**Completed**
- Built SQLite DB from sample data  
- Wrote SQL helper function (`q()`)  
- Verified SQL execution inside Google Colab  
- Conducted first EDA using SQL and Python  
- Added charts for wins, points, grid vs finish, pit stops  
- Confirmed notebooks render correctly on GitHub  

---

## 3. Transition to Real Data (FastF1)  
**Completed**
- Decision made to use **FastF1** as the primary real-time data source  
- Project expanded to include telemetry, lap-by-lap pace, tyre strategy, stints, weather and more  
- Decided to start with **one race first**, then scale to the entire season  

### Installing FastF1 (Documented for Reproducibility)

To install FastF1 inside Google Colab or local Python environment:

```python
!pip install fastf1 fastf1[plotting]
```

Enable caching so FastF1 reuses downloaded data:

```python
import fastf1
import os

CACHE_PATH = "/content/fastf1_cache"
os.makedirs(CACHE_PATH, exist_ok=True)
fastf1.Cache.enable_cache(CACHE_PATH)
```

This ensures:
- Faster data loading  
- Reliability  
- Reproducible sessions  

---

## 4. Next Steps (Planned)
- Create notebook: `03_fastf1_real_data_analysis.ipynb`
- Load the first race session using FastF1  
- Extract structured tables:
  - laps  
  - telemetry  
  - stints  
  - pitstops  
  - weather  
  - session results  
  - driver metadata  
- Build race pace analysis  
- Build tyre degradation curves  
- Build telemetry comparison  
- Export datasets into CSV + SQLite format  
- Develop Power BI race dashboard  
- Begin creating the **Driver Purchase Recommendation Model**

---

## 5. Vision for Full Season  
Once the single-race pipeline is validated:
- Process all 23 races of 2023  
- Build season-level dataset  
- Generate driver performance scorecard  
- Build dashboard filters by:
  - Driver  
  - Constructor  
  - Circuit  
  - Session type  
  - Tyre compound  
  - Stint  
- Produce final Executive Summary report  
- Identify top drivers based on:
  - Race pace  
  - Qualifying performance  
  - Tyre management  
  - Consistency index  
  - Telemetry-based racecraft metrics  

---

### 6. Silverstone 2023 — First Real Race Analysis (VER vs HAM)
- Installed and configured FastF1 with cache
- Loaded full race session for Silverstone 2023 (British GP)
- Built structured laps and pit-stop tables
- Created first race pace comparison chart (lap time vs lap number for VER vs HAM)
- Built first telemetry comparison (speed vs distance for fastest lap)
- Created initial driver performance summary metrics (avg, median, std lap time)
- Exported CSVs for SQL / Power BI use

- ---

## 7. Silverstone 2023 — Tyre & Stint Analysis (VER vs HAM)  
**Completed**

- Focused analysis on the **2023 British Grand Prix (Silverstone) – Race session**.  
- Filtered clean race laps for **VER** and **HAM**, excluding out-laps, in-laps, and invalid lap times.  
- Built a **tyre-compound-level pace table**:
  - Average, median, and standard deviation of lap times by driver and compound.
  - Lap counts per compound to understand sample size and stint length.  
- Created a **tyre compound pace comparison chart**:
  - Bar chart of average lap time by compound (Soft/Medium/Hard) for VER vs HAM.
  - Designed to show how compound choice impacts race pace for each driver.  
- Built **stint-level boxplots**:
  - Boxplots of lap-time distributions per stint, split by driver.
  - Highlights consistency, variability, and potential degradation patterns within each stint.  
- Exported analysis tables (compound pace, stint-level laps) as CSVs for future:
  - SQL database integration.
  - Power BI visualizations.
- These analyses move the project closer to a **driver performance scouting** use case by quantifying:
  - How each driver performs on different compounds.
  - How stable and competitive their stint pace is across the race.

23rd November 2025

1. README File Fully Refined

Added a polished Silverstone analysis section.

Standardized formatting, fixed structural issues, and improved clarity.

Updated wording for professionalism and precision.

Created a refined downloadable README (README_refined.md).

Added internal documentation links (ABOUT, CONTRIBUTING, LICENSE, LOG).

Outcome:
README is now portfolio-ready, clear, professional, and informative.

2. Created ABOUT.md (Detailed Project Overview)

Added a full breakdown of project purpose, workflow, and vision.

Documented all tools, pipelines, and analytical workflows.

Added future roadmap and author details.

Outcome:
Enhanced depth and professionalism for recruiters reviewing the project.

3. Added CONTRIBUTING.md

Included environment setup, coding style, branching guidelines, and PR instructions.

Added contribution philosophy tailored to F1 analytics.

Outcome:
Repository now follows open-source standards and signals engineering maturity.

4. Added LICENSE (MIT License)

Created a formal MIT license with author attribution.

Enables legal use, modification, and distribution.

Outcome:
Makes the repo production-complete and compliant with GitHub norms.

5. Banner Image Added to Repository

A professional repository banner was created and uploaded.

README updated to display banner at the top for branding and visual impact.

Outcome:
Enhances visual identity and professionalism of the GitHub project.

6. Repository Navigation Improved

Set up internal documentation cross-links.

Cleaned structural layout in the README.

Ensured consistency across project folders.

Outcome:
Improved user experience and clarity for anyone reviewing the project.

7. Prepared Next Steps for the F1 Analytics Pipeline

The upcoming work was planned and defined:

Position evolution analysis

Lap-by-lap pace deltas

Sector performance breakdown

Telemetry (throttle / brake / speed trace) overlays

Consistency Index metric

SQL table export of FastF1 outputs

Power BI driver scorecard

Phase 1 of “Driver Buy Recommendation Model”

Outcome:
Clear direction for the next major development phase.

## 🔄 Ongoing Updates  
Each milestone added to this log will help recruiters see the entire engineering and analytics process from start to finish, demonstrating:
- Technical skill  
- Analytical thinking  
- Documentation discipline  
- Real-world motorsport relevance  

This log will be updated as new notebooks, data pipelines, dashboards and insights are added.
