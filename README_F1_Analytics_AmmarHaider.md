# 🏎️ Formula 1 Race Strategy Analytics
**End-to-End Data Analytics Project (SQL | Python | Power BI | Tableau)**  

## 🎯 Project Goal
Analyze Formula 1 race, qualifying, and lap data to uncover **how driver performance, team strategies, and pit-stop timing affect race outcomes** — and present findings through **data-driven insights and interactive dashboards**.

---

## 💡 Objectives
- Clean, structure, and integrate multi-source F1 datasets (Ergast API, Kaggle, or FastF1).  
- Perform **SQL-based exploratory analysis** on races, drivers, constructors, and circuits.  
- Visualize **driver consistency, qualifying vs. race correlation, and pit-stop strategy**.  
- Derive actionable insights that could help a “team principal” or strategist make decisions.  
- Deliver results as a **professional analytics case study** with code, queries, and visuals.

---

## 🧩 Key Questions Explored
1. Which drivers and teams are most consistent across seasons?  
2. How strong is the correlation between qualifying grid position and final result?  
3. How much time is typically gained or lost through pit-stop strategy?  
4. Which circuits favor which teams or drivers?  
5. What is the impact of pitting under a safety car vs. normal race conditions?  

---

## 🗂️ Project Structure
```
f1-analytics-portfolio/
│
├─ data/                     # CSVs or API extracts (drivers, races, results, etc.)
├─ notebooks/
│   ├─ 01_data_import_and_cleaning.ipynb
│   ├─ 02_exploratory_analysis.ipynb
│
├─ sql/
│   ├─ schema.sql            # relational data model
│   ├─ queries.sql           # analytical SQL queries
│
├─ dashboard/
│   ├─ power_bi/ or tableau/ or streamlit_app.py
│
├─ reports/
│   ├─ executive_summary.md  # key insights
│   ├─ slide_deck.pdf
│
├─ README.md
└─ requirements.txt
```

---

## 🛠️ Tech Stack
| Category | Tools / Libraries |
|-----------|-------------------|
| Data Ingestion | Python (pandas, requests), Ergast API, FastF1, Kaggle CSVs |
| Database | SQLite (for demo), PostgreSQL (for production) |
| Analysis | SQL, pandas, numpy |
| Visualization | Power BI / Tableau / Plotly / Matplotlib |
| Reporting | Markdown, PDF, PowerPoint slides |

---

## 🔍 Data Sources
- **[Ergast API](https://ergast.com/mrd/)** – historical race results, qualifying, pit stops, lap times.  
- **[FastF1 Library](https://theoehrly.github.io/Fast-F1/)** – timing, telemetry, and tyre data.  
- **Kaggle Datasets** – pre-compiled F1 historical CSVs for easier offline use.  

---

## 📊 Analytical Highlights
| Area | Example Analysis |
|------|------------------|
| Performance | Top drivers & constructors by wins, podiums, and points |
| Consistency | Standard deviation of finishing positions |
| Strategy | Average positions gained after pit stops |
| Qualifying vs Race | Correlation of grid vs finish positions |
| Circuit Analysis | Best & worst tracks per driver/team |
| Telemetry | Lap-by-lap speed / tyre / safety-car patterns (FastF1) |

---

## 🖥️ Deliverables
- 🧮 **Clean Database** (`data/f1.db`)  
- 🗃️ **SQL Queries** (12+ analysis scripts)  
- 📓 **Jupyter Notebooks** (cleaning + EDA)  
- 📈 **Interactive Dashboard** (Power BI / Tableau / Streamlit)
- 📊 **Power BI Dashboard:**  
Visuals under development — to be added in the next project iteration.  
The layout and metrics are described in `dashboard/powerbi_layout.md`.

Exploratory Data Analysis — November 2025 Update

This update adds a full SQL-driven exploratory notebook demonstrating analytical thinking and visualization skills.

New Components

notebooks/02_exploratory_analysis.ipynb

SQL-first analysis with clean Python visualizations

Queries include:

Wins per driver

Average points per driver

Positions gained (grid − finish)

Pit-stop durations by team

Grid vs Finish correlation (Pearson & Spearman)

Circuit performance summary

Simple Matplotlib visuals for clarity and reproducibility

Highlights

Pure SQL workflow showing ability to extract insights from relational data

Verified in Google Colab using SQLite (f1.db)

Plots designed to translate directly into Power BI visuals

Notebook ready for inclusion in analytics dashboards and reports

- 🧾 **Executive Summary Report** (1-page business insights)  

---

## 🧠 Key Insights Example
> - **Early pit-stop advantage**: Drivers pitting before lap 15 gained an average of +0.7 positions.  
> - **Qualifying ↔ Finish correlation**: r = 0.68 — track position remains crucial.  
> - **Consistency outliers**: Certain midfield drivers had podium-rate consistency over full seasons.

---

## 🚀 How to Use
1. Clone this repository  
   ```bash
   git clone https://github.com/ammarhaider/f1-analytics-portfolio.git
   cd f1-analytics-portfolio
   ```
2. Place CSVs from Kaggle/Ergast into `/data`.  
3. Run `notebooks/01_data_import_and_cleaning.ipynb`.  
4. Execute the SQL scripts in `/sql`.  
5. Open the dashboard file (Power BI/Tableau) to explore visuals.  

---

## 📘 Latest Updates
- Added interactive data import and EDA notebooks (Nov 2025)
- Included sample SQLite database (`data/f1.db`)
- All analysis tested and validated in Google Colab
- --

## 📅 Future Enhancements
- Add predictive modeling (finish position regression).  
- Integrate weather / safety-car data for race simulations.  
- Compare multiple seasons dynamically.  
- Deploy Streamlit web app version of the dashboard.  

---

## 👨‍💻 Author
**Ammar Haider**  
Data Analytics Enthusiast | F1 Fan | Portfolio Builder   
[LinkedIn Profile 🔗](#)  |  [GitHub Repo 🔗](#)
