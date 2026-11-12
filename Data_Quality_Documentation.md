# Data Quality Documentation

## 1. Dataset and scope

| Item | Result |
|---|---:|
| Source | `Consumer_Complaints.xlsx` supplied for this analysis |
| Rows / complaints | 62,516 |
| Source columns | 12 |
| Submission date coverage | 2017-05-01 to 2023-08-28 |
| Received date coverage | 2017-05-01 to 2023-08-28 |
| Complete calendar years | 2018–2022 |
| Partial calendar years | 2017 (May–December) and 2023 (January–August) |

The supplied data dictionary was used to interpret the date and response fields. It provides column meanings; it is descriptive reference material rather than a separate instruction set for the analysis.

## 2. Record and identifier checks

- All 62,516 rows contain a Complaint ID.
- All 62,516 Complaint IDs are distinct; no duplicate ID values or extra duplicate-ID rows were found.
- Complaint count is therefore reported as the number of rows, equivalent to the number of unique Complaint IDs for this extract.
- The source has one record per observed complaint for this analysis. No separate narrative/text field is included in the dashboard calculations.

## 3. Missing-value profile

Missing counts below treat empty cells and whitespace-only strings as missing. Other supplied category values are preserved as reported.

| Field | Missing | Share of records | Handling / interpretation |
|---|---:|---:|---|
| Complaint ID | 0 | 0.00% | Identifier present on all rows |
| Submitted via | 0 | 0.00% | Complete in extract |
| Date submitted | 0 | 0.00% | Complete in extract |
| Date received | 0 | 0.00% | Complete in extract |
| State | 0 | 0.00% | Complete in extract |
| Product | 0 | 0.00% | Complete in extract |
| Sub-product | 7 | 0.01% | Retained as blank category in relevant groupings |
| Issue | 0 | 0.00% | Complete in extract |
| Sub-issue | 10,858 | 17.37% | Blanks retained and disclosed; not imputed |
| Company public response | 2,175 | 3.48% | Blank remains distinct from explicit no-public-response category |
| Company response to consumer | 0 | 0.00% | Complete in extract |
| Timely response? | 1,494 | 2.39% | Excluded from valid Yes/No rate denominator and reported separately |

Product and issue fields are populated for all rows, which supports the main product and issue volume views. The sub-issue field has appreciable missingness, so sub-issue rankings and paired details do not represent every complaint.

## 4. Validity and consistency checks

### Timely response

| Value | Count | Treatment |
|---|---:|---|
| Yes | 58,619 | Numerator and denominator |
| No | 2,403 | Denominator |
| Blank / invalid | 1,494 | Excluded from denominator; separately disclosed |
| Valid Yes/No denominator | 61,022 | Yes + No |
| Recorded timely-response rate | 96.06% | 58,619 ÷ 61,022 |

No nonblank unexpected values were observed in the timely-response field; all excluded records are blank. A record-level check found all 1,494 complaints marked **In progress** also have a blank timely-response value in this extract. This describes the supplied snapshot; it does not imply that missing timeliness should be treated as “No.”

### Dates and forwarding interval

- Date fields parse as valid dates for all 62,516 rows.
- Forwarding interval is calculated as **Date received − Date submitted**, in calendar days, using the data dictionary meanings.
- No negative intervals were found; minimum is 0 days, maximum is 275 days.
- Average interval is 1.2249 days and median is 0 days. The difference indicates a right-skewed interval distribution.
- 49,634 complaints (79.39%) have a same-day interval.
- 454 complaints have an interval of at least 30 calendar days. These cases are flagged for review; the threshold is a reporting rule, not a data error definition.

### Category handling

- Empty categorical values are shown as `(blank)` in the underlying calculations and are not silently assigned to another category.
- “Company has responded … and chooses not to provide a public response” is an explicit category, separate from a blank public-response field.
- Company response-to-consumer categories, including **In progress**, are preserved as distinct recorded values.

## 5. Limitations and interpretation

1. The extract is a time-bounded snapshot through 2023-08-28; the full year 2023 is not present. 2017 begins on 2017-05-01. Annual comparisons involving either partial year are not like-for-like comparisons.
2. The dashboard is descriptive. It does not establish why volumes, issues, timeliness, or company response categories changed.
3. A high timely-response percentage reflects only records with a valid Yes/No value. The 1,494 blank records are not counted as timely or untimely.
4. The mean forwarding interval is sensitive to long delays. The median and long-delay counts are shown alongside the mean for context.
5. Missing sub-issue values and blank public-response values are not imputed. Analyses depending on these fields should be interpreted with their missing counts in mind.
6. This deliverable is a standalone interactive HTML dashboard, not a Power BI `.pbix` file.

## 6. Reproducibility summary

The calculations use the supplied workbook fields and one-row-per-complaint count convention. Categories are grouped using their supplied values, with empty fields preserved as blanks. Timely-response rate is computed from valid Yes/No rows only. Forwarding interval is computed from the two parsed date fields, without excluding zero-day intervals.
