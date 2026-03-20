# Bank Loan Risk & Performance Analysis | Excel Dashboard
**Microsoft Excel · Data Cleaning · Pivot Tables · Dashboard Design**

---

## Executive Snapshot (3-Minute Read)

**Business Context**
A retail bank's loan portfolio contains 38,600+ loan applications spanning multiple borrower profiles, purposes, and risk grades. Leadership needs visibility into where the loan book is healthy, where defaults are concentrated, and what borrower characteristics correlate with charge-off risk — before exposure compounds.

**5 Numbers That Define This Portfolio**

| Metric | Value | Signal |
|---|---|---|
| Total Loan Applications | 38.6K | Full portfolio scope |
| Bad Loan Rate | 13.82% | 1 in 7 loans charged off |
| Charged-Off Exposure | $65.5M funded → $37.3M received | $28.2M unrecovered |
| Debt Consolidation Share | 18.2K applications | 47% of all loan purposes |
| Avg Interest Rate | 12.05% | Charged-off loans average 13.88% |

**Root Causes Identified**
- Bad loan exposure is concentrated in specific purpose and term segments — not uniformly distributed across the portfolio
- Charged-off loans carry a higher average interest rate (13.88%) than fully paid loans (11.64%) — higher-risk borrowers are being charged more but still defaulting
- 60-month term loans represent a disproportionate default risk relative to 36-month term loans
- Renters (18,439) outnumber mortgage holders (17,198) in the applicant pool — a key risk stratification signal

**Actionable Recommendations**
- Tighten underwriting criteria for debt consolidation loans — 47% portfolio concentration in a single purpose creates structural vulnerability
- Apply stricter DTI thresholds for 60-month term applications — longer tenure correlates with higher default exposure
- Flag high-interest-rate approvals for enhanced monitoring — 13.88% average rate on charged-off loans vs 11.64% on fully paid suggests pricing is not compensating for actual risk
- Prioritise retention of fully paid segment — $411.6M received on $351.4M funded demonstrates strong return profile worth protecting

---

## 📌 Project Overview

This project delivers a risk monitoring and performance analysis dashboard for a retail bank loan portfolio using Microsoft Excel.

The business question: *"Where is the loan portfolio generating returns, where is it absorbing losses, and what borrower and loan characteristics are driving default risk?"*

As the analyst on this project, the focus was on three goals — quantifying good vs bad loan exposure, identifying the purpose and profile segments driving charge-offs, and building an interactive monitoring dashboard for portfolio oversight.

---

## 🛠️ Tools Used

- **Microsoft Excel** — Data cleaning, transformation, Pivot Tables, KPI cards, interactive dashboard

---

## 📊 Executive Summary

### Portfolio Health Overview
- Total funded: **$435.8M** | Total received: **$473.1M** — net positive portfolio performance
- Average interest rate: **12.05%** | Average DTI: **13.33%**
- Month-to-date applications: **4.3K** | MoM growth: **+6.91%**
- Funded amount MoM growth: **+13.04%** — portfolio is actively expanding

Implication: Topline portfolio metrics appear healthy. The risk is concentrated beneath the surface in specific segments.

![Overview Dashboard](assets/overview_dashboard.png)

---

### Good Loan vs Bad Loan Split

| Segment | Applications | Funded | Received |
|---|---|---|---|
| ✅ Good Loan (Fully Paid + Current) | 33.2K (86.18%) | $370.2M | $435.8M |
| 🔴 Bad Loan (Charged Off) | 5.3K (13.82%) | $65.5M | $37.3M |

- Good loans return **$435.8M on $370.2M funded** — a strong positive yield
- Bad loans recover only **$37.3M on $65.5M funded** — $28.2M unrecovered exposure
- The bad loan rate of **13.82%** means 1 in every 7 loans in this portfolio ends in charge-off

![Summary Dashboard](assets/summary_dashboard.png)

---

### Loan Status Breakdown

| Status | Applications | Funded | Received | Avg Interest Rate |
|---|---|---|---|---|
| Fully Paid | 32.1K | $351.4M | $411.6M | 11.64% |
| Current | 1.1K | $18.9M | $24.2M | 15.10% |
| Charged Off | 5.3K | $65.5M | $37.3M | 13.88% |

Critical signal: Charged-off loans carry a **2.24% higher interest rate** than fully paid loans — the bank is pricing for risk but not successfully mitigating it.

---

## 🔍 Insights Deep Dive

### Loan Purpose
- **Nearly half of all loans (47%) are for Debt Consolidation** — 18.2K out of 38.6K applications
- If this segment starts defaulting, it affects almost half the entire portfolio

### Employment Length
- **Borrowers with 10+ years of employment apply the most (8.9K)**
- Borrowers with less than 1 year of employment (4.6K) apply more than those with 2–9 years — an unexpected pattern

