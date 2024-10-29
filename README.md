```markdown
# HR Attendance Dashboard with Power BI

A Power BI dashboard for visualizing HR attendance data, including metrics on employee presence, work-from-home trends, and sick leave rates. This project automates data analysis and visualization, enabling HR managers to track trends, receive alerts, and make data-driven decisions.

---

## Project Overview

The project involves:
- Cleaning and transforming attendance data from multiple Excel sheets
- Calculating key HR metrics using DAX functions
- Designing a dashboard in Power BI to visualize presence trends, work-from-home percentages, and sick leave insights
- Setting up real-time data refresh and automated alerts
- Implementing role-based security to control access levels

---

## Table of Contents

- [Requirements](#requirements)
- [Installation](#installation)
- [Data Preparation](#data-preparation)
- [Usage](#usage)
- [Features](#features)
- [Future Improvements](#future-improvements)

---

## Requirements

- **Power BI Desktop** (for building and designing the dashboard)
- **Power BI Pro** or **Power BI Service** account (for sharing and setting up alerts)
- **Excel** (for data sources)

---

## Installation

1. **Clone the repository**:
   ```bash
   git clone https://github.com/yourusername/HR-Attendance-Dashboard.git
   ```
2. **Install Power BI Desktop**: Download and install Power BI Desktop from [Power BI's official site](https://powerbi.microsoft.com/desktop/).
3. **Open the Project in Power BI**:
   - Open `HR_Attendance_Dashboard.pbit` file in Power BI Desktop.
   - Follow the prompts to load sample data or connect your own data source.

---

## Data Preparation

### Step 1: Load and Transform Data
The Excel sheets contain attendance data for multiple months with different headers. Each sheet includes:
- **Employee Names** (anonymized)
- **Dates** and corresponding **attendance codes** (P = Present, WFH = Work From Home, SL = Sick Leave, etc.)

#### Steps:
1. Import each Excel sheet into Power Query.
2. Clean and format the data:
   - Promote headers and rename columns.
   - Unpivot date columns into a single "Date" column for uniform analysis.
3. Merge all sheets into a single dataset using **Append Queries**.

### Step 2: DAX Calculations for Metrics
In Power BI, use DAX to calculate key HR metrics, such as:
- **Total Working Days**: Counts non-weekend days for attendance.
- **Presence Percentage**: Measures employee presence across the timeframe.
- **Work-From-Home Rate**: Tracks days employees worked from home.

---

## Usage

### Step 1: Design and Customize Dashboard
1. Create key metrics using **DAX formulas** (see `DAX Calculations for Metrics` in Data Preparation).
2. Design the dashboard with visuals:
   - **Line Charts**: Visualize trends over time (presence rate, sick leave rate).
   - **Tables**: Show detailed employee attendance.
   - **Slicers**: Allow users to filter by date, employee, etc.
3. Use conditional formatting for clearer insight.

### Step 2: Automate Data Refresh and Alerts
1. Publish the dashboard to Power BI Service.
2. Set up **scheduled refresh** (e.g., hourly, daily) for real-time updates.
3. Configure **email alerts** for specific thresholds (e.g., alert HR when presence falls below 75%).

### Step 3: Implement Role-Based Security
1. Use **Row-Level Security (RLS)** to restrict data based on roles (e.g., HR Manager, Employee).
2. Define roles within Power BI:
   - “HR Manager” for full access.
   - “Employee” role to view only individual attendance records.
3. Publish the restricted views as needed.

---

## Features

- **Real-Time HR Insights**: Track employee attendance, work-from-home trends, and sick leave patterns.
- **Automated Alerts**: Set thresholds for key metrics to receive email alerts.
- **Role-Based Access**: Limit access based on user roles with RLS.
- **Interactive Filters**: Enable dynamic filtering by date, employee, and work preference.

---

## Future Improvements

- **Enhanced Visualizations**: Add trend comparisons, e.g., between departments.
- **Data Integration**: Connect directly to HR systems or databases for continuous updates.
- **Additional Metrics**: Include metrics like overtime and productivity analysis.
- **Performance Optimization**: Improve DAX formulas for large datasets.

---

