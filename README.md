
# ClinData Exprorar: AI-Powered Cohort & Data Quality Explorer 

> **Track 2 – AI for Smarter Patient Care Hackathon**

---

## 1. Problem Statement

Hospital data is complex, fragmented, and messy. A single admission spans multiple tables (labs, medications, diagnoses, procedures, transfers, ICU observations). Researchers spend hours writing SQL and manually checking for data errors before they can even begin analysis.

**ClinData Explorer** solves this by providing a **transparent, AI-driven workspace** where researchers can:
- Define cohorts using plain English
- Receive instant data quality audits
- Trace every finding back to its source

All without sacrificing reproducibility or safety.

---

## 2. Proposed Solution

The system allows researchers to ask questions using natural language instead of writing SQL manually. The system then:

1. Interprets the research question
2. Generates human-readable inclusion/exclusion criteria
3. Converts requirements into SQL
4. Executes the query and retrieves records
5. Performs data-quality analysis 
6. Identifies quality flags (missing values, duplicates, unit variations, temporal misalignments)
7. Shows source tables and provenance
8. Provides an explainable AI-generated summary

**Key Principle:** The system is designed to be **transparent, traceable, and research-oriented**.

---

## 3. Target Users

- Clinical-data researchers
- Healthcare data teams
- Clinical research students
- Educators working with structured clinical datasets

**Not intended for clinical decision-making.**

---

## 4. Track Selection

**Track 2 — Cohort & Data Quality Explorer**

The system focuses on:
- Defining cohorts from natural language
- Visible inclusion/exclusion logic
- Data-quality analysis (missingness, duplicates, units, temporal issues)
- Measurement coverage and coding patterns
- Evidence and source-table provenance
- Distinguishing clinical findings from data-quality flags

---

## 5. System Workflow

---

## 4. System Workflow

```text
Natural Language Query
        ↓
Cohort Interpretation
        ↓
Inclusion / Exclusion Logic
        ↓
Text-to-SQL
        ↓
SQL Validation
        ↓
Database Query
        ↓
Retrieved Cohort / Records
        ↓
Relevant Data Quality Analysis
        ↓
Evidence & Provenance
        ↓
Explainable Result
        ↓
AI-Generated Summary
