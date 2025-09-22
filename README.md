# Optimization Project 1 – CVaR Portfolio Analysis

This repository contains the implementation and report for **Project 1: Portfolio Optimization using Conditional Value-at-Risk (CVaR)**.  
The goal is to construct and analyze low-risk stock portfolios using 2019–2020 Nasdaq data, applying linear programming optimization.

---

## Project Overview
- **Problem**: Traditional Value-at-Risk (VaR) has limitations in convexity and subadditivity.  
- **Solution**: We use **Conditional Value-at-Risk (CVaR)** to construct optimal portfolios that minimize downside risk.  
- **Dataset**: Daily returns of 100 Nasdaq stocks from **2019 (training)** and **2020 (testing)**.  
- **Methods**:
  - Optimize portfolio weights to minimize CVaR.  
  - Compare in-sample vs out-of-sample performance.  
  - Evaluate sensitivity to confidence levels (β).  
  - Test conservative approaches and monthly rebalancing.  
  - Discuss portfolio stability.  

---

## Repository Structure
- [project_1.ipynb](project_1.ipynb) — Jupyter Notebook (main analysis & code)  
- [project_1.pdf](project_1.pdf) — Final report (exported from notebook)

- [README.md](README.md) — Project documentation
- [Project Overview (PDF)](project_overview.pdf) — Assignment instructions  
- [stocks2019.csv](stocks2019.csv) — Training data (2019 returns)  
- [stocks2020.csv](stocks2020.csv) — Testing data (2020 returns)  


---

## Task Tracking
| Step                                | What                                                                 | Assigned/Completed by |
| ----------------------------------- | -------------------------------------------------------------------- | --------------------- |
| **Step 1: Data Preparation**        | Load 2019 & 2020 stock data, compute daily returns, exclude NDX      | Melissa               |
| **Step 2: Base CVaR Optimization**  | Implement β=0.95 CVaR minimization with R=0.02% using 2019 data      |                       |
| **Step 3: Out-of-Sample Test**      | Apply 2019 portfolio to 2020 data, compute CVaR, compare with NDX    |                       |
| **Step 4: Sensitivity Analysis**    | Rerun optimization with β=0.90 and β=0.99, analyze allocation shifts |                       |
| **Step 5: Conservative Approach**   | Minimize maximum monthly CVaR (worst-case month) in 2019             |                       |
| **Step 6: Monthly Rebalancing**     | Optimize portfolios monthly in 2020 (rolling window), evaluate risks |                       |
| **Step 7: Stability Constraint**    | Propose/model weight change ≤ 5% month-to-month                      |                       |
| **Step 8: Report Writing**          | Summarize analysis, graphs, recommendations in PDF                   |                       |
| **Final Integration**               | Clean repo, finalize README, push all deliverables                   |                       |
