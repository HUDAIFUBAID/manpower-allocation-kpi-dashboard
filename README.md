# Manpower Allocation KPI Dashboard (Power BI)

A Power BI dashboard that scores the Manpower Allocation team every month against an 8-section KPI sheet (100 marks), and shows the total score and performance rating automatically.

![Dashboard](dashboard.png)

## What it shows

| Section | Max marks | Rule (summary) |
|---|---|---|
| Client Demobilization Forecasting | 15 | % of demobilizations forecast 7+ days early: 95–100% = 15, 90–94% = 12, 80–89% = 8 |
| Daily IDLE Circulation (9 AM) | 10 | 0 missed days = 10, 1–2 = 7, 3–4 = 4, more = 0 |
| Skill Mapping & Training | 10 | Regular = 10, Partial = 6, Minimal = 3, None = 0 |
| IDLE Manpower Control | 30 | Avg IDLE % ≤ 2% = 30, 2–3% = 10, 3–4% = 2, then −2 per extra 1% |
| Mobilization & Trade Test | 10 | +5 / −5 for trade test and mobilization within 3 days |
| ERP Compliance | 10 | Full compliance = 10, any failure = 0 |
| Attendance Accuracy | 10 | 100% = 10, 90–99% = 5, 80–89% = 0, −2 per 10% below 80% |
| Reporting to Manager | 5 | Daily and monthly reports on time = 5 |

**Rating:** 90–100 Excellent · 75–89 Very Good · 60–74 Satisfactory · below 60 Needs Immediate Improvement

## Features

- Month selector: every card, the score, the rating, the table and the chart update for the chosen month
- Score and forecast-% rings, colour-coded cards, red highlight for negative marks
- All scoring done with DAX measures, organised into Inputs / Section Marks / Totals folders

## How to use

1. Open `chenoth llc project.pbix` in Power BI Desktop.
2. Each month: **Home → Transform data → Source**, add one row with that month's values, then **Close & Apply**.
3. Pick the month in the Month dropdown.

## Data columns

`Month, Total_Demob, Forecast_Before_7_Days, Avg_Idle_Pct, TradeTest_Within_3Days, Mob_Within_3Days, Missed_Days, Skill_Level, ERP_Compliance, Attendance_Percentage, Daily_Report_On_Time, Monthly_Report_On_Time`

## Tools

Power BI Desktop · DAX · Power Query
