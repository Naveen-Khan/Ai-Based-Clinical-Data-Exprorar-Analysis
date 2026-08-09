# AI-Powered Clinical Data Explorer

## 1. Problem Statement

Clinical research data is often stored across multiple structured database
tables, making it difficult for researchers to quickly define patient
cohorts, retrieve relevant records, and determine whether the available data
is reliable enough for a specific analysis.

Researchers may need to understand:

- Which patients satisfy specific research criteria?
- What inclusion and exclusion criteria were applied?
- What SQL query was used to retrieve the data?
- Are important measurements missing?
- Are measurements recorded using different units?
- Are there inconsistent or duplicated records?
- What coding patterns exist in the dataset?
- Which database tables were used to produce a result?
- Are the findings supported by the available data?

Traditional database querying requires technical SQL knowledge and does not
always provide an easy way to understand the quality and provenance of the
retrieved data.

## 1. Project Overview

Clinical datasets are distributed across multiple relational tables,
making it difficult for researchers to define cohorts, query relevant
records, and assess whether the underlying data is suitable for a
specific analysis.

This project provides a conversational interface for exploring
structured clinical data using natural language.

The system supports:

- Natural-language clinical research queries
- Patient cohort definition
- Inclusion and exclusion criteria
- Natural-language-to-SQL conversion
- SQL validation and execution
- Data-quality analysis
- Measurement coverage analysis
- Unit variation analysis
- ICD coding pattern analysis
- Data-quality flags
- Evidence and source-table provenance
- Explainable AI-generated summaries
- Dataset-level insights

---

## 2. Target Users

The system is designed for:

- Clinical-data researchers
- Healthcare data teams
- Clinical research students
- Educators working with structured clinical datasets

It is not intended for clinical decision-making.

---

## 3. Selected Track

**Track 2 — Cohort & Data Quality Explorer**

The system focuses on:

1. Defining cohorts from natural-language requirements.
2. Making inclusion and exclusion logic visible.
3. Querying structured clinical data.
4. Identifying data-quality issues relevant to the requested analysis.
5. Exploring measurement coverage, unit variation, and coding patterns.
6. Providing evidence and source-table provenance.
7. Clearly distinguishing clinical findings from data-quality flags.

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
