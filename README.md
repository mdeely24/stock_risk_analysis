# Stock Returns and Risk Analysis

Analysis of five large-cap stocks (AAPL, MSFT, JPM, XOM, JNJ) against the S&P 500 (SPY), 2019 to present, built in Python with yfinance, pandas, NumPy, and matplotlib.

## What I did
- Pulled adjusted daily prices from 2019 onward with yfinance
- Computed annualized return, volatility, and Sharpe ratio (risk-free rate assumed at 4%)
- Analyzed correlations between the stocks
- Measured maximum drawdowns for each stock, the portfolio, and SPY
- Compared an equal-weight portfolio's growth to SPY
- Ran a 1,000-path Monte Carlo simulation of 1-year portfolio outcomes

## Key findings
- **Riskiest stock:** XOM (volatility 30.8%, max drawdown -60.3%)
- **Best Sharpe ratio:** AAPL (0.96) among single stocks; the equal-weight portfolio is higher at 1.00
- **Portfolio vs SPY:** return 23.5% vs 17.7%, Sharpe 1.00 vs 0.71
- **Max drawdown:** portfolio -35.2% vs SPY -33.7% (average single stock -40.4%)
- **Monte Carlo 1-year range (5th to 95th percentile):** $0.91 to $1.71 per $1 invested (median $1.24)

## Limitations
- **Hindsight bias:** I chose the stocks knowing AAPL and MSFT performed well, so the portfolio's edge over SPY is likely overstated.
- **Monte Carlo assumptions:** it uses historical mean returns from a strong 2019 to 2026 run and assumes normally distributed returns, so it likely overstates the median and understates crashes.
- **Risk-free rate:** a flat 4% was used, though rates were near zero for much of 2019 to 2021.
- **Annualization:** annual return is the daily mean times 252. Compounded growth (CAGR) was 24.1% for the portfolio and 17.1% for SPY, so the two measures differ by about 0.6 points in opposite directions.

## How to run
Open [https://colab.research.google.com/drive/1gSztR9XwVo9E1DIgD4ydolruZGwOFHMa#scrollTo=SFe_KktdCIpT ](https://colab.research.google.com/drive/1gSztR9XwVo9E1DIgD4ydolruZGwOFHMa#scrollTo=SFe_KktdCIpT) in Google Colab and run all cells.

## Author
