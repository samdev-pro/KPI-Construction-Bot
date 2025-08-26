# 🏗️ Construction KPI Bot

The **Construction KPI Bot** is a Python-based automation tool that demonstrates:
- **Data handling** with [pandas](https://pandas.pydata.org/)
- **Visualization** with [matplotlib](https://matplotlib.org/)
- **Reporting** with [fpdf2](https://py-pdf.github.io/fpdf2/)
- **Automation** with built-in email support

It generates a professional PDF report of construction project KPIs (Key Performance Indicators) from a CSV file, complete with charts and summary tables.

---

## ✨ Features
- Load and process project data from a CSV file
- Generate charts for:
  - **Schedule Completion (%)**
  - **Budget Variance (%)**
- Create a polished PDF report with:
  - Per-project KPIs
  - Data tables
  - Charts embedded in-line
- Automated email delivery of the report
- Secure handling of email credentials using environment variables

---

## ⚙️ Setup

### 1. Clone the Repository
```bash
git clone https://github.com/your-username/kpi-bot.git
cd kpi-bot
```

### 2. Create and activate a virtual environment
```bash
python3 -m venv venv
source venv/bin/activate   # On macOS/Linux
venv\Scripts\activate      # On Windows
```

### 3. Install dependencies
```bash
pip install -r requirements.txt
```

### 4. Configure environment variables
Create a .env file in the project root:
```bash
EMAIL_HOST=smtp.gmail.com
EMAIL_PORT=587
EMAIL_USER=your_email@example.com
EMAIL_PASS=your_app_password
```
⚠️ **Security Note**: Never hardcode credentials into your scripts. Always store sensitive data like email passwords in environment variables.

### ▶️ Usage

1. Add or update your mock_data.csv with project metrics
2. Run the KPI Bot:
```bash
python3 kpi_bot.py
```
3. The script will:
   * Process the CSV with pandas
   * Generate KPI charts with matplotlib
   * Create a PDF report
   * Send the report to configured email recipients

---

### 📑 Sample Output

**PDF Report Includes:**
* Project-level KPI summary tables
* Schedule Completion chart
* Budget Variance chart
  
Example (illustrative only):
```bash

Project: Building A
 - Budget: $1,200,000.00
 - Actual Cost: $1,180,500.00
 - Budget Variance %: -1.6%
 - Scheduled Tasks: 120
 - Completed Tasks: 95
 - Schedule % Complete: 79.2%

```
📎 The PDF will also embed **bar charts** showing project schedule and budget performance.

---

### 🚀 Future Improvements

* Add trend analysis over time
* Support for Excel input files
* More KPIs (change orders, subcontractor performance, etc.)
* Web dashboard integration

---

### 📬 Contact

[Sam Huss]
Feel free to fork, open issues, or suggest improvements!
