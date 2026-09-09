# MedioPharm Medical Center — Healthcare Operations Analytics

## Project Overview

MedioPharm Medical Center is experiencing increasing operational pressure due to the volume and complexity of healthcare activity across patient admissions, doctor visits, and vital-sign monitoring.

Although the organisation collects substantial operational data, there is an opportunity to use this data more effectively to support **performance monitoring, patient-risk analysis, resource planning, and operational decision-making**.

This Power BI project transforms healthcare operational data into an interactive analytics solution that enables stakeholders to monitor patient activity, departmental performance, readmissions, doctor response times, and abnormal vital-sign observations.

The project demonstrates an end-to-end data analytics workflow covering **data preparation, data modelling, DAX, KPI development, interactive visualisation, insight generation, and business recommendations**.

---

# Dashboard Preview

## Hospital Overview

![Executive Overview](Screenshots/Executive_Overview.png)

The Executive Overview provides a high-level view of hospital activity, allowing stakeholders to quickly monitor key operational KPIs, patient trends, departmental performance, readmissions, and abnormal vital-sign activity.

---

## Patient & Department Analysis

![Patient & Department Analysis](Screenshots/Patient_Analysis.png)

This page analyses patient demographics, department activity, admissions, outcomes, and patient flow to identify differences in workload and patient activity across departments.

---

## Vital Signs & Patient Risk

![Vital Signs Analysis](Screenshots/Vital_Signs_Analysis.png)

This page focuses on abnormal vital-sign observations and helps identify patterns in patient monitoring, including repeated abnormal readings.

---

## Doctor & Operational Performance

![Operational Performance](Screenshots/Operational_Performance.png)

This page evaluates operational performance, including doctor response times and departmental activity, to identify potential areas of operational pressure.

---

# Business Objectives

The analysis was designed to answer the following business questions:

* How is patient activity distributed across departments?
* Which departments experience the greatest patient workload?
* How are admissions and discharges changing over time?
* What is the hospital's readmission rate?
* Which departments have higher readmission activity?
* How frequently are abnormal vital-sign readings recorded?
* Which patients have repeated abnormal vital-sign observations?
* How do doctor response times vary across departments?
* What operational patterns could support better resource allocation?

---

# Key Performance Indicators

The dashboard incorporates KPIs including:

* **Total Patients**
* **Total Admissions**
* **Total Discharges**
* **Total Readmissions**
* **Readmission Rate**
* **Average Length of Stay**
* **Abnormal Vital Frequency**
* **Abnormal Vital Rate**
* **Doctor Response Time**
* **Patient Outcomes**

These KPIs provide a consolidated view of hospital operations while allowing users to drill down into departments, patients, doctors, and time periods.

---

# Data Analysis

## Patient Analysis

Patient-level analysis was used to examine:

* Patient demographics
* Age distribution
* Patient activity
* Department utilisation
* Patient outcomes
* Readmission patterns

Patients were segmented into five age groups:

| Age Band       | Age Range |
| -------------- | --------: |
| Children       |      0–17 |
| Young Adults   |     18–34 |
| Adults         |     35–49 |
| Older Adults   |     50–64 |
| Older Patients |       65+ |

This segmentation supports comparison of patient activity and outcomes across different age groups.

---

## Vital Signs Analysis

Vital-sign observations were analysed to identify readings outside the defined analytical thresholds.

| Vital Sign               | Abnormal Reading |
| ------------------------ | ---------------- |
| Heart Rate               | <60 or >100 bpm  |
| Systolic Blood Pressure  | <90 or >140 mmHg |
| Diastolic Blood Pressure | <60 or >90 mmHg  |
| Oxygen Saturation        | <95%             |
| Temperature              | <36°C or >38°C   |

The analysis also considers the **frequency of abnormal observations** to identify patients with repeated abnormal readings.

---

# Data Model

The Power BI solution uses a dimensional modelling approach to separate transactional data from descriptive information.

