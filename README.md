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
.
├── project 1 - cvar - overview.pdf # Assignment overview
├── stocks2019.csv # Training data (returns from 2019)
├── stocks2020.csv # Testing data (returns from 2020)
├── src/ # Source code (to be added)
│ ├── cvar_optimization.py
│ ├── utils.py
├── reports/
│ ├── project1_cvar_analysis.pdf # Final report (to be added)
└── README.md


---

## ⚙️ Setup
1. Clone the repo:
   ```bash
   git clone https://github.com/graccelinn/optimization_project1.git
   cd optimization_project1
