# Volatility Modeling of S&P 500 Excess Returns with AR/MA/GARCH

## Overview
This project performs time-series econometric analysis of S&P 500 **excess returns** and estimates **time-varying volatility** with GARCH. It documents distributional tests, serial dependence diagnostics, mean-dynamics via AR/MA/ARMA, and conditional variance modeling via GARCH(1,1). Outputs include figures and a processed CSV for downstream work.

## Methods
- **Data:** Goyal (2022) monthly dataset (`GoyalData2022.xlsx`):contentReference[oaicite:0]{index=0}
- **Excess returns:** log(S&P 500) minus log risk-free:contentReference[oaicite:1]{index=1}
- **Normality tests:** Jarque–Bera, Lilliefors (reject normality):contentReference[oaicite:2]{index=2}
- **Serial dependence:** Ljung–Box Q tests and ACFs (returns and squared returns):contentReference[oaicite:3]{index=3}
- **Mean dynamics:** AR(1), MA(1), ARMA(1,1) (very low R²):contentReference[oaicite:4]{index=4}
- **Volatility:** GARCH(1,1) with `arch` (clear volatility clustering):contentReference[oaicite:5]{index=5}
- **Outputs:** `processed/base_rep_SP500.csv` with returns and volatility series:contentReference[oaicite:6]{index=6}

## Results (brief)
- Non-normal returns and significant autocorrelation in **squared** returns (volatility clustering):contentReference[oaicite:7]{index=7}  
- AR/MA/ARMA provide **minimal** explanatory power in mean (R² ≈ 0.005–0.006 on AR(1)/MA(1)/ARMA(1,1)):contentReference[oaicite:8]{index=8}  
- GARCH(1,1) conditional volatility tracks major market episodes and aligns with realized 12-month volatility:contentReference[oaicite:9]{index=9}

## Repository Structure (suggested)
