# Consumer Complaint Intelligence Dashboard

## Purpose

An interactive dashboard for exploring 62,516 consumer complaint records supplied for the AnalystLab Africa Week 4 analysis. It contains four report pages: Executive Complaint Overview, Product and Issue Analysis, Company Response Analysis, and Complaint Timeline Analysis.

## Open and use the dashboard

1. Extract the submission ZIP to a local folder.
2. Open `Consumer_Complaint_Intelligence_Dashboard.html` in a current version of Chrome, Edge, Firefox, or another modern browser. The dashboard runs locally and requires no internet connection.
3. Use the **Year** and **Product** dropdowns in the header to filter KPI cards and visuals across all four pages.
4. Use the report tabs to switch pages. Use browser Print → Save as PDF if a fixed-format copy is needed.

The filters apply to the complaint records in the dashboard. Selecting one product makes its product share 100% within that filtered selection; use **All products** to see each product's contribution to the overall total.

## Dashboard pages

- **Executive Complaint Overview:** total complaints, monthly and annual trends, product distribution, recorded timely-response rate, and average/median forwarding interval.
- **Product and Issue Analysis:** counts by product, sub-product and issue, product-versus-issue view, and leading sub-product/sub-issue pairs.
- **Company Response Analysis:** response-to-consumer categories, valid Yes/No timeliness, in-progress complaints, and public-response categories.
- **Complaint Timeline Analysis:** monthly and annual volume, forwarding-delay distribution, intervals by product, and cases with intervals of at least 30 days.

## KPI conventions

- Complaint volume is a row count; Complaint ID is unique in the supplied extract.
- Periods use **Date submitted**, which the supplied data dictionary defines as the date the CFPB received the complaint.
- Forwarding interval is **Date received − Date submitted**, in calendar days; the dictionary defines Date received as when the CFPB sent the complaint to the company.
- Recorded timely-response percentage = **Yes ÷ (Yes + No)**. Blank/invalid values do not enter the denominator and are reported separately.
- Year-over-year change compares calendar-year counts. 2017 and 2023 are partial years in this extract.

## Submission files

- `Consumer_Complaint_Intelligence_Dashboard.html` — interactive dashboard (standalone HTML).
- `consumer_complaint_kpi_definitions_and_results.docx` — KPI definitions and headline results.
- `consumer_complaint_kpi_detail.csv` — detailed calculated KPI output.
- `Business_Insights_and_Recommendations.md` — evidence-based findings and recommended actions.
- `Data_Quality_Documentation.md` — source, completeness, uniqueness, temporal checks, limitations, and denominator rules.

## Important format note

The interactive dashboard is a standalone HTML deliverable. It is not a Power BI `.pbix` report. The supplied PBIX canvas was blank and could not be safely edited in this session. If the course portal requires a `.pbix` specifically, confirm that format requirement before submission.