### Core Tables

* **Admissions** — hospital admission and discharge records
* **Patients** — patient demographic information
* **Doctors** — doctor information and departmental details
* **Vitals** — patient vital-sign observations
* **Calendar** — dedicated date dimension for time-based analysis
* **Measures** — centralised DAX measures

The **Admissions table** functions as the primary operational fact table, with supporting dimension tables providing descriptive context.

The Calendar dimension enables analysis by:

* Date
* Year
* Quarter
* Month
* Week
* Week Number
* Weekday
* Time of Day

The model was designed to ensure that measures respond appropriately to filters such as **department, date, patient, doctor, and demographic group**.

---

# Power BI Development

## Data Preparation

Power Query was used to:

* Inspect source datasets
* Correct data types
* Clean and transform data
* Create derived fields
* Standardise datasets
* Prepare tables for analysis

## Data Modelling

The data model was structured around fact and dimension tables, with relationships established between patient, admission, doctor, vital-sign, and calendar data.

The modelling process focused on creating a reliable analytical structure that supports filtering, aggregation, and cross-dimensional analysis.

## DAX

DAX was used to create analytical measures including:

* Total Patients
* Total Admissions
* Total Discharges
* Total Readmissions
* Readmission Rate
* Average Length of Stay
* Abnormal Vital Frequency
* Abnormal Vital Rate
* Patient Outcome measures
* Time-based analytical measures

Time intelligence was implemented using the dedicated Calendar table to support date and recent-period analysis.

---

# Dashboard Structure

The Power BI report is organised into four key analytical areas.

### 1. Executive Overview

Provides management with a consolidated view of:

* Patient activity
* Admissions and discharges
* Readmissions
* Abnormal vital observations
* Department performance
* Trends over time

### 2. Patient & Department Analysis

Examines:

* Patient volume by department
* Demographic distribution
* Department workload
* Patient outcomes
* Admission patterns

### 3. Vital Signs & Patient Risk

Focuses on:

* Abnormal vital readings
* Vital-sign categories
* Frequency of abnormal observations
* Repeated abnormal readings
* Trends over time

### 4. Doctor & Operational Performance

Analyses:

* Doctor response times
* Patient workload
* Department-level performance
* Operational patterns

---

# Key Insights

The analysis identified several patterns across patient activity, operational performance, and vital-sign monitoring.

### 1. Patient Activity

* **[Insert your finding]** recorded the highest patient activity.
* Patient admissions showed **[insert trend/pattern]** over the reporting period.
* **[Insert department]** experienced the greatest operational workload.

### 2. Readmissions

* The overall readmission rate was **[insert percentage]**.
* **[Insert department]** recorded the highest readmission rate.
* The analysis indicates that readmission patterns vary across departments and should be investigated alongside patient outcomes and length of stay.

### 3. Vital Signs

* **[Insert vital sign]** accounted for the highest number of abnormal observations.
* **[Insert number/percentage]** of observations were classified as abnormal based on the project thresholds.
* **[Insert number]** patients recorded repeated abnormal vital-sign observations.

### 4. Operational Performance

* Average doctor response time was **[insert value]**.
* **[Insert department]** recorded the highest average response time.
* The variation in response times indicates potential differences in departmental workload or operational processes.

> **Important:** Replace the bracketed sections with the actual findings from the completed dashboard. The insights should reflect the data rather than assumptions.

---

# Recommendations

Based on the findings, the following recommendations can be developed.

### 1. Review Department Resource Allocation

Departments experiencing consistently high patient volumes should be reviewed to determine whether staffing and operational resources are appropriately aligned with demand.

### 2. Investigate Readmission Patterns

Departments with higher readmission rates should be investigated further to identify potential relationships between readmissions, patient outcomes, length of stay, and discharge processes.

### 3. Monitor Repeated Abnormal Vital Readings

Patients with repeated abnormal observations should be identifiable through appropriate monitoring processes so that recurring patterns can be investigated by relevant healthcare professionals.

