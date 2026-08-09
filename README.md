# ClinData Explorer: AI-Powered Cohort & Data Quality Explorer

> **Track 2 – AI for Smarter Patient Care Hackathon**

---

## 1. Project Title

**ClinData Explorer** – An AI-powered web application for clinical researchers to define patient cohorts, audit data quality, and trace provenance using natural language.

---

## 2. Problem Statement

Hospital data is complex, fragmented, and messy. A single admission spans multiple tables (labs, medications, diagnoses, procedures, transfers, ICU observations). Researchers spend hours writing SQL and manually checking for data errors before they can even begin analysis.

**ClinData Explorer** solves this by providing a **transparent, AI-driven workspace** where researchers can:
- Define cohorts using plain English
- Receive instant data quality audits
- Trace every finding back to its source

All without sacrificing reproducibility or safety.

---

## 3. Proposed Solution

The system allows researchers to ask questions using natural language instead of writing SQL manually. The system then:

1. Interprets the research question
2. Generates human-readable inclusion/exclusion criteria
3. Converts requirements into SQL
4. Executes the query and retrieves records
5. Performs data-quality analysis (12 rules)
6. Identifies quality flags (missing values, duplicates, unit variations, temporal misalignments)
7. Shows source tables and provenance
8. Provides an explainable AI-generated summary

**Key Principle:** The system is designed to be **transparent, traceable, and research-oriented**.

---

## 4. Project Objective

To build a transparent, reproducible, and user-friendly web application that empowers clinical researchers to:

- Define patient cohorts using natural language
- Automatically assess the fitness of the underlying data for analysis
- Trace every result back to its exact source (table, field, record ID)
- Generate structured, AI-powered plain-English summaries for research communication

The goal is to **accelerate the data preparation phase** of clinical research while maintaining full auditability.

---

## 5. Selected Track — Track 2

**Track 2 — Cohort & Data Quality Explorer**

The system focuses on:
- Defining cohorts from natural language
- Visible inclusion/exclusion logic
- Data-quality analysis (missingness, duplicates, units, temporal issues)
- Measurement coverage and coding patterns
- Evidence and source-table provenance
- Distinguishing clinical findings from data-quality flags

---

## 6. Target Users

- Clinical-data researchers
- Healthcare data teams
- Clinical research students
- Educators working with structured clinical datasets

**Not intended for clinical decision-making.**

---

## 7. System Workflow / Data Flow

```text
Natural Language Query
        ↓
Cohort Interpretation
        ↓
Inclusion / Exclusion Logic
        ↓
Text-to-SQL (Gemini)
        ↓
SQL Validation
        ↓
Database Query (SQLite)
        ↓
Retrieved Cohort / Records
        ↓
Data Quality Analysis (12 Rules)
        ↓
Evidence & Provenance
        ↓
AI-Generated Summary (Gemini)
        ↓
Structured JSON Response
```

## 8. Features

| Feature | Description |
|---------|-------------|
| **Cohort Explorer** | Define patient cohorts using natural language; visible inclusion/exclusion logic. |
| **Data Quality Audit** | Automated detection of missing values, duplicates, temporal misalignments, unit variations (12 rules). |
| **Measurement Analysis** | Full visibility into chart events, lab events coverage, and prescription timeline alignments. |
| **Provenance & Evidence** | Every finding traces back to source table, field, record ID, and timestamp. |
| **Dataset Insights** | Full dataset-level analysis – table inventory, missingness, unit variation, ICD coding patterns. |
| **AI Summary** | Gemini-powered plain-English summary – research-only, never clinical. |

---
## 9. AI Method
The system uses Google Gemini (via LangChain) for two distinct tasks:

### Text-to-SQL Translation:
A zero-shot prompt containing the complete database schema is passed to Gemini. The model generates a valid SQLite SELECT query with explicit inclusion and exclusion criteria. Strict prompt engineering ensures the AI never generates destructive commands (DROP, DELETE, UPDATE) and refuses clinical advice requests.

### Cohort Summarization:
After data retrieval and quality analysis, the system passes the cohort statistics, quality flags, and query logic to Gemini. The model returns a structured plain-English summary (in JSON format) that explains the cohort, highlights key findings, and lists limitations—all while adhering to the "research-only" mandate.

LangChain is used as the orchestration layer to manage prompt templating, schema injection, and output parsing.

## 10. Dataset
MIMIC-IV Clinical Database Demo v2.2 – a publicly available subset of the MIMIC-IV database.

> MIMIC-IV Clinical Database Demo v2.2 — dataset, documentation, files, licence, and citation: 
https://physionet.org/content/mimic-iv-demo/2.2/
