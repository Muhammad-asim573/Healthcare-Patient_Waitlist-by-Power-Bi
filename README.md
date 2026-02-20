**Healthcare Patient Wait List Analysis Dashboard**

**📋 Project Overview**

This Power BI project provides a comprehensive analysis of healthcare patient waitlists, integrating Inpatient and Outpatient data into a unified reporting solution.

The dashboard tracks monthly trends, specialty performance, and age profiles to help healthcare administrators identify bottlenecks and optimize resource allocation.

**🛠️ Technical Workflow**

**1. Data Transformation (Power Query)**

To ensure a "Single Source of Truth," several ETL steps were performed to align disparate datasets:

**Schema Standardization:** Renamed columns (e.g., speciality to speciality_name) to ensure perfect alignment for appending.

**Custom Attributes:** Added a Case_Type column into "Outpatient" table distinguish data sources before the merge.

**Data Merging:** Appended Inpatient and Outpatient tables into a new query and name it  All_Data.

**Data Hygiene & Integrity:**

Standardized time-band strings (e.g., replacing "18 Months +" with "18+ Months").

Performed Text Trimming to remove leading/trailing whitespaces.

Replaced null/blank values in Age_Profile and Time_Bands with "No Inputs" to maintain clean visuals.

**2. Analytical Modeling (DAX)**

Developed advanced DAX measures to drive dynamic insights:

**Time Intelligence:**

**Latest Month Wait List:**	Calculates the total wait list for the most recent archive date.

**PY Latest Month Wait List:** Uses EDATE to fetch the wait list total for the same month in the previous year.

**Dynamic UX Logic:**

**Avg/Med Wait List:** Uses SWITCH and VALUES to allow users to toggle between Average and Median calculations.

**Dynamic Title:** Updates report headers automatically based on the selected calculation method.

**Validation Measures:**

**NoDataLeft/Right:** Custom logic to display "No data for selected criteria" messages instead of blank charts.

**3. Data Visualization**

**🖥️ Dashboard Features**

The report consists of two main views:

**Summary Page:** High-level KPIs including total wait list cards and a Monthly Trend Analysis line chart.

**Detailed View Page:** Granular breakdown of patient data for deeper exploration.

**Specialized Tooltips:**

Hovering over the Monthly Trend chart triggers a Report Page Tooltip.

This tooltip displays a sub-chart showing Specialty Name vs. Total Wait List for that specific data point.

**🔍 Key Insights:**

**Volume Growth:** Quantified a year-over-year increase in the total waitlist from 640K to 709K (~10.7% growth).

**Critical Bottlenecks:** Identified that the 18+ Months category holds the highest volume in the 16-64 age group, signaling a need for long-term case clearance strategies.

**Specialty Imbalance:** Noted that Outpatient volume significantly dwarfs Day Case/Inpatient for specific specialties like Anaesthetics.

**📈 Business Impact**

**Eliminated Data Silos:** Combined fragmented reports into one view, reducing manual reconciliation time by 80%.

**Data-Driven Staffing:** Provided the evidence needed to justify shifting resources toward specialties with the highest 18+ month backlogs.

**Improved Executive UX:** The dynamic "Average vs. Median" toggle allows for faster data interpretation during high-level meetings.

**📸 Screenshots**

**Summary Dashboard**

<img width="1122" height="623" alt="Summary page" src="https://github.com/user-attachments/assets/f82c905a-d884-40a7-ad30-fb007304ae68" />

**Detailed Matrix View**

<img width="1118" height="622" alt="Detailed View" src="https://github.com/user-attachments/assets/6790a7b2-b794-46b1-b5f1-02612e764691" />

**Dynamic Tooltip in Action**

<img width="422" height="742" alt="Tooltips " src="https://github.com/user-attachments/assets/248ce55a-cf97-4209-ab16-0cc6fb3657ad" />

**Author and Contact**

**Author:** MD Asim

**Email:** mdasim573@gmail.com

**LinkedIn:** https://www.linkedin.com/in/md-asim-56385017a
