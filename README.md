# Recruitment & Workforce MIS Dashboard — Excel

## 📊 Project Overview

The **Recruitment & Workforce MIS Dashboard** is an interactive Excel-based Management Information System designed to monitor and analyze recruitment performance across departments, locations, recruitment sources, job roles, and recruiters.

The objective of this project was to transform raw recruitment transaction data into a **management-ready one-page MIS dashboard** that helps HR and management monitor the recruitment funnel, hiring trends, recruiter performance, recruitment sources, and hiring SLA compliance.

The dashboard was developed in **Microsoft Excel using PivotTables, PivotCharts, slicers, formulas, and dashboard design techniques**.

---

## 🎯 Business Objective

The dashboard is designed to answer key recruitment management questions:

- How many candidates applied?
- How many candidates reached the interview stage?
- How many offers were released?
- How many candidates actually joined?
- What is the overall hiring conversion rate?
- How long does the recruitment process take?
- Which departments are hiring the most?
- Which locations have the highest number of hires?
- Which recruitment sources generate the most hires?
- How is hiring changing month by month?
- How are individual recruiters performing?
- What percentage of hires were completed within the defined hiring SLA?

---

## 🗂️ Dataset

The project uses a prepared recruitment dataset containing **6,000 application records**, stored inside the same Excel workbook as the dashboard.

### Key Fields

| Column | Description |
|---|---|
| Application ID | Unique identifier for each application |
| Candidate ID | Unique candidate identifier |
| Application Date | Date when the candidate applied |
| Candidate Experience | Candidate experience category |
| Education | Highest education qualification |
| Job Role | Role applied for |
| Department | Department associated with the role |
| Location | Hiring location |
| Recruitment Source | Source through which the candidate applied |
| Recruiter | Recruiter responsible for the candidate |
| Hiring Manager | Hiring manager responsible for the position |
| Screening Status | Screening result |
| Interview Status | Interview result |
| Offer Status | Offer status |
| Joining Status | Joining status |
| Final Status | Final recruitment outcome |
| Interview Date | Interview date |
| Offer Date | Offer release date |
| Joining Date | Candidate joining date |
| Days to Hire | Number of days taken to complete hiring |
| SLA Status | Hiring SLA classification |
| Hiring Cost | Recruitment/hiring cost |
| Salary Offered | Offered salary in LPA |

---

## 🛠️ Tools & Technologies

- **Microsoft Excel**
- PivotTables
- PivotCharts
- Excel Slicers
- Excel formulas
- Conditional Formatting
- Excel Tables
- Date Grouping
- Dashboard Design
- MIS Reporting

---

# 🔄 Project Development Process

The project was developed through the following workflow:

```text
Raw Recruitment Data
        ↓
Data Validation & Preparation
        ↓
Business Requirements Identification
        ↓
KPI Definition
        ↓
PivotTable Calculations
        ↓
PivotCharts
        ↓
Slicers & Interactivity
        ↓
Recruiter Performance & SLA Table
        ↓
Dashboard Design & Formatting
        ↓
Final Recruitment & Workforce MIS
```

---

# 1. Dataset Preparation

The recruitment dataset used for this project was a **prepared/cleaned dataset provided for the project**. The dashboard development was performed on this prepared dataset rather than independently cleaning the raw source data.

The prepared dataset was structured with:

- Unique Application IDs
- Consistent recruitment dates
- Logical recruitment status progression
- Calculated `Days to Hire`
- Recruitment funnel stages
- Recruiter, department, location, and source attributes

The recruitment process was structured as:

```text
Application
    ↓
Screening
    ↓
Interview
    ↓
Offer
    ↓
Joining
```

---

# 2. Business Requirements

The dashboard was designed around five major reporting areas.

### Recruitment Volume

- Total Applicants
- Interviews
- Offers Released
- Total Hires

### Recruitment Efficiency

- Average Days to Hire
- Hiring Conversion %

### Recruitment Analysis

- Recruitment Funnel
- Monthly Hiring Trend
- Hires by Department
- Hires by Location
- Hires by Recruitment Source

### Recruiter Performance

- Applications
- Interviews
- Offers
- Hires
- Average Days to Hire
- SLA %

### Interactive Analysis

- Job Role
- Department
- Location
- Recruitment Source
- Recruiter
- Year
- Month
- Quarter
- Application Date

---

# 3. KPI Development

Six major KPIs were created.

## Total Applicants

Measures the total number of applications received.

```text
Total Applicants = Count of Application ID
```

**Result: 6,000**

---

## Interviews

Measures candidates who progressed to the interview stage.

```text
Interviews = Count of Application ID
where Interview Status = Selected
```

**Result: 1,401**

---

## Offers Released

Measures candidates who received an offer.

