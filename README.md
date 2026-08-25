# Testing the Conventional Wisdom: Does Literacy and Income Explain India's Female LFPR Gap?

## Overview
Conventional policy thinking treats female literacy and state prosperity as the primary
levers for closing India's female Labour Force Participation Rate (LFPR) gap — which ranges
from 10.4% to 53.4% across states (PLFS 2025). This analysis tests that assumption directly
against state-level data: do literacy and income actually hold up as strong, statistically
supported explanations for the gap, or does the evidence point elsewhere?

## Data Sources
- **LFPR data:** Periodic Labour Force Survey (PLFS) Annual Report 2025, MoSPI
- **Female Literacy Rate:** PLFS Annual Report 2025, Table 7 (Appendix A)
- **Per Capita NSDP & Sector Shares:** RBI Handbook of Statistics on Indian States,
  Tables 20, 32, 44, 52 (constant prices, base 2011-12, reference year 2022-23)
- **Scope:** 28 states + Delhi (NCT); smaller Union Territories excluded due to
  incomplete RBI economic data (see notebook methodology notes)

## Methods
- Exploratory Data Analysis (univariate, bivariate, multivariate)
- Correlation analysis with significance testing (Pearson's r, p-values)
- Multicollinearity check (VIF)
- OLS regression (statsmodels)

## Key Finding
The data does not support the conventional assumption. Neither female literacy nor
per-capita income shows a statistically significant relationship with female LFPR —
individually, jointly, or across sector composition (R² = 0.055, not significant; F-statistic
p = 0.481). States like Delhi, Goa, and Punjab rank among India's richest yet have some of the
lowest female LFPR, while lower-income states like Sikkim, Himachal Pradesh, and Nagaland rank
highest.

This suggests that the policy levers most commonly assumed to close the gap — education access
and economic growth — are, at minimum, insufficient on their own. Social norms, the type of
work locally available, and household/caregiving structures likely matter more than
conventional wisdom assumes, and warrant further investigation.

## Files
- `Female_LFP
