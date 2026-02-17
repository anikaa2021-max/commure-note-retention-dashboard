# Note Retention Dashboard (Retool)

This repository contains a Retool dashboard built as a case-style project
to analyze note-creation retention across the clinical documentation funnel:
**AI Draft → Provider Edit → Signed Note**.

The goal is to help Customer Success and Operations teams identify
low-retention (“at-risk”) sites early using clear metrics, alerts, and drill-downs.

---

## Dashboard Overview

This dashboard shows:
- Retention % by **site**, **provider**, and **note type**
- Filtering by note stage (AI Draft, Provider Edit, Signed Note)
- Color-coded alerts for low retention
- Drill-downs to investigate specific sites
- Auto-refresh to simulate near real-time event ingestion

---

## Retention Metric

Retention is calculated as:

Retention % = (tokens_after / tokens_before) * 100


- Safely handles `tokens_before = 0` (returns 0)
- Visual thresholds:
  - Green: ≥ 80%
  - Yellow: 60–79%
  - Red: < 60%

---

## How to View the Dashboard

1. Download the Retool JSON file from this repository
2. Log into https://retool.com
3. Create a new app → **Import from JSON**
4. Upload the dashboard JSON
5. When prompted, upload the provided CSV file

The full interactive dashboard will load automatically.

---

## Tech Stack

- Retool
- JavaScript (query logic and filtering)
- CSV-based event data (simulated edit-event stream)

---

## Author

Anika Aggarwal
