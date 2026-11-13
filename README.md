# Enterprise AI Operations, Escalation & Snapdragon Telemetry Pipeline

An interactive *Stateful Multi-Agent Time Boundary Monitor, **Automated Shift Escalation Hub, and **Snapdragon Performance Telemetry Pipeline* built with *Streamlit, **Python, and **SQLite. Monitors account SLA time boundaries across production teams, dispatches automated 9:00 PM warning and 10:00 PM critical breach escalations, tracks Snapdragon hardware performance metrics, and exports structured telemetry datasets for **Power BI* dashboards.

## Key Features
* *Stateful Multi-Agent Escalation Engine (master_ai_pipeline.py):* Evaluates account monitoring nodes against strict shift time boundaries, automatically triggering 9:00 PM Shift Warnings (warning_9pm_sent) and 10:00 PM Critical Drift Breach Escalations (breach_10pm_sent) with formatted governance alerts.
* *Snapdragon Performance Monitor (snapdragon_performance_monitor.py):* Tracks hardware execution telemetry, throughput, and latency baselines stored in snapdragon_telemetry_metrics.csv.
* *Multi-Vault Telemetry Storage:* Persists operational and cloud telemetry across local SQLite databases (enterprise_telemetry_vault.db, azure_telemetry_vault.db, operations_pipeline_v3.db).
* *Automated Power BI Data Pipeline:* Populates power_bi_telemetry.csv and production_telemetry_metrics.csv in real time for direct enterprise BI visualization.

## Architecture Flow
text
[Telemetry Vaults (.db) & Metrics (.csv)]
       │
       ▼
[Stateful Multi-Agent Monitor (master_ai_pipeline.py)]
       ├──► [Shift Warning] (9:00 PM SLA Alert)
       ├──► [Critical Breach] (10:00 PM Escalation)
       └──► [Streamlit Operations Hub] ──► [Power BI Export (power_bi_telemetry.csv)]


## Project Structure
* master_ai_pipeline.py — Main Streamlit application for Account Monitoring Nodes, time-boundary shift escalations, and Power BI dataset generation.
* snapdragon_performance_monitor.py — Performance monitoring module for Snapdragon telemetry metrics.
* enterprise_telemetry_vault.db / azure_telemetry_vault.db / operations_pipeline_v3.db — SQLite telemetry storage vaults.
* power_bi_telemetry.csv — Auto-populated data matrix for Power BI reporting.
* production_telemetry_metrics.csv — Production team performance metrics dataset.
* snapdragon_telemetry_metrics.csv — Snapdragon runtime performance telemetry dataset.

## Quick Start

1. *Clone the repository:*
   bash
   git clone https://github.com
   cd Enterprise_Agentic_Pipeline
   

2. *Install dependencies:*
   bash
   pip install streamlit pandas
   

3. *Run the Enterprise AI Operations & Escalation Hub:*
   bash
   streamlit run master_ai_pipeline.py
   

4. *Run the Snapdragon Performance Monitor:*
   bash
   streamlit run snapdragon_performance_monitor.py
