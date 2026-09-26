# Microfinance Loan Risk Analysis & Power BI Dashboard

## Project Overview
This project analyzes a microfinance bank loan dataset to identify the key
drivers behind loan repayment risk and support data-driven credit policy
decisions. It was built to match the requirements of a Data Analyst role
focused on microfinance data analytics, portfolio risk, and product insights.
The workflow covers the full analyst pipeline: data cleaning, exploratory
data analysis, statistical hypothesis testing, and business intelligence
dashboarding.

## Dataset
The dataset contains 501 individual microfinance loans with details on loan
status, principal amount, term length, disbursement and due dates, past due
days, and borrower demographics (age, gender, education, guarantor status,
application mode).

## Methodology
1. **Data Cleaning** — Handled missing values using domain-aware logic
   (structurally missing `past_due_days` treated as zero, non-recoverable
   `paid_off_time` dropped), verified data integrity (no duplicates).
2. **Exploratory Data Analysis** — Examined loan status distribution,
   Portfolio at Risk (PAR30/PAR60/PAR90), and risk breakdowns across
   guarantor status, gender, education, age group, loan size, and
   application channel.
3. **Statistical Validation** — Used Chi-square tests, independent t-tests,
   one-way ANOVA, and Pearson correlation to confirm which relationships
   were statistically significant rather than coincidental.
4. **Cross-Segment Analysis** — Combined variables (e.g. Guarantor + Gender,
   Guarantor + Loan Size) to uncover compounded risk segments.
5. **Dashboarding** — Translated findings into an interactive Power BI
   dashboard for portfolio monitoring and decision support.

## Key Findings
- **Guarantor presence is the strongest, statistically proven risk driver**
  (Chi-square p < 0.0001; t-test on delay days p < 0.0001).
- Only 33% of loans currently have a guarantor, representing a major risk
  exposure opportunity.
- The **"No Guarantor + Male"** segment has the weakest repayment rate
  (46% PAIDOFF).
- **PAR30 = 20.16%, PAR90 = 0%** — risk is concentrated in short-to-medium
  delays, with no severe long-term defaults.
- Gender and education alone are **not** statistically significant risk
  factors (p > 0.05) once tested rigorously.
- Loans issued on **Sundays** show the highest volume but weaker repayment
  quality than Mondays, suggesting a need for stricter verification during
  high-volume disbursement days.

## Tools & Libraries
Python (pandas, seaborn, matplotlib, scipy), Jupyter/Kaggle Notebook,
Microsoft Power BI

## Repository Structure
