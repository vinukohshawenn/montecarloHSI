# Monte Carlo Simulation on the Hang Seng Index (HSI)

##  Project Overview

This project applies a **Monte Carlo simulation** to the **Hang Seng Index (HSI)** to study how uncertainty and volatility influence possible future market outcomes.

The objective is **not price prediction**, but **risk and uncertainty modeling** using a stochastic framework. The project focuses on understanding distributions of outcomes, tail risk, and probabilistic measures such as percentiles and Value at Risk (VaR).

---

##  Objectives

- Apply Monte Carlo simulation to a real-world, volatile market index  
- Model future price evolution using a stochastic process  
- Visualize uncertainty through simulated price paths  
- Quantify downside and upside risk using simple probabilistic metrics  

---

##  Why the Hang Seng Index?

The Hang Seng Index was chosen due to its **structural volatility**, driven by:

- High exposure to Chinese financials, property, and technology sectors  
- Sensitivity to policy decisions, capital flows, and global macroeconomic events  

These characteristics make HSI a suitable candidate for stochastic modeling, where randomness dominates deterministic forecasts.

---

##  Modeling Assumptions

The simulation is based on **Geometric Brownian Motion (GBM)** with the following assumptions:

- Prices evolve according to a stochastic process  
- Log returns are assumed to be normally distributed  
- Volatility is constant over the simulation horizon  
- Drift and volatility are estimated from historical log returns  
- Future price paths are independent realizations of the same process  


##  Methodology

1. Historical HSI data is fetched using `yfinance`  
2. Daily log returns are computed  
3. Drift (μ) and volatility (σ) are estimated from historical returns  
4. **10,000 Monte Carlo price paths** are simulated over a one-year horizon (≈252 trading days)  
5. Simulated paths and final price distributions are analyzed  

---

##  Outputs & Analysis

The project generates:

###  Simulated Price Paths
- Each path represents a possible future scenario  
- Paths diverge over time, illustrating how uncertainty compounds  

###  Distribution of Final Prices
From the final simulated values, the following metrics are computed:

- Expected final value  
- Probability of loss relative to the current index level  
- 5th and 95th percentiles (confidence bounds)  
- 95% Value at Risk (VaR)  

These metrics provide insight into **risk and tail behavior**, rather than point forecasts.

---

## Key Insights

- Volatility plays a larger role than drift in determining future outcomes  
- Downside risk is meaningful even when average returns appear modest  
- Large upside scenarios exist but occur with low probability  
- Risk is better captured through distributions and percentiles than averages  

---

##  Key Takeaway

> Monte Carlo simulation does not predict where the market will go — it quantifies **how uncertain the future is and how extreme outcomes can be**.

For volatile indices like HSI, this probabilistic perspective is more informative than deterministic forecasts.

---

## 🛠️ Tools & Libraries

- Python  
- NumPy  
- Pandas  
- Matplotlib  
- yfinance  

---

## 📎 vinukohshawenn

[Vinay]  
