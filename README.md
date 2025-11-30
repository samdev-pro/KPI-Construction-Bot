# 🤖 KPI Construction Bot

> A Python-based automation engine that generates KPI reports for construction Quality Control (QC) and budgeting workflows.

> *(Automates ETL, reporting, and email delivery to improve efficiency and timeliness of data insights.)*

---

## 🧭 Overview

The **KPI Construction Bot** demonstrates the potential of data-driven automation in construction operations — showcasing how streamlined workflows can deliver clear visual insights and measurable efficiency gains.

Developed to eliminate repetitive manual reporting, the bot automatically generates KPI summaries and PDF/email reports for QC, NCR, and budget tracking.  

The current version reads data from a CSV file for demonstration purposes but can be adapted to integrate with platforms like Procore or Smartsheet via their APIs. To accelerate development, I used ChatGPT and Cursor AI as part of the build process — illustrating how AI-assisted tools can enhance coding speed and workflow efficiency.

By automating data collection and visualization, this system provides consistent, repeatable, and transparent KPI reporting for project managers and commissioning teams.

📸 [View KPI Report PDF](https://github.com/samdev-pro/KPI-Construction-Bot/blob/main/output/kpi_report.pdf)

---

## 📁 Project Structure

```
construction_kpi_bot/
│
├─ kpi_bot.py                     # CLI entrypoint
│
├─ src/
│   ├─ data_adapter.py            # CSV loading, cleaning, schema validation
│   ├─ metrics.py                 # KPI + ETL computations
│   ├─ charts.py                  # Matplotlib chart generation
│   ├─ layout.py                  # PDF layout primitives (cards, grids, spacing)
│   ├─ pdf_builder.py             # High-level PDF composition using ReportLab
│   ├─ emailer.py                 # SMTP send logic
│   └─ utils.py                   # helpers: formatting, date parsing, logger
│
├─ sample-data/
│   ├─ *.csv                      # CSV data files
│   └─ schema.md                  # CSV schema documentation
│
├─ assets/
│   └─ fonts/
│       ├─ NotoSans-Bold.ttf
│       ├─ NotoSans-ExtraBold.ttf
│       ├─ NotoSans-Medium.ttf
│       └─ NotoSans-Regular.ttf
│
├─ output/
│   └─ kpi_report_*.pdf           # Generated PDF reports
│
├─ tests/
│   └─ test_metrics.py            # Unit tests for KPI logic
│
├─ .env.example                   # SMTP, email recipients, runtime config
├─ requirements.txt               # Python dependencies
└─ README.md                      # This file
```

---

## 🧰 What I Did

**Data Engineering:** Python · Pandas · NumPy · ETL · CSV Transformation  
**Construction Tech:** Smartsheet · QC/NCR/Punch List Tracking  
**Automation & Visualization:** Matplotlib · ReportLab · Email Automation · PDF  
**Dev Tools:** GitHub · ChatGPT · Cursor  

---

## 🚀 Features

- Automated ETL pipeline that cleans and aggregates project data  
- Generates KPI visualizations (pass rate, punch list aging, budget usage)  
- Converts outputs to PDF reports and emails them to stakeholders  
- Scheduled automation with customizable frequency  

---

## 🧠 Tech Stack

| Category | Tools & Libraries |
|-----------|------------------|
| **Languages** | Python |
| **Data Processing** | Pandas · NumPy |
| **Visualization** | Matplotlib |
| **Reporting & Output** | ReportLab · CSV · Smartsheet |
| **Automation** | smtplib (Email) · Task Scheduler / Cron |
| **Version Control** | GitHub |

---

## 📊 Outputs

The generated PDF includes:

**Page 1: Overview**
- Header with project title
- Four KPI cards (Open NCRs, Inspection Pass Rate, Avg Days to Close NCR, Overdue Punch Items)
- Stats section with three donut charts (Budget, Pass/Fail, Punch List Items)

**Page 2: Detailed Reports**
- Full-width bar chart: Open NCRs by Responsible Party
- Full-width bar chart: Aging Punch List Report
- Full-width bar chart: Systems Most Frequently Failed

**Page 3+: In-Depth**
- Full-width table: Punch List Roll-Up Report
- Grouped by responsible party
- Columns: Primary, Responsible Party, Aging Bucket, Status

---

## ⚙️ How It Works

1. **Extract** – Pulls exported data from Smartsheet or CSV input files.  
2. **Transform** – Uses Pandas to clean, merge, and calculate project KPIs.  
3. **Visualize** – Builds Matplotlib charts summarizing performance trends.  
4. **Automate** – Compiles charts into PDF reports and emails them automatically to project stakeholders.

---

## 📈 Results & Impact

This automation tool was developed to demonstrate the potential of data-driven reporting in construction operations — showing how automation can deliver clear visual insights and measurable efficiency gains.

By reducing manual reporting time, QC and project managers can focus on analysis instead of data preparation.

The system provides consistent, repeatable, and easily auditable KPI reporting, enabling faster insights and greater project transparency.

---

## 🧩 Future Improvements

- Add Smartsheet API and Procore integration for real-time data ingestion
- More KPIs (change orders, subcontractor performance, etc.)
- Implement web dashboard output (Astro/React) for interactive KPI visualization
- Integrate Slack or Teams notifications for weekly report summaries
- Web dashboard integration

---

## 🤝 Contact

Interested in how I can help your team transform its construction data workflows? Let’s connect.<br />
📧 [Email Me](mailto:sam@samhuss.dev)  💼 [LinkedIn](https://www.linkedin.com/in/samhuss/)
