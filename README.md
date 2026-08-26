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

## Limitations
- **Correlation/regression, not causation.** This analysis identifies statistical association (or its absence), not causal mechanisms.
- **Linear methods only.** OLS regression and Pearson correlation both assume a straight-line relationship, which may not capture the true shape   of these relationships.
- **Small sample (n=29).** With 28 states + Delhi, statistical power is limited; a true weak effect may fail to reach significance simply due to   sample size.
- **Cross-sectional, single time-point.** This analysis compares states at one point in time rather than tracking how these relationships evolve over time within a state.
- **Omitted variables.** Social norms, household structure, job availability, and safety cannot be measured with the data sources used here, and   likely matter more than what was tested.
  
## Literature Context
This finding is consistent with existing research on Indian labor economics. The "Indian Paradox" (Chatterjee, Desai & Vanneman, 2018) documents a similar disconnect between rising female education and declining female LFPR at the national level. Separately, the "Feminization U-Hypothesis" (Goldin, 1995) — which proposes a non-linear relationship between income and female LFPR — has also failed to find clean empirical support in Indian state-level data in prior studies. This analysis's findings sit within this broader, well-documented puzzle rather than standing as an isolated result.

## Key references:
- Chatterjee, E., Desai, S., & Vanneman, R. (2018). Indian Paradox: Rising Education, Declining
  Women's Employment. *Demographic Research*, 38, 855.
- Desai, S., & Joshi, O. (2019). The Paradox of Declining Female Work Participation in an Era
  of Economic Growth. *The Indian Journal of Labour Economics*, 62(1), 55-71.
- Goldin, C. (1995). The U-Shaped Female Labor Force Function in Economic Development and
  Economic History. In T.P. Schultz (Ed.), *Investment in Women's Human Capital and Economic
  Development*. University of Chicago Press.
- Gaddis, I., & Klasen, S. (2014). Economic Development, Structural Change, and Women's Labor
  Force Participation: A Re-Examination of the Feminization U Hypothesis. *Journal of
  Population Economics*, 27(3), 639-681.
  
## Files
- `PLFS_ANALYSIS.ipynb` — full analysis notebook
- `PLFS_ANALYSIS.xlsx` — merged dataset (PLFS + RBI, 28 states + Delhi)

## Tools
Python, pandas, numpy, matplotlib, seaborn, statsmodels, scipy
