# isharesRegression

This repository contains a group final project for a regression analysis class that models short-term movements in the iShares 20+ Year Treasury Bond ETF (TLT) using lagged macroeconomic indicators and linear regression.

**Overview**
Goal: Predict the 1st–10th trading-day average of TLT each month (TLT_Avg_1_10) from macro indicators. 

Why it matters: Treasury bond ETFs react to inflation, policy rates, and growth expectations. A compact, explainable model helps with tactical bond positioning. 

Data window: Monthly observations, Jan 2022–Dec 2024 (34 rows × 8 columns). 

Features (lagged): CPI, GDP, Unemployment (squared), Fed Funds rate, Consumer Sentiment. 

Preprocessing: Standardized predictors; exploratory histograms, boxplots, and time-series views. 

**Methods**
Baseline linear model using lagged macro variables, then added pairwise interactions. 

Forward/backward stepwise selection (AIC-driven). 

Multicollinearity checked via VIF; assumptions checked via Durbin–Watson, Shapiro–Wilk, and residual plots. 

**Key Results**
Final model fit: Adjusted R² ≈ 0.883; AIC ≈ 30.86 (improved vs. initial model). 

Significant terms (α = 0.05): CPI_lag (−), GDP_lag (−), Unemp² (+), CPI_lag:GDP_lag (+). 

Predictions: January prediction close to observed; February within the 95% CI (but off by ≈ $8). 

Interpretation (high-level): Higher lagged inflation and growth generally align with lower TLT (rate-sensitive asset), while the squared unemployment term captures nonlinearity; the CPI×GDP interaction picks up stagflation-like conditions. 
