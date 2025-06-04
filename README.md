# 🏥 NHS A&E Performance Dashboard (SQL + Tableau | Nov 2024 – Apr 2025)

📌 **Project Overview**  
This project analyzes 6 months of A&E (Accident & Emergency) activity and performance data from NHS England, using SQL and Tableau to explore trends in patient volumes, breach rates, and hospital pressure.  
The goal: uncover system inefficiencies and deliver public-sector-ready insights using real-world healthcare data.

---

## 🔍 Business Questions

- 📈 How have A&E attendances and breaches changed over time?
- ⏱️ Which providers consistently fail to meet the 4-hour standard?
- 🚥 Can we classify hospitals into performance bands?
- 📍 What are the top 5 most pressured NHS Trusts?
- 🗓️ Are there monthly or seasonal patterns worth acting on?

---

## 🛠️ Tools Used

| Tool        | Purpose                             |
|-------------|--------------------------------------|
| PostgreSQL  | SQL querying + data cleaning         |
| DBeaver     | SQL IDE                              |
| Excel       | XLS to CSV conversion, % cleaning    |
| Tableau     | Interactive data storytelling        |
| Git & GitHub| Version control and public portfolio |

---

## 📊 Project Workflow

### 1. **Data Collection & Cleaning**
- Source: [NHS A&E Statistics – NHS England](https://www.england.nhs.uk/statistics/statistical-work-areas/ae-waiting-times-and-activity/)
- Months: **Nov 2024 → Apr 2025**
- Removed footnotes, headers, merged cells
- Cleaned percent values (removed `%` symbols)
- Saved as `.csv` for PostgreSQL import

### 2. **SQL Table Design & Load**
- Table: `nhs_ae_data`
- Imported cleaned monthly data via DBeaver
- Used `NULLIF()` to prevent division by zero

### 3. **SQL Analysis Queries**
- 🧮 Monthly trend of A&E attendances
- ⚠️ Breach rate by provider per month
- 🚩 Flagging providers as:
  - `Critical` (>40% breached)
  - `High` (>30%)
  - `Acceptable` (≤30%)
- 📍 Top 5 worst-performing trusts each month

### 4. **Dashboard Design (Tableau)**
- Connected to exported SQL insight `.csv`
- Visuals:
  - Monthly breach trend
  - Monthly attendance trend
  - Top 5 breached trusts
  - Trusts Performance flag by Attendance 
- Filters:
  - Month dropdown
  - Perfomance flag dropdown
  - Trust name search Bar
- Shared publicly via Tableau Public

---

## 📈 Final Dashboard

🔗 **Live Dashboard (Tableau Public)**  
[Click here to view](https://public.tableau.com/app/profile/olanrewaju.oyenekan/viz/NHSAEPerformanceDashboardNov2024Apr2025/NHSAEPerformanceDashboardNov2024Apr2025)

📦 **Full Packaged Workbook (`.twbx`)**  
Located in `dashboard/nhs_ae_dashboard_multi_months.twbx`

---

## 📂 Folder Structure
```
nhs-ae-performance-sql-tableau/
├── data/
│   ├── raw/               # Original .xls source files
│   ├── processed/         # Cleaned monthly .csv files
│   └── insights/          # Final SQL export results (summary files for Tableau)
│
├── sql/
│   ├── create_table.sql   # Table schema and import SQL
│   └── analysis_queries.sql # Analytical queries for insights
│
├── dashboard/
│   └── nhs_ae_dashboard_multi_months.twbx  # Tableau dashboard file
│
├── visuals/               # 📸 dashboard preview
│   └── dashboard_preview.png
|
└── README.md              # Project overview, tools used, and instructions
```
---

## 🧠 Key Insights

- 🕒 Breach rates spiked in winter months (Dec–Feb)
- 🏥 Over 20 NHS Trusts flagged as `Critical`
- 📉 Trusts with 30,000+ patients often had highest delays
- 📊 Consistent underperformance observed in same regions across months

---

## 📢 Professional Highlights

- Full SQL workflow with joins, filters, CASE, and performance logic
- Dashboard communicates healthcare capacity under pressure
- Public sector domain with strong storytelling and interactivity
- End-to-end project (clean → SQL → dashboard → publish)

---

## 🚀 Future Work

- Add regional/geospatial maps in Tableau
- Extend dataset to full 12 months
- Predict breach likelihood with Python model
- Rebuild dashboard in Power BI (next portfolio project!)

---

## 📬 Let’s Connect

📫 I'm actively seeking **Data Analyst roles (UK or remote)**.  
View more projects at: [github.com/Larry0615](https://github.com/Larry0615)

---

