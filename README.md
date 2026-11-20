# Story 4: Data Practitioner Salary & Purchasing Power Analysis

An interactive, self-contained data storytelling presentation evaluating the structural gap between headline nominal salaries, state individual income taxes, and regional cost-of-living adjustments (BEA Regional Price Parities) for graduating data practitioners across 10 major U.S. labor markets.

## Overview

When graduating students compare job offers, ranking opportunities strictly by nominal gross compensation can lead to suboptimal financial decisions. This analysis normalizes federal wage benchmarks against state-level tax schedules and regional price parities to reveal true disposable purchasing power across five core data career trajectories:

* **Business Analyst**
* **Data Analyst**
* **Data Scientist**
* **Data Engineer**
* **Data Architect**

## Story Structure (6-Act Narrative Arc)

1. **Act I — The Nominal Mirage:** Interactive diverging bar charts comparing nominal gross salary against real purchasing power across 10 states, filterable by practitioner role.
2. **Act II — The Specialization Ladder:** Cross-role grouped matrix illustrating which technical specializations outrun high cost-of-living drag.
3. **Act III — The Paycheck Autopsy:** Stacked decomposition waterfall separating real retained value, regional price parity drag, and statutory state income tax.
4. **Act IV — Geographic Variance & Friction Quadrant:** Statistical dispersion spread (Min / Mean / Max) by role alongside a two-variable macro quadrant mapping Regional Price Parity vs. Effective State Tax Rate.
5. **Act V — Reference Methodology & Data Standards:** Documentation of data sources and normalization formulas.
6. **Act VI — The Graduating Practitioner's Decision Playbook:** Actionable rules of thumb for evaluating and negotiating early-career offers.

## Key Analytical Findings

* **The Coastal Nominal Mirage:** While California ($151,040) and New York ($147,200) offer the highest nominal salaries for Data Scientists, high statutory state income taxes (up to 9.3%) and elevated living costs (RPP > 110) reduce real purchasing power to **$121,772** and **$124,426**, respectively.
* **Zero-Income-Tax Leverage:** Washington ($132,987 real) and Texas ($128,789 real) outperform coastal hubs in real disposable income by eliminating state personal income tax drag.
* **Specialization Insulation:** Infrastructure roles (Data Engineer and Data Architect) maintain high compensation floors that absorb regional price drag across all analyzed markets, whereas entry-level analyst roles face severe compression in high-COL states.

## Methodology & Data Sources

| Domain | Authoritative Source | Standard Metric / Classification | Applied Formula |
| :--- | :--- | :--- | :--- |
| **Salary Baselines** | U.S. Bureau of Labor Statistics (BLS) OEWS | SOC 15-2051 (Data Scientists), 15-1251 (Engineers), 13-1111 (Analysts) | $\text{Gross} = \text{National Median} \times \text{State Multiplier}$ |
| **State Taxation** | Tax Foundation / State Revenue Schedules | Effective Individual Income Tax Rates ($100k–$200k bracket) | $\text{Net} = \text{Gross} - (\text{Gross} \times \text{Tax Rate})$ |
| **Cost of Living (COL)** | U.S. Bureau of Economic Analysis (BEA) | Regional Price Parities (RPP) by State (US Baseline = 100.0) | $\text{Real Value} = \left(\frac{\text{Post-Tax Net}}{\text{RPP}}\right) \times 100$ |

## Technical Architecture

* **100% Standalone & Dependency-Free:** Built in pure HTML5, CSS3, and inline SVG graphics with zero external CDN scripts or network calls, ensuring instant rendering across all browsers and LMS environments.
* **Lightweight Interactivity:** Uses a 5-line vanilla JavaScript role switcher (`data-role` attribute filtering) in Act I for instant switching across practitioner tracks.

## Repository Structure

```text
├── how_much_vfinal.html      # Complete standalone presentation with inline SVGs
└── README.md       # Project documentation and methodology
