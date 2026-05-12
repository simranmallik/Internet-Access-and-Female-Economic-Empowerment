# Internet-Access-and-Female-Economic-Empowerment
Cross-national nonparametric analysis examining whether national internet usage rates are associated with female employment rates and female management representation across 92 countries (2022). Uses Mann-Whitney U tests with Bonferroni correction. Data from World Bank Gender Data Portal.

# Internet Access & Female Economic Empowerment
### A Cross-National Nonparametric Analysis
**ISyE 6404 — Nonparametric Data Analysis | Georgia Institute of Technology | Spring 2026**

*Simran Mallik, Yuritzy Ramos, Melika Baghi, Keerthana Ramasubramonian*

---

## Overview

This project investigates whether national internet usage rates are associated with two indicators of female economic empowerment across 92 countries in 2022:

1. **Female employment rate** (employment-to-population ratio, 15+)
2. **Female share of senior and middle management positions**

Countries are split into high internet access (≥50%) and low internet access (<50%) groups, and Mann-Whitney U tests are used to compare the two groups on each outcome.

---

## Research Questions

1. Is there a significant difference in the **median female employment rate** between countries with high vs. low national internet usage?
2. Is there a significant difference in the **median female share of middle and senior management** between countries with high vs. low national internet usage?

---

## Data

All data is sourced from the [World Bank Gender Data Portal](https://genderdata.worldbank.org/en/indicators).

| Dataset | Indicator | Role |
|---|---|---|
| Individuals using the Internet (% of population) | Total internet usage rate | Grouping variable |
| Employment to population ratio, 15+, female (%) | Modeled ILO estimate | Outcome variable 1 |
| Female share of employment in senior and middle management (%) | Management representation | Outcome variable 2 |

- **Year:** 2022
- **Final sample:** 92 countries with complete data across all three indicators
- Regional and income-group aggregates removed using ISO 3166-1 alpha-3 country codes

---

## Methods

| Step | Method |
|---|---|
| Normality assessment | Shapiro-Wilk test, Anderson-Darling test, histograms, Q-Q plots |
| Hypothesis testing | Mann-Whitney U test (Wilcoxon rank-sum) |
| Multiple comparisons | Bonferroni correction (α = 0.025 per test) |
| Effect size | Rank-biserial correlation r |

Nonparametric methods were chosen because the Employment–High Internet group significantly violated normality (Anderson-Darling A*² = 2.17, p < 0.001), and cross-national development indicators are broadly known to exhibit skewed distributions.

---

## Key Results

| Test | Median (High Internet) | Median (Low Internet) | p-value | Effect Size | Decision |
|---|---|---|---|---|---|
| Female Employment Rate | 48.18% | 54.07% | 0.0032 | r = 0.23 (small) | Reject H₀ |
| Female Management Share | 35.59% | 24.04% | < 0.0001 | r = 0.43 (medium) | Reject H₀ |

- Low-internet countries had **higher** female employment rates, likely reflecting survival labor in informal and agricultural sectors rather than economic empowerment.
- High-internet countries had **significantly higher** female management representation, suggesting digital connectivity supports women's advancement into leadership roles.