### 4. Review Doctor Response Times

Departments with longer response times should be reviewed to identify potential operational bottlenecks, workload imbalances, or workflow issues.

### 5. Strengthen Time-Based Operational Monitoring

Management should continue monitoring admissions, patient activity, abnormal observations, and departmental workload over time to identify emerging pressure points and support proactive resource planning.

---

# Insights → Recommendations

| Key Finding                                 | Recommended Action                                 |
| ------------------------------------------- | -------------------------------------------------- |
| High patient volume in specific departments | Review staffing and resource allocation            |
| Higher readmission rate in a department     | Investigate readmission and discharge patterns     |
| Frequent abnormal vital readings            | Strengthen monitoring of recurring observations    |
| Longer doctor response times                | Investigate workflow and operational bottlenecks   |
| Peaks in patient activity                   | Use historical trends to support resource planning |

This approach demonstrates how the analysis can move beyond reporting historical performance to support **data-informed operational decision-making**.

---

# Tools & Technologies

| Tool            | Purpose                                            |
| --------------- | -------------------------------------------------- |
| **Power BI**    | Data modelling, analysis and dashboard development |
| **Power Query** | Data cleaning and transformation                   |
| **DAX**         | Measures, KPIs and analytical calculations         |
| **Excel / CSV** | Source data                                        |
| **GitHub**      | Project documentation and portfolio presentation   |

---

# Skills Demonstrated

### Data Analytics

* Data cleaning and transformation
* Exploratory data analysis
* KPI development
* Trend analysis
* Operational performance analysis
* Healthcare analytics
* Insight generation
* Business recommendations

### Power BI

* Data modelling
* Dimensional modelling
* Relationships
* Power Query
* DAX
* Calculated columns
* Measures
* Time intelligence
* Interactive dashboards
* Slicers and filtering
* Drill-down analysis

### Business Analysis

* Translating business problems into analytical questions
* Identifying relevant KPIs
* Analysing operational trends
* Interpreting data patterns
* Communicating insights to non-technical stakeholders
* Translating analytical findings into recommendations

---

# Project Workflow

```text
Raw Healthcare Data
        ↓
Data Cleaning & Transformation
        ↓
Data Modelling
        ↓
DAX Measures & Calculations
        ↓
Exploratory Analysis
        ↓
Dashboard Development
        ↓
Insight Generation
        ↓
Recommendations
```

---

# Repository Structure

```text
MedioPharm-Healthcare-Analytics/
│
├── README.md
│
├── Data/
│   ├── Patients.csv
│   ├── Admissions.csv
│   ├── Doctors.csv
│   └── Vitals.csv
│
├── PowerBI/
│   └── MedioPharm_Healthcare_Analytics.pbix
│
├── Screenshots/
│   ├── Executive_Overview.png
│   ├── Patient_Analysis.png
│   ├── Vital_Signs_Analysis.png
│   └── Operational_Performance.png
│
└── Documentation/
    └── Project_Insights.md
```

---

# Project Outcome

The MedioPharm Medical Center project demonstrates how healthcare operational data can be transformed into an interactive business intelligence solution.

The dashboard enables stakeholders to:

* Monitor hospital activity
* Compare departmental performance
* Track admissions, discharges, and readmissions
* Analyse patient demographics
* Identify abnormal vital-sign patterns
* Monitor operational performance
* Investigate areas of potential operational pressure

The project demonstrates the application of **Power Query, data modelling, DAX, data visualisation, KPI development, and business-focused analysis** to transform raw data into actionable insights.

---

# Disclaimer

This is a **portfolio project using fictional/synthetic healthcare data**. It is intended to demonstrate data analytics and Power BI capabilities and should not be used for real-world clinical decision-making.

This is a **portfolio project using fictional/synthetic healthcare data**. It is intended to demonstrate data analytics and Power BI capabilities and should not be used for real-world clinical decision-making.
