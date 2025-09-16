# Volatility Modeling of S&P 500 Excess Returns with AR/MA/GARCH

## Overview
This project performs time-series econometric analysis of S&P 500 **excess returns** and estimates **time-varying volatility** with GARCH. It documents distributional tests, serial dependence diagnostics, mean-dynamics via AR/MA/ARMA, and conditional variance modeling via GARCH(1,1). Outputs include figures and a processed CSV for downstream work.

## Methods
- **Data:** Goyal (2022) monthly dataset (`GoyalData2022.xlsx`)
- **Excess returns:** log(S&P 500) minus log risk-free
- **Normality tests:** Jarque–Bera, Lilliefors (reject normality)
- **Serial dependence:** Ljung–Box Q tests and ACFs (returns and squared returns)
- **Mean dynamics:** AR(1), MA(1), ARMA(1,1) (very low R²)
- **Volatility:** GARCH(1,1) with `arch` (clear volatility clustering)
- **Outputs:** `processed/base_rep_SP500.csv` with returns and volatility series

## Results
- Non-normal returns and significant autocorrelation in **squared** returns (volatility clustering)  
- AR/MA/ARMA provide **minimal** explanatory power in mean (R² ≈ 0.005–0.006 on AR(1)/MA(1)/ARMA(1,1))  
- GARCH(1,1) conditional volatility tracks major market episodes and aligns with realized 12-month volatility

## Repository Structure
