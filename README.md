# Candidate Job-Change Intent Analysis

**R&D TalentBridge**

An Excel-based HR analytics project exploring how candidates’ stated job-change intent varies across experience, relevant experience, city development index, and company-size information.

![Dashboard preview](04_Portfolio/Dashboard_Screenshot.png)

## Business Objective

Identify patterns in stated job-change intent that can help HR teams understand candidate groups and guide further investigation.

## Dataset

This project uses the [HR Analytics: Job Change of Data Scientists dataset](https://www.kaggle.com/datasets/arashnic/hr-analytics-job-change-of-data-scientists).

- Original training data: 19,158 records
- Records included in the analysis: 19,093
- 65 records with missing experience were excluded
- `Target = 1` means the candidate stated an intent to change jobs; `Target = 0` means no stated intent

## Key Findings

- **Overall job-change intent rate:** 24.90% (4,754 of 19,093 candidates).
- **Experience:** Intent rate declined from 34.31% for candidates with 0–5 years of experience to 15.31% for candidates with 21+ years.
- **Relevant experience:** Candidates without relevant experience had a 33.84% intent rate, compared with 21.42% for those with relevant experience.
- **City development index:** The intent rate was 57.98% in the 0.60-or-below group and 16.02% in the above-0.85 group. The lower-index group is much smaller, so interpret its rate cautiously.
- **Company size information:** 31.0% of records had company size marked “Not Provided.” Within those records, the intent rate was 40.6%. “Not Provided” means missing information, not a company-size segment.

## Tools and Methods

- Microsoft Excel
- Power Query
- PivotTables and PivotCharts
- Interactive dashboard slicers
- Data-quality checks and a data dictionary

## Project Files

- `01_Source_Data/Raw/aug_train.csv` — source dataset, if included
- `02_Workbook/HR_Candidate_Job_Change_Insights.xlsx` — cleaned data, analysis, and dashboard
- `03_Documentation/Project_Brief.txt` — project overview
- `03_Documentation/Data_Dictionary.xlsx` — field definitions and data-handling notes
- `03_Documentation/KPI_Definitions.txt` — KPI meanings and calculations
- `04_Portfolio/Dashboard_Screenshot.png` — dashboard preview
- `04_Portfolio/Project_Summary.pdf` — project summary

## Limitations

- Stated job-change intent is not actual resignation or attrition.
- The findings describe associations in this dataset; they do not establish cause and effect.
- The 65 excluded records had a 35.4% intent rate (23 of 65); their exclusion may affect interpretation.
- “Not Provided” values indicate missing information and should be interpreted cautiously.
- Findings from this dataset should not be generalized to every candidate or organization.

## Reproducing the Analysis

Download `aug_train.csv` from the Kaggle source above and place it in `01_Source_Data/Raw/`. Open the Excel workbook and refresh its queries and PivotTables. If the project folder has moved, update the Power Query source location first.
