# <img src="https://raw.githubusercontent.com/lucasalamanni/Global-Force-Automatizaci-n-de-un-Dashboard-interactivo-/main/Captura%20de%20pantalla%202026-05-29%20092727.png" alt="GlobalForce Dashboard" width="100%"/>

# GlobalForce - Workforce Executive Reporting Automation

## 🎥 Project Demo

<p align="center">
  <a href="https://youtu.be/cOYKCcVSubc?si=nGSUx2DoNSSo0pDW" target="_blank">
    <img src="https://img.youtube.com/vi/cOYKCcVSubc/maxresdefault.jpg" alt="GlobalForce Demo Video" width="80%">
  </a>
</p>

<p align="center">
  <a href="https://youtu.be/cOYKCcVSubc?si=nGSUx2DoNSSo0pDW">
    ▶️ Watch Full Process Demo on YouTube
  </a>
</p>

---

## 📌 Project Overview

This project automates the generation of workforce executive reports for GlobalForce enterprise clients by integrating multiple internal data sources into a centralized analytics pipeline.

The solution reduces the manual reporting process from **3 days to less than 1 hour**, enabling analysts and client managers to access updated executive KPIs through an interactive Power BI dashboard and exportable PDF reports.

---

# 🚀 Business Problem

GlobalForce clients require monthly executive reports including:

- Workforce turnover
- Cost analysis by region
- Capacity utilization
- Workforce operational metrics

Previously, these reports were manually prepared in Excel, requiring extensive consolidation efforts across multiple files and systems.

This project automates the complete workflow using:

- Google Drive
- n8n
- Supabase
- PostgreSQL
- Power BI

---

# 🏗️ Solution Architecture

## End-to-End Automated Flow

```mermaid
flowchart LR

A[Google Drive CSV Uploads] --> B[n8n ETL Pipeline]

B --> C[Supabase Staging Tables]

C --> D[PostgreSQL Data Model]

D --> E[Power BI Dashboard]

E --> F[Executive PDF Report]
```

---

# ⚙️ Technologies Used

| Technology | Purpose |
|---|---|
| n8n | Workflow orchestration and ETL automation |
| Google Drive | File ingestion and trigger source |
| Supabase | Cloud PostgreSQL database and staging environment |
| PostgreSQL | Centralized relational data model |
| Power BI | Interactive executive dashboard and PDF reporting |
| CSV Files | Source operational workforce data |

---

# 📂 Data Sources

The ETL workflow processes multiple workforce datasets:

| Dataset | Description |
|---|---|
| Departments | Organizational departments |
| Employees | Employee master data |
| Work Hours | Monthly workforce utilization |
| Workforce Costs | Salary and operational costs |
| Regions | Geographic operational regions |

---

# 🔄 n8n ETL Workflow

The workflow was developed in n8n using automated Google Drive triggers.

Each workflow follows the same ETL pattern:

1. Detect new CSV file uploaded to Google Drive
2. Download the file automatically
3. Extract and parse CSV contents
4. Load records into Supabase staging tables

---

# 📌 Workflow Components

## Google Drive Triggers

Each data source has its own automated trigger configured with:

- Polling every minute
- File creation event detection
- Dedicated source folder

### Tracked Folders

| Trigger | Dataset |
|---|---|
| Departments Drive Trigger | Departments |
| Employees Drive Trigger | Employees |
| Work_hours_trigger | Work Hours |
| Work force trigger | Workforce Costs |
| Region trigger | Regions |

---

# 🧱 Data Pipeline Structure

## ETL Standardization

Every workflow branch follows this architecture:

```text
Google Drive Trigger
        ↓
Download File
        ↓
Extract From File
        ↓
Insert Into Supabase Staging Table
```

---

# 🗄️ Database Architecture

The project uses a staging-based architecture inside Supabase/PostgreSQL.

## Staging Tables

```sql
departments_stagging
employees_staging
work_hours_staging
workforce_costs_staging
regions_stagging
```

These tables act as the ingestion layer before transforming the data into the analytical model consumed by Power BI.

---

# 📊 Power BI Dashboard

The dashboard provides executive visibility into workforce operations through interactive KPIs and visualizations.

## Main KPIs

- Employee Turnover
- Workforce Cost by Region
- Capacity Utilization
- Overtime Analysis
- Operational Workforce Distribution

## Dashboard Features

- Interactive filtering
- Regional analysis
- Monthly trend tracking
- Exportable PDF reports
- Automated data refresh from Supabase

---

# 📈 Key Benefits

| Before Automation | After Automation |
|---|---|
| 3-day manual process | Less than 1 hour |
| Manual Excel consolidation | Automated ETL pipeline |
| High risk of human error | Centralized validated data |
| Static reports | Interactive dashboards |
| Manual report exports | One-click PDF generation |

---

# 👥 Users

## GlobalForce Analyst

Responsible for:

- Uploading operational files
- Reviewing KPIs
- Generating executive PDF reports

## Client Manager

Uses dashboards and exported reports for:

- Workforce analysis
- Strategic decision-making
- Client reporting

---

# 🔁 Operational Flow

```text
Analyst uploads CSV files to Google Drive
                ↓
n8n detects new files automatically
                ↓
ETL pipeline processes the datasets
                ↓
Supabase staging tables are updated
                ↓
Power BI dashboard refreshes
                ↓
Analyst validates KPIs
                ↓
Executive PDF report generated
                ↓
Report delivered to client
```

---

# 📌 Repository Structure

```text
📦 GlobalForce Dashboard Automation
 ┣ 📂 n8n-workflows
 ┣ 📂 screenshots
 ┣ 📂 sql-model
 ┣ 📂 powerbi-dashboard
 ┣ 📜 README.md
 ┗ 📜 workflow.json
```

---

# 🔐 Data Governance & Scalability

The architecture was designed to support:

- Scalable monthly processing
- Centralized data governance
- Cloud-based access
- Automated ingestion pipelines
- Future integration with APIs and ERP systems

---

# 📄 Future Improvements

Potential enhancements include:

- Real-time dashboard refresh
- API-based ingestion instead of CSV files
- Automated email delivery of reports
- AI-driven workforce forecasting
- Data quality monitoring layer

---

# 👨‍💻 Developed By

**Lucas Alamanni**  
Data Analyst | BI Developer | Automation Enthusiast

---

# 📬 Contact

Feel free to connect for collaboration, analytics projects, or automation solutions.

- LinkedIn
- GitHub
- Portfolio

---