```text
Offers Released = Count of Application ID
where Offer Status = Offered
```

**Result: 623**

---

## Total Hires

Measures candidates who successfully joined.

```text
Total Hires = Count of Application ID
where Joining Status = Joined
```

**Result: 478**

---

## Average Days to Hire

Measures the average number of days required to complete hiring for candidates who joined.

```text
Avg. Days to Hire = Average of Days to Hire
for candidates where Joining Status = Joined
```

**Result: 34.44 days**

---

## Hiring Conversion %

Measures the percentage of applicants who ultimately joined.

```text
Hiring Conversion %
=
Total Hires / Total Applicants × 100
```

Calculation:

```text
478 / 6000 × 100 = 7.97%
```

**Result: 7.97%**

---

# 4. Recruitment Funnel

A recruitment funnel was created to visualize candidate movement through the hiring process.

```text
Applicants
    ↓
Screened
    ↓
Interviewed
    ↓
Offers
    ↓
Joined
```

The funnel helps management understand how candidate volume changes at each recruitment stage.

The funnel was created using PivotTable-based calculations and displayed as a horizontal bar-style visualization.

---

# 5. Monthly Hiring Trend

A PivotTable was created using:

### Rows
`Joining Date`

### Values
`Count of Application ID`

### Filter
`Joining Status = Joined`

The date field was grouped by:

- Year
- Month

A **Line Chart** was then created to visualize monthly hiring movement.

### Business Question

> How is hiring changing over time?

---

# 6. Hires by Department

A PivotTable was created using:

### Rows
`Department`

### Values
`Count of Application ID`

### Filter
`Joining Status = Joined`

The results were sorted from largest to smallest and displayed using a **horizontal bar chart**.

### Business Question

> Which departments are hiring the most employees?

---

# 7. Hires by Location

A PivotTable was created using:

### Rows
`Location`

### Values
`Count of Application ID`

### Filter
`Joining Status = Joined`

The results were visualized using a horizontal bar chart.

### Business Question

> Which locations have the highest number of hires?

---

# 8. Recruitment Source Performance

Recruitment source effectiveness was analyzed using:

### Rows
`Recruitment Source`

### Values
`Count of Application ID`

### Filter
`Joining Status = Joined`

Recruitment sources include:

- LinkedIn
- Naukri
- Indeed
- Company Career Page
- Employee Referral
- Campus Hiring
- Consultancy
- Walk-in

A bar chart was used to compare actual hires by recruitment source.

### Business Question

> Which recruitment sources are generating actual hires?

---

# 9. Recruiter Performance & SLA

A recruiter-level management table was created to monitor recruitment workload and efficiency.

The final table contains:

| Metric | Purpose |
|---|---|
| Applications | Recruitment workload handled |
| Interviews | Candidates progressed to interview |
| Offers | Candidates receiving offers |
| Hires | Candidates who joined |
| Avg. Days to Hire | Average recruitment turnaround time |
| SLA % | Percentage of hires completed within the defined SLA |

---

# 10. Hiring SLA

A **30-day Hiring SLA** was defined for this MIS project.

### SLA Definition

```text
Days to Hire ≤ 30 Days
        ↓
Within SLA

Days to Hire > 30 Days
        ↓
Breached
```

The SLA percentage is calculated as:

```text
SLA %
=
Candidates Within SLA / Total Hires × 100
```

Example:

```text
Recruiter Hires = 46
Within SLA = 14

SLA %
= 14 / 46 × 100
= 30.43%
```

The 30-day SLA is a **project-defined management benchmark** used for demonstrating recruitment turnaround and SLA compliance analysis.

---

# 11. Recruiter Performance Table

The final dashboard table contains:

| Recruiter | Applications | Interviews | Offers | Hires | Avg. Days to Hire | SLA % |
|---|---:|---:|---:|---:|---:|---:|
| Aarav Sharma | 609 | 147 | 62 | 46 | 34.98 | 30.43% |
| Ankit Mishra | 569 | 113 | 51 | 37 | 34.00 | 43.24% |
| Karan Mehta | 594 | 145 | 57 | 55 | 33.69 | 45.45% |
| Neha Gupta | 624 | 167 | 64 | 51 | 34.94 | 31.37% |
| Pooja Agarwal | 598 | 155 | 62 | 48 | 35.52 | 33.33% |
| Priya Singh | 615 | 128 | 56 | 44 | 34.86 | 43.18% |
| Rahul Verma | 601 | 140 | 68 | 53 | 34.30 | 35.85% |
| Riya Kapoor | 619 | 138 | 69 | 45 | 33.87 | 35.56% |
| Sneha Joshi | 607 | 131 | 64 | 51 | 33.49 | 50.98% |
| Vivek Kumar | 564 | 137 | 60 | 48 | 34.79 | 39.58% |