### Loan Term
- **Most borrowers prefer shorter loans — 36-month (28.2K) vs 60-month (10.3K)**
- Longer 60-month loans are riskier — more time means more opportunity to default

### Home Ownership
- **Renters (18,439) slightly outnumber homeowners with a mortgage (17,198)**
- Only 2,838 borrowers fully own their home — the most financially stable group is the smallest

### Geographic Distribution
- **Loan applications are heavily concentrated in Texas, California, and mid-Atlantic states**
- Heavy reliance on a few states means a regional economic downturn could hit the portfolio hard

### Monthly Trend
- **Applications nearly doubled from January (2.3K) to December (4.3K)**
- The portfolio is growing fast — which means risk is also growing and needs closer monitoring
---

## ✅ Recommendations

### Short-Term (Risk Monitoring)
- **Watch Debt Consolidation loans closely** — nearly half the portfolio is in one category; problems here affect everything
- **Investigate why high-interest loans are still defaulting** — charged-off loans average 13.88% rate, meaning the bank charged more but still didn't get paid back
- **Keep an eye on Current loans** — at 15.10% average rate, these are the most expensive active loans and the next likely risk

### Medium-Term (Underwriting)
- **Make it harder to get a 60-month loan** — longer loans give borrowers more time to default; approval criteria should be stricter
- **Don't treat all loan purposes the same** — a debt consolidation loan and a home improvement loan carry very different risk levels
- **Factor in whether the borrower rents or owns** — renters and homeowners have different levels of financial stability

### Long-Term (Portfolio Strategy)
- **Avoid relying on one loan type for nearly half the portfolio** — diversify so no single purpose exceeds 35% of total applications
- **Understand which states are carrying the most risk** — heavy concentration in a few states means a local economic shock hits hard
- **Build a simple early warning system** — combining interest rate, DTI, employment length, and loan purpose to catch risky loans before they default
---

## 🧠 Key Analytical Decisions

*The judgement calls that shaped this analysis — not just what was done, but why.*

- **Good vs Bad loan classification over raw status** — Grouped Fully Paid + Current as "Good" and Charged Off as "Bad" to give leadership a binary risk.

- **Amount Received vs Funded as the primary loss metric** — Funded amount overstates loss. The true loss signal is the gap between funded ($65.5M) and received ($37.3M) — a $28.2M unrecovered exposure figure that raw charge-off counts alone would not surface.

- **Interest rate segmented by loan status** — Average interest rate is a portfolio-level vanity metric. Segmenting by Fully Paid, Current, and Charged Off revealed that the bank's risk pricing (13.88% on charge-offs vs 11.64% on fully paid) is not successfully compensating for actual default outcomes.

- **MoM tracked alongside MTD** — Month-to-date figures alone are misleading without directional context. MoM comparisons (+6.91% applications, +13.04% funded) reveal portfolio acceleration — which amplifies both the opportunity and the risk concentration.

- **Employment length retained as a segment despite non-linear pattern** — The 10+ year segment dominating (8.9K) while <1 year (4.6K) outpaces mid-tenure segments is a non-obvious finding. Removing this dimension would have hidden a counterintuitive borrower profile signal worth investigating.

---

## 🔍 Data Quality & Preparation

- 38,600+ rows validated for completeness across key fields
- Loan status values standardised to three canonical categories: Fully Paid, Current, Charged Off
- Monetary fields verified for consistency between funded and received amounts
- Employment length categories standardised for correct sort order in Pivot analysis
- Date fields formatted for monthly aggregation and trend analysis

---

## 📊 Dashboard Pages 

| Page | Purpose |
|---|---|
| Overview | KPI cards, monthly trend, geographic map, purpose and term distribution |
| Summary | Good vs Bad loan split, status-level funded and received breakdown |
| Data | Raw filtered table for drill-down inspection |

---

## ⚠️ Assumptions & Caveats

- Dataset is sourced from Kaggle — figures are indicative and should not be treated as real bank portfolio data
- Good loan classification includes Current loans — these are active and have not yet completed repayment; a subset may eventually charge off
- Loss figures ($28.2M unrecovered) represent the funded-to-received gap on charged-off loans only — does not account for recovery proceedings
- Interest rate and DTI averages are unweighted — large loan amounts in specific segments may skew portfolio-level means

---

## 📬 Contact and Feedback

This project was developed as part of a portfolio demonstrating data analysis and financial dashboard capabilities in Microsoft Excel.

**Data Analyst:** Praveen M
**LinkedIn:** [Profile](https://www.linkedin.com/in/praveen-m-a6b0a1354)
**Email:** praveenm2124@gmail.com

---

*Data Source: Kaggle Bank Loan Dataset | Tools: Microsoft Excel | Records: 38,600+*
