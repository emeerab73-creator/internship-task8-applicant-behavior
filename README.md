# Internship Task 8 – Applicant Behavior Analysis

## Objective
Analyze how applicants interact with Internee.pk's application process to identify drop-off points and improve conversion, as part of the Internee.pk Data Analytics Internship (Task 8).

## What was done
- Simulated applicant behavior data tracking 300 sessions across 5 funnel stages: viewed listing → started application → filled personal info → uploaded resume → submitted application.
- Loaded the data into a **SQLite** database and used real **SQL queries** (`SELECT`, `SUM`, `GROUP BY`) to extract funnel counts, matching the "Google Analytics or SQL" requirement in the guidelines.
- Calculated the percentage drop-off between each stage to identify the biggest bottleneck.
- Segmented the funnel by device type (Mobile vs Desktop) to test whether the bottleneck was device-specific.

## Key finding
The largest drop-off (**31.4%**) occurs between "filled personal info" and "uploaded resume" — the resume upload step. Initially hypothesized this might be a mobile usability issue, but segmenting by device showed **Desktop actually had a higher drop-off (35.7%) than Mobile (28.1%)** at this step — disproving that theory. This suggests the bottleneck is more likely due to applicants being unprepared with a ready resume at the time of applying, rather than a technical or device-specific barrier.

## Tools used
- Python
- SQLite (SQL queries via `sqlite3`)
- Pandas
- Google Colab

## Files
- `applicant_funnel_analysis.csv` — funnel stage counts used for the drop-off analysis

## Result
Identified a clear, evidence-based bottleneck in the application funnel and validated (and corrected) an initial hypothesis using data segmentation — demonstrating the importance of testing assumptions rather than assuming them.