**Hiring SLA Target: ≤30 Days**

---

# 12. Interactive Slicers

Interactive slicers were added to allow users to filter the dashboard dynamically.

### Slicers

- Job Role
- Year
- Month
- Quarter
- Application Date
- Department
- Location
- Recruitment Source
- Recruiter

These filters allow HR and management users to analyze recruitment performance for specific segments.

---

# 13. Dashboard Design

The dashboard was designed as a **single-page HR Management Information System**.

### Dashboard hierarchy

```text
Header
   ↓
Interactive Filters
   ↓
KPI Cards
   ↓
Recruitment Funnel + Source Performance + Department Analysis
   ↓
Monthly Hiring Trend + Location Analysis + Recruiter Performance
```

### Dashboard Components

#### KPI Cards

1. Total Applicants
2. Interviews
3. Offers Released
4. Total Hires
5. Avg. Days to Hire
6. Hiring Conversion %

#### Visualizations

1. Recruitment Funnel
2. Recruitment Source Performance
3. Hires by Department
4. Monthly Hiring Trend
5. Hires by Location

#### Management Table

**Recruiter Performance & SLA**

---

# 📈 Management Questions Answered

The dashboard can help management monitor:

- Recruitment pipeline volume
- Hiring conversion
- Monthly hiring patterns
- Department-level hiring demand
- Location-level hiring demand
- Recruitment source contribution
- Recruiter workload
- Recruiter hiring output
- Average recruitment turnaround time
- SLA compliance

---

# 🔄 Dashboard Refresh Process

The dashboard was created in **one Excel workbook**. The prepared recruitment data, PivotTables, calculations, PivotCharts, slicers, and final MIS Dashboard are maintained within the same workbook.

When the underlying recruitment data is updated:

```text
Updated Recruitment Data
        ↓
Refresh All
        ↓
PivotTables Update
        ↓
PivotCharts Update
        ↓
Dashboard Updates
```

In Excel:

**Data → Refresh All**

The dashboard slicers and connected PivotCharts can then be used to analyze the refreshed data.

---

# 📁 GitHub Repository Structure

The project uses a single Excel workbook for the complete dashboard implementation.

```text
Recruitment-Workforce-MIS/
│
├── README.md
├── Recruitment_Workforce_MIS.xlsx
│
└── screenshots/
    └── recruitment-workforce-mis-dashboard.png
```

### Excel Workbook

The Excel workbook contains the complete project, including:

- Prepared recruitment dataset
- PivotTables
- KPI calculations
- PivotCharts
- Dashboard
- Interactive slicers
- Recruiter Performance & SLA table
- Supporting calculation sheets

---

# 📌 Project Highlights

- Built a complete **one-page HR MIS dashboard**
- Analyzed **6,000 recruitment application records from a prepared dataset**
- Created **6 management KPIs**
- Created **5 analytical visualizations**
- Built a recruitment funnel
- Developed recruiter-level performance reporting
- Implemented hiring SLA monitoring
- Added interactive Excel slicers
- Used PivotTables for analytical calculations
- Used PivotCharts for visualization
- Designed a management-ready dashboard
- Implemented dynamic dashboard reporting through Excel refresh functionality

---

# 🎓 Skills Demonstrated

### Excel

- PivotTables
- PivotCharts
- Slicers
- Excel Tables
- Excel formulas
- Conditional Formatting
- Working with Prepared Data
- Date Grouping
- KPI Development
- Dashboard Design
- MIS Reporting

### Data Analysis

- Recruitment Funnel Analysis
- Trend Analysis
- Category Analysis
- KPI Analysis
- SLA Analysis
- Operational Reporting
- Management Reporting

### Business Analysis

- Business Requirement Identification
- KPI Definition
- Metric Design
- Management Reporting
- Operational Performance Monitoring
- Exception Monitoring
- Decision-Support Reporting

---

# 👨‍💻 Author

**Shubham Gupta**

B.Tech — Computer Science & Engineering

Aspiring Data Analyst | MIS Analyst | Business Analyst

### Skills

`Microsoft Excel` `Power BI` `SQL` `Python` `Data Analysis` `MIS Reporting` `Dashboard Development`

---

## ⭐ Project Purpose

This project was developed as a portfolio project to demonstrate practical skills in **Excel-based data analysis, MIS reporting, dashboard development, KPI design, PivotTables, PivotCharts, SLA analysis, and business-oriented reporting**.

> **Dataset note:** The recruitment dataset used in this project was prepared/cleaned before the dashboard-building stage. The primary focus of this project is the Excel-based MIS analysis, KPI development, PivotTable/PivotChart reporting, interactive filtering, and dashboard design.
