# stock-market-trading-analysis
Power BI dashboard analyzing stock market trades, net volume, and company-level activity
# 📊 Stock Market Trading Analysis Dashboard

## 🔍 Project Overview
This project analyzes stock market trading activity using Power BI.  
The dashboard highlights trading behavior, net volume impact, and company-level insights.

## 🛠 Tools & Technologies
- Power BI
- DAX
- Power Query
- SQL-style data modeling

## 📈 Key Metrics
- Total Trades
- Total Trade Quantity
- Net Volume (BUY vs SELL impact)

## 📊 Dashboard Features
- KPI cards for high-level metrics
- Net Volume by Company
- Trade behavior analysis
- Interactive filtering

## Key DAX Measures
```DAX
Net Volume =
SUMX(
    share_trade,
    IF(
        share_trade[trade_type] = "BUY",
        -share_trade[volume],
        share_trade[volume]
    )
)
