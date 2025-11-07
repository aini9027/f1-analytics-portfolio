
# Power BI Dashboard Layout Brief — Formula 1 Race Strategy Analytics

## 🎯 Purpose & Audience
This dashboard is designed for **Formula 1 team strategists, analysts, and performance managers**.  
Its goal is to present a **clear, data-driven overview** of how drivers, teams, and strategies perform across seasons — emphasizing pit-stop timing, consistency, and qualifying-to-race outcomes.

---

## 🗂️ Dashboard Pages

### **Page 1 — Season Overview**
**Objective:** Provide an executive snapshot of driver and team performance.
- **KPIs (cards):**
  - Total Races
  - Total Points Earned
  - Average Positions Gained
  - Podium Count (%)
- **Visuals:**
  - **Bar Chart:** Top 10 Drivers by Wins
  - **Line Chart:** Points by Season (Driver Comparison)
  - **Matrix Table:** Constructor Standings by Year
- **Slicer/Filter:** Season, Team, Driver

---

### **Page 2 — Qualifying vs Race**
**Objective:** Examine how qualifying positions translate into final results.
- **Visuals:**
  - **Scatter Plot:** Grid Position vs Finish Position (colored by Constructor)
  - **KPI Cards:** Average Grid Position, Average Finish Position
  - **Text Card:** Correlation (r-value between grid and finish)
  - **Gauge/Bar:** Driver Consistency Index (lower variance = better)
- **Insights:** Identify overperformers and underperformers on race day.

---

### **Page 3 — Pit Stop Strategy**
**Objective:** Highlight pit-stop timing efficiency and its impact on outcomes.
- **Visuals:**
  - **Gantt-style Chart:** Pit Laps per Driver per Race
  - **Bar Chart:** Average Pit Duration by Team
  - **KPI:** Average Positions Gained/Lost after Pit
- **Additional Filters:** Circuit, Tyre Compound, Weather (if available)
- **Insights:** Compare undercut vs overcut effectiveness.

---

### **Page 4 — Circuit Insights**
**Objective:** Analyze performance by track characteristics.
- **Visuals:**
  - **Map:** Circuits with Average Finish Position (color gradient)
  - **Heatmap:** Driver vs Circuit Average Finish
  - **Bar Chart:** Team Points by Circuit
- **Slicers:** Season, Circuit, Driver
- **Insights:** Identify “strong” and “weak” circuits for each team.

---

### **Page 5 — Executive Summary**
**Objective:** Present the top-level takeaways for management.
- **Cards:** 3–4 headline metrics (Best Driver, Fastest Team, Avg Pit Time)
- **Text Box:** Key Insights & Recommendations
- **Visual:** “Pit Under SC” Advantage KPI (e.g., +0.8 avg positions)
- **Design Tip:** Use red highlights for positive outliers and grey for neutral.

---

## 🧱 Data Model Guidelines
- **Tables:**
  - `drivers`, `constructors`, `races`, `results`, `pit_stops`, `lap_times`
- **Relationships:**
  - `races[race_id] → results[race_id]`
  - `results[driver_id] → drivers[driver_id]`
  - `results[constructor_id] → constructors[constructor_id]`
  - `races[circuit_id] → circuits[circuit_id]`
- **Hide ID fields** and show only readable names (Driver, Constructor, Circuit).
- **Calculated Measures:**
  - `Total Points = SUM(results[points])`
  - `Avg Finish Position = AVERAGE(results[position])`
  - `Avg Pit Duration = AVERAGE(pit_stops[duration_ms])`
  - `Positions Gained = results[grid] - results[position]`
  - `Consistency Index = STDEV.P(results[position])`

---

## 🎨 Design Guidelines
- **Color Palette:** Dark-grey background, F1 Red accent, neutral whites for text.
- **Layout:**
  - Top Row: KPIs
  - Middle: Core visuals
  - Right Pane: Filters/Slicers
- **Font Choices:** Segoe UI, Lato, or Roboto for readability.
- **Interactions:** Enable cross-filtering between charts for deeper insights.

---

## 🧩 Deliverables
- `.pbix` file (Power BI dashboard)
- Screenshot exports (placed under `/reports/`)
- Updated README linking visuals and insights.

---

**Author:** Ammar Haider  
**Project:** Formula 1 Race Strategy Analytics  
**Tools:** Power BI, SQLite, Python, SQL
