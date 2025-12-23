# Health Tracker Report Automation

## 📌 Project Overview
This project focuses on automating the generation of patient-level health tracker reports for a clinical trial environment. Each patient’s clinical data is captured across multiple visits and includes key health metrics such as lipids, body mass index (BMI), HbA1c, and other vital indicators.

The goal of this solution was to eliminate manual data consolidation and reporting by creating a fully automated, scalable reporting workflow using Power Automate that delivers clear and easy-to-understand health summaries to patients and clinical stakeholders.

## 🔍 Key Insights
1. 🔁 Automated Refresh: Scheduled refresh (daily) to ensure near real-time monitoring
2. 🔗 On-preise dataset: Data connected from shared folder and connected through gateway for scheduled refresh.
3. 🔍 Smart Join Logic: Integrated 12 Excel-based datasets (~30K+ rows) 
4. 🛠 Power Query Transformations: Data cleaning, structuring, and transformation handled entirely in Power Query
5. 📊 User-Focused Visuals: Dashboard includes dynamic tables and clean layouts tailored for clinical teams

## 🔗 Join Logic Overview
1. Query Report → joined with Adverse Event using Subject ID & AE ID
2. Query Report → joined with combined AE-related forms using Subject ID & Related AE ID
3. Final output shows Seriousness (Yes/No) from matching rows
4. If no match, “Not Applicable” is filled using Power Query coalesce() logic

## Conclusion
Automated the generation of consolidated patient-level PDF health tracker reports using Power Automate by consolidating clinical data across multiple visits.
Reducing manual effort by ~80% and was well received by stakeholders for its efficiency and scalability.

## Thank you!!!
