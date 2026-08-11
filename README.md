# A Comparative Statistical Analysis of Life Expectancy Between Developed and Developing Countries (R)

An academic statistics project (M.Sc. Statistics, Dept. of Statistics, S.V. University) using R to statistically compare life expectancy trends between developed and developing countries, identify key determinants, and forecast future life expectancy.

## Overview

Life expectancy is a key indicator of a nation's health and socio-economic development, yet a persistent gap exists between developed and developing countries. This project uses country-year panel data from 2016–2024 (sourced from WHO, World Bank, and UNDP) to statistically quantify that gap, identify which economic, social, and health factors drive it, and build predictive models to forecast life expectancy 10 years into the future.

## Objectives

- Examine the trend in life expectancy over 2016–2024
- Test whether the difference between developed and developing countries is statistically significant
- Examine relationships between life expectancy and key socio-economic/health indicators
- Predict life expectancy 10 years ahead using multiple regression
- Evaluate model performance using R² and RMSE

## Dataset

Country-year observations covering economic, social, health, and demographic indicators, including:

- **Dependent variable:** Life expectancy (years)
- **Economic:** GDP, total expenditure, percentage expenditure, income composition of resources
- **Social:** Schooling, alcohol consumption
- **Health:** Adult mortality, infant/under-five deaths, immunization rates (Hepatitis B, Polio, Diphtheria, Measles), HIV/AIDS prevalence, BMI, thinness indicators
- **Demographic:** Population, year, country, development status (Developed / Developing)

## Methods (R)

All analysis was performed in R using the following techniques:

- **Trend analysis** — linear regression (`lm`) of life expectancy on year, run overall and separately by development status, plus an interaction model to test whether growth rates differ between groups
- **One-Way ANOVA** — tests for a significant difference in mean life expectancy between developed and developing countries, backed by Welch's t-test, Shapiro-Wilk (normality), and Bartlett's test (homogeneity of variance)
- **Two-Way ANOVA** — tests the combined effects of development status and year, including their interaction
- **Correlation analysis** — Pearson correlation between life expectancy and each socio-economic/health variable, computed separately for developed and developing countries
- **Multiple linear regression** — models life expectancy as a function of year, GDP, population, schooling, BMI, and adult mortality, fit separately by country and by development group, then used to project life expectancy for 2034
- **Model evaluation** — R² and RMSE used to assess model fit and predictive accuracy

R packages used include `ggplot2` (visualization) and `dplyr` (data wrangling).

## Key Findings

- **Trend:** Life expectancy rose significantly in both groups from 2016–2024 (developed: 79.5 → 82.5 years; developing: 68.5 → 71.6 years), but the rate of increase did not differ significantly between groups — the gap persists.
- **ANOVA:** A highly significant difference in mean life expectancy exists between developed (~81.2 years) and developing (~70.1 years) countries (p < 0.001).
- **Correlation:** Life expectancy in developing countries is strongly correlated with mortality rates, healthcare expenditure, education, and nutrition (e.g. infant deaths: −0.845, BMI: 0.661, schooling: 0.408). These relationships are much weaker in developed countries, suggesting a more stable health equilibrium.
- **Regression/Forecast:** The multiple regression model explains far more variance in developing countries (R² = 0.778) than in developed countries (R² = 0.189), and 2034 projections suggest developing nations — including India, Nepal, Nigeria, and Ethiopia — have the greatest potential for life expectancy gains if current health, education, and economic trends continue.

## Conclusion

Life expectancy is closely tied to socio-economic development, and the gap between developed and developing countries — while both groups are improving — remains persistent. The findings point to the need for sustained investment in healthcare, education, and economic development in lower-income countries to close this gap.

## Files

| File | Description |
|---|---|
| Project report (PDF) | Full write-up: introduction, literature review, methodology, R code/output, results, and conclusion |

## Skills demonstrated

- Statistical modeling in R (`lm`, `aov`, `cor`, `t.test`, `shapiro.test`, `bartlett.test`)
- Hypothesis testing (One-Way & Two-Way ANOVA, t-tests)
- Correlation analysis
- Multiple linear regression and predictive forecasting
- Data cleaning and preprocessing in R
- Data visualization with `ggplot2`
- Model evaluation (R², RMSE)

## Author

Roja V, Addepalli Anusha — M.Sc. Statistics, Department of Statistics, S.V. University College of Sciences, Sri Venkateswara University (Supervisor: Prof. B. Sarojamma).
