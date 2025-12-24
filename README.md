# Health Tracker Report Automation

## 📌 Project Overview
This project focuses on automating the generation of patient-level health tracker reports for a clinical trial environment. Each patient’s clinical data is captured across multiple visits and includes key health metrics such as lipids, body mass index (BMI), HbA1c, weight, Blood Pressure and FPG.

The goal of this solution was to eliminate manual exporting from Power BI, data consolidation and reporting by creating a fully automated, scalable reporting workflow using Power Automate that delivers clear and easy-to-understand health summaries to patients and clinical stakeholders.

## 🔍 Power BI Dashboard Details:
Data Visualizations:
Line charts showing the timeline of patient readings:
1. Lipids (Cholesterol, LDL, HDL)
2. BMI
3. HbA1c
4. Weight
5. Blood Pressure (Systolic/Diastolic)
6. Fasting Plasma Glucose (FPG)

Patient Information Table:
SiteID
PatientID

Dashboard Features:
Dynamic filtering by PatientID to display individual patient’s longitudinal trends. 
Visuals update automatically when filtered by Power Automate flow.

## 🔗 Power Automate Logic Overview
Flow 1: Export Individual Patient Reports

Type: Scheduled Flow (monthly)

Steps:
1. Trigger: Scheduled recurrence.
2. Get Excel rows: Pull PatientID and SiteID from Excel table.
3. Loop (Apply to Each PatientID):
    Filter Power BI dashboard by current PatientID.
4. Export filtered report as PDF using Power BI “Export to File” connector.
5. Save PDF to a folder (file name = PatientID.pdf).

Outcome: Individual PDF for each patient in the folder.

Flow 2: Merge PDFs into a Consolidated Report

Type: Scheduled or Instant Flow

Steps:
1. Get files from folder: List all patient PDFs created in Flow 1.
2. Merge PDFs: Use Encodian connector to combine individual PDFs.
3. Save Consolidated PDF: Save as Consolidated_Health_Tracker.pdf in a folder.

Outcome: Consolidated PDF containing all patient reports.

## Conclusion
Automated the generation of consolidated patient-level PDF health tracker reports using Power Automate by consolidating clinical data across multiple visits.
Reducing manual effort by ~80% and was well received by stakeholders for its efficiency and scalability.

## Thank you!!!
