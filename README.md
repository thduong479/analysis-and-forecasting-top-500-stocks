# analysis-and-forecasting-top-500-stocks

Using five years of daily prices for the 500 largest U.S. companies, this project evaluates trend and risk, annualized return, 12-month momentum, volatility, and Sharpe ratio, to identify sustained, risk-efficient performers. Simple, interpretable time-series models (ETS) produce next-quarter return forecasts for the most attractive candidates, with outputs including sector rollups and a ranked shortlist to support selection.

## Questions to be explored
1. What are each stock’s annualized return, rolling 12-month momentum, and volatility over the past five years?
2. Which stocks rank highest by Sharpe ratio (return/volatility) over the period?
3. How do average trend and volatility metrics differ across S&P sectors?
4. Which time-series model (ARIMA vs. exponential smoothing) best predicts next-quarter returns for high-Sharpe stocks?
5. Under a 5% overall market downturn, how do our top 50 candidates’ forecast distributions shift?

## Analysis Steps
- **Step 1:** Import data (.csv files) into Jupyter Notebook (via Anaconda)
- **Step 2:** Exploring Data
- **Step 3:** Profiling Data
- **Step 4:** Cleaning Data
- **Step 5:** Data Analysis 

## Insights
- The top 50 stocks ranked by Sharpe ratio exhibit annualized returns averaging ~38% with volatility near 31%, indicating excellent risk-adjusted performance relative to the broader dataset (baseline Sharpe ~0.5).
- The Health Care and Technology sectors are heavily represented among the top performers, including companies like NVO, LLY, SNPS, and NVDA. These firms combine high returns with controlled volatility, indicating sustained growth and resilience over time.
- Using Exponential Smoothing (ETS) models, the median next-quarter forecasted return across the top 50 is ~+4.7%. When adjusted for a 5% market downturn, median forecasts drop but still hover around -0.6%, showing that many high-Sharpe tickers retain strong momentum even under stress conditions.
- Some firms (e.g., NVO, TRI, SNPS) showed relatively low beta exposure in the downturn simulation, making them attractive for stability-oriented allocations.

## Recommendations
- Build a diversified portfolio of the top 10-15 stocks with the highest Sharpe ratios, focusing on those in Health Care and Technology that consistently delivered strong performance.
- Give special weight to stocks with resilient forecasts under downturn scenarios (e.g., NVO, SNPS, TRI), as these can help reduce drawdown risk while preserving upside potential.
- Re-evaluate Sharpe rankings and forecasts quarterly, incorporating updated volatility and return trends, to ensure your high-performing portfolio remains data-driven and responsive to market dynamics.
- Consider complementing ETS forecasts with ARIMA or LSTM models in the future to enhance predictive robustness, especially for more volatile tickers.
