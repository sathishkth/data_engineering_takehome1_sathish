# Data Engineering Coding Challenge Documentation - Sathish [09-march-2026] for ENBD dubai 

## 1. Overview
This project analyzes NYC job posting data using PySpark running on a Spark cluster deployed using Docker containers.

The goal is to explore the dataset, derive KPIs, perform feature engineering, and generate insights.

---

## 2. Dataset
Dataset used:
nyc-jobs.csv

Source:
NYC Official Jobs Website

The dataset contains information about job postings including:

- Agency
- Job Category
- Salary Range
- Posting Date
- Skills
- Job Description

---

## 3. Data Exploration

Initial exploration was performed to understand:

- Data types
- Null values
- Salary columns
- Categorical columns

Example checks:

- Schema inspection
- Null value count
- Distinct categories

---

## 4. KPIs Implemented

### KPI-1
Number of job postings per category (Top 10)

### KPI-2
Salary distribution per job category

### KPI-3
Correlation between higher degree requirements and salary

### KPI-4
Highest salary job per agency

### KPI-5
Average salary per agency for the last 2 years

---

## 5. Feature Engineering

The following features were created:

1. **Average Salary**
avg_salary = (Salary Range From + Salary Range To) / 2


2. **Posting Year**
Extracted from posting date.

3. **Cleaned Column Names**
Spaces replaced with underscore for processing.

---

## 6. Data Cleaning

The following transformations were applied:

- Convert salary columns to numeric
- Handle missing values
- Clean column names
- Filter recent jobs

---

## 7. Output Dataset

Processed dataset is stored as:/dataset/processed_nyc_jobs_sathishKThangavelu
Format used:Parquet

Reason:

- Faster processing
- Efficient compression
- Columnar storage

---

## 8. Testing

Functions were created for KPIs.

Example test case created using mock dataset to validate function output.

---

## 9. Deployment Approach

If deployed in production:

1. PySpark job packaged as Python script
2. Scheduled using Airflow
3. Data stored in Data Lake
4. Results visualized using BI tools

---

## 10. Challenges

Challenges encountered:

- Salary columns stored as strings
- Column names containing spaces
- Docker Spark cluster configuration

These were resolved using type casting and column renaming.

---

## 11. Learnings

Key learnings from this assignment: Really Good Assignment - 

- Running PySpark on Docker Spark cluster
- Data exploration using Spark
- Feature engineering using PySpark
- Data visualization with matplotlib
