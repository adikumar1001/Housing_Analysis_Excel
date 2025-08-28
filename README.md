# 🏡 East Coast Living Index — *Best Place to Live* (Excel Dashboard)

An **Excel-based** decision dashboard that ranks East Coast states by quality-of-life factors such as **safety, healthcare, education, rent, cost of living, crime, climate, and sunshine**. Built with **PivotTables, slicers, charts, and lightweight VBA** for reset/navigation.

---

## 🔎 Preview

> KPI examples visible on the dashboard: **Best Place to Live**, **Safety Index**, **Health Score**, **Average Rent**, **Education Index**, **Avg Annual Temperature**, **Cost of Living**, **Crime Rate**, **Sunny Days**.  
> Persona buttons (top right) filter recommendations for **Students (18–22)**, **Young Adults (18–35)**, **Families (35–55)**, **Middle‑Aged (55–70)**, and **Seniors (70+)**.

---

## 📦 Repository Contents
```
.
├─ Best place to live data analysis project.xlsm   # Main interactive dashboard (macro‑enabled)
├─ Average Housing Rent.xlsx                       # Rent by state
├─ Safety Ratings of the states.xlsx               # Safety index
├─ Crime Rate Dataset.xlsx                         # Crime statistics
├─ cost-of-living-index-by-state-2025.csv          # Cost-of-living index
├─ README.md

```

---

## 🧭 How to Use
1. **Download** the repo and open `Best place to live data analysis project.xlsm`.
2. In Excel, click **Enable Editing** and **Enable Content** (macros) when prompted.
3. Use the **Region** and **State** slicers on the left to scope results.
4. Explore KPIs and charts:
   - **Average Rent by State** (bar)
   - **Crime Rate vs Safety Index** (combo)
   - **Education Index by State** (column)
   - **Housing Share of Total Cost of Living** (area)
   - US **map** highlighting your current selection
5. Click **Reset Dashboard** (top-left) to clear filters.  
6. Optional: Persona buttons tailor suggested states for different life stages.


---

## ⚙️ Data & Refresh
- Data files live next to the workbook (no external DB required).  
- If you relocate the files, update connections via **Data → Queries & Connections** (or **Data → Get Data → Data Source Settings**) and refresh.
- Keep the **CSV** and **XLSX** column names stable to avoid breaking charts/measures.

---

## 🧪 Method (High Level)
- Each metric is scaled to a comparable range (e.g., min–max or index-style scores).  
- A composite **Living Index** ranks states across multiple dimensions (rent/cost ↓ better; safety/education/health/sunshine ↑ better).  
- Persona filters adjust emphasis (e.g., students → affordability & safety; families → schools, safety, rent).  
- All steps are transparent in the workbook so you can tweak weights and thresholds.

> Tip: If you rebuild the scoring, a simple pattern is:  
> **`Index = Σ (w_i × scaled_metric_i)`**, where `Σ w_i = 1`. Keep weights in a **Weights** table to make them easy to edit.

---

## 🛠 Excel Features Used
- PivotTables & PivotCharts
- Slicers & Map chart
- Conditional formatting for KPI cards
- Named ranges / helper tables for scoring
- **VBA macros** for one‑click **Reset** and **navigation**

---

## ✅ QA Checklist
- After refresh, confirm that slicers filter **all** charts (Format → *Edit Interactions*).  
- Verify sign of each metric (e.g., **lower** rent/cost/crime is better).  
- Spot-check extreme states to ensure the composite ranking reacts as expected.

---

## 🚀 Roadmap
- Expand beyond East Coast to **all 50 states**.
- Add **job market** and **tax burden** metrics.
- Publish a **read‑only web version** via Power BI or Excel for web.

---

## 👤 Author
**Aditya Kumar** — Analytics & Excel dashboards  
Feedback and PRs are welcome!

---
