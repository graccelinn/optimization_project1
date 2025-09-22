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
- [project_1_final.ipynb](project_1_final.ipynb) — Jupyter Notebook (main analysis & code)  
- [project_1_final.pdf](project_1_final.pdf) — Final report (exported from notebook)

- [README.md](README.md) — Project documentation
- [Project Overview (PDF)](project_overview.pdf) — Assignment instructions  
- [stocks2019.csv](stocks2019.csv) — Training data (2019 returns)  
- [stocks2020.csv](stocks2020.csv) — Testing data (2020 returns)  


---

## Task Tracking
| Task                                | What                                                                 | File/Notebook                                                                                                 | Completed by | Date | Validated by | Notes / PR |
| ----------------------------------- | -------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------- | ------------ | ---- | ------------ | ---------- |
| **Task A: Data Preparation**        | Load 2019 & 2020 stock data, compute daily returns, exclude NDX      | <a href="src/utils.py" target="_blank">utils.py</a>                                                           | Grace        |      |              |            |
| **Task B: Base CVaR Optimization**  | Implement β=0.95 CVaR minimization with R=0.02% using 2019 data      | <a href="src/cvar_optimization.py" target="_blank">cvar_optimization.py</a>                                   |              |      |              |            |
| **Task C: Out-of-Sample Test**      | Apply 2019 portfolio to 2020 data, compute CVaR, compare with NDX    | <a href="src/cvar_optimization.py" target="_blank">cvar_optimization.py</a>                                   |              |      |              |            |
| **Task D: Sensitivity Analysis**    | Rerun optimization with β=0.90 and β=0.99, analyze allocation shifts | <a href="src/cvar_optimization.py" target="_blank">cvar_optimization.py</a>                                   |              |      |              |            |
| **Task E: Conservative Approach**   | Minimize maximum monthly CVaR (worst-case month) in 2019             | <a href="src/cvar_optimization.py" target="_blank">cvar_optimization.py</a>                                   |              |      |              |            |
| **Task F: Monthly Rebalancing**     | Optimize portfolios monthly in 2020 (rolling window), evaluate risks | <a href="src/cvar_optimization.py" target="_blank">cvar_optimization.py</a>                                   |              |      |              |            |
| **Task G: Stability Constraint**    | Propose/model weight change ≤ 5% month-to-month                      | <a href="src/cvar_optimization.py" target="_blank">cvar_optimization.py</a>                                   |              |      |              |            |
| **Task H: Report Writing**          | Summarize analysis, graphs, recommendations in PDF                   | <a href="reports/project1_cvar_analysis.pdf" target="_blank">project1_cvar_analysis.pdf</a>                   |              |      |              |            |
| **Final Integration**               | Clean repo, finalize README, push all deliverables                   | <a href="README.md" target="_blank">README.md</a>                                                             |              |      |              |            |
