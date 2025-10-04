# Cross-Market Arbitrage Between NSE and BSE  

This repository contains research, analysis, and code for identifying arbitrage opportunities between the **National Stock Exchange (NSE)** and the **Bombay Stock Exchange (BSE)** using tick-by-tick data.  

The project investigates whether retail traders can capture cross-market spreads using broker APIs (like Zerodha Kite Connect), and compares the feasibility against institutional setups with ultra-low-latency infrastructure.  

---

## 🚀 Project Features  
- **Historical Data Analysis**: Clean and process tick-by-tick market data stored in SQLite.  
- **Arbitrage Detection**: Identify profitable spreads where `(Ask_NSE - Bid_BSE)` or `(Ask_BSE - Bid_NSE)` exceeds transaction cost thresholds.  
- **Backtesting**: Evaluate profitability with filters like minimum spread × quantity > ₹40.  
- **Live Setup (Prototype)**:  
  - Stream live ticks using **Zerodha Kite Connect API**.  
  - Save data in SQLite JSON format with simultaneous read/write.  
  - Run real-time arbitrage detection logic.  
  - (Institutional only) Place simultaneous buy/sell orders across NSE and BSE.  

---

## 📊 Key Findings  
- Profitable arbitrage opportunities do exist, especially in **midcap and IPO stocks**.  
- Execution is challenging for retail traders due to **latency, brokerage costs, and API limits**.  
- Institutions with **colocation and DMA** can capture spreads reliably.  

---
