# Consumer Complaint Business Insights and Recommendations

**Source:** Consumer complaints extract supplied for the dashboard  
**Coverage:** May 2017–August 2023; 62,516 complaint records. Calendar year 2017 is partial at the start of the extract and 2023 is partial at the end. Counts are descriptive and do not, by themselves, establish causes or customer outcomes.

## Evidence-based findings

1. **Complaint volume is concentrated in two product groups.** Checking or savings account complaints total 24,814 (39.7%); credit card or prepaid card complaints total 16,197 (25.9%). Together they account for 41,011 complaints (65.6%).

2. **Account management is the largest reported issue.** “Managing an account” appears on 15,109 records (24.2% of all complaints), making it the leading issue overall. It is also the leading issue within checking or savings account complaints.

3. **The largest complete-year volume was in 2022.** Complaint counts rose from 7,075 in 2019 to 8,942 in 2020, 11,149 in 2021, and 12,953 in 2022. The 2019–2022 increase was 5,878 complaints (83.1%). The 2023 count of 9,131 covers only January–August and should not be compared directly with full-year totals.

4. **Recorded response timeliness is high, but a material number of valid responses were marked No.** Of 61,022 records with a valid Yes or No, 58,619 were Yes (96.1%) and 2,403 were No (3.9%). The other 1,494 records have blank/invalid timeliness values and are excluded from the rate denominator.

5. **Most complaints were closed with an explanation; 1,494 remained in progress.** “Closed with explanation” is the recorded category for 41,044 cases (65.7%); “Closed with monetary relief” for 14,697 (23.5%); and “Closed with non-monetary relief” for 5,273 (8.4%). “In progress” accounts for 1,494 (2.4%). These categories describe recorded company responses and should not be treated as a direct measure of consumer satisfaction.

6. **Forwarding intervals are usually short, with a long-delay tail.** The median interval from Date submitted to Date received is 0 days, and 49,634 records (79.4%) were forwarded on the same calendar day. The average is 1.22 days, higher than the median because 454 cases took at least 30 days; the longest observed interval was 275 days.

7. **The public-response field mostly records an explicit choice not to post publicly.** In 60,311 records (96.5%), the company is recorded as having responded to the consumer and CFPB but choosing not to provide a public response. Another 2,175 (3.5%) have a blank public-response value. These are distinct states and do not mean the company failed to respond privately.

## Actionable recommendations

1. **Prioritize root-cause review for checking/savings account complaints.** Start with “Managing an account,” then break it down by sub-product and sub-issue to identify repeatable process failures. Track monthly counts and share so improvement work targets the largest observed volume.

2. **Create an aged-forwarding exception queue.** Flag cases at 30 days, review the 454 observed cases at or above that threshold, and escalate the oldest first. Track both the median and upper tail (for example, 30+ days) so the mean alone does not obscure unusually long cases.

3. **Audit the 2,403 untimely records and monitor timeliness by product and issue.** Use the 96.1% valid Yes/No result as the baseline, retain the 1,494 blank/invalid records as a separate completeness measure, and avoid treating blanks as “No.”

4. **Manage the 1,494 in-progress cases as an explicit backlog.** Add aging bands and an owner/next-action field to operational review, then check whether the in-progress count and missing timeliness values move together over time. In this extract, a record-level cross-check shows all 1,494 in-progress cases are the same records with blank timeliness values.

5. **Keep private response, public response, timeliness, and resolution outcome as separate reporting dimensions.** In particular, do not interpret the dominant “chooses not to provide a public response” category as a lack of consumer response. Review the small blank public-response group separately for data completeness.

## Measurement notes

- Annual and monthly complaint volume use **Date submitted** (the date the CFPB received the complaint, per the supplied data dictionary).
- Forwarding interval is **Date received minus Date submitted**, in calendar days (Date received is when the CFPB sent the complaint to the company).
- Timely-response percentage is **Yes ÷ (Yes + No)**. Only valid Yes/No values enter the denominator; 1,494 blank values are reported separately.
- Year-over-year comparisons use calendar-year counts. The partial 2017 and 2023 periods limit comparability with full years.
- Findings are descriptive of the supplied extract; they do not establish why complaint volumes or response outcomes changed.
