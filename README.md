# CryptoCurrency Predictor

## Problem Statement

The CryptoCurrency Predictor dashboard provides insights into cryptocurrency market trends, helping traders and investors make informed decisions. It leverages historical data to forecast price movements, assess market volatility, and track portfolio performance. By analyzing key metrics, traders can refine their strategies, mitigate risks, and optimize their investments.

### Steps followed 
Step 1: Loaded historical cryptocurrency data into Power BI Desktop (dataset in CSV format).

Step 2: Opened Power Query Editor and enabled "Column Distribution," "Column Quality," and "Column Profile" options under the View tab.

Step 3: Selected "Column Profiling Based on Entire Dataset" to analyze data consistency and completeness.

Step 4: Identified missing values in price data and handled them appropriately using interpolation.

Step 5: Created calculated columns for key performance indicators (KPIs), including:

7-day moving average price

30-day moving average price

Relative Strength Index (RSI)

Percentage change in price

Step 6: Applied data transformations to normalize trading volume and market capitalization.

Step 7: Designed an interactive dashboard with multiple visual elements:

Line Charts: To display historical price trends and moving averages.

Bar Charts: To compare daily percentage changes across different cryptocurrencies.

Heatmaps: To visualize market volatility and correlation between assets.

Slicers: To filter data by date range, asset type, and market condition.

Step 8: Created a DAX measure to compute predicted price based on past trends:

Predicted Price =
VAR Previous_Close = SELECTEDVALUE(Crypto_Data[Close])
VAR Moving_Avg = AVERAGEX(FILTER(Crypto_Data, Crypto_Data[Date] >= TODAY() - 7), Crypto_Data[Close])
RETURN Previous_Close * (1 + (Moving_Avg - Previous_Close) / Previous_Close)

Step 9: Built a portfolio tracker displaying total investments, profits/losses, and return on investment (ROI).

Step 10: Designed an alert system using conditional formatting to highlight overbought and oversold conditions based on RSI values.

Step 11: Created an insights panel summarizing market trends, top-performing assets, and trading recommendations.

Step 12: Published the report to Power BI Service for real-time monitoring and accessibility.
# Key Insights

Market Trends: Identified bullish and bearish trends across major cryptocurrencies.Highlighted price fluctuations and high-volatility periods.

Predicted Price Movements: Provided short-term price forecasts based on historical trends
Integrated moving average indicators for trend confirmation.

Portfolio Analysis:Displayed investment performance for individual assets.Monitored real-time profit and loss updates.

Risk Assessment:Used RSI and Bollinger Bands to identify overbought and oversold conditions.Highlighted assets with high market risk.

  ### Visual Representations

Price Prediction Line Chart: Forecasts future price movements.

Heatmap: Shows market volatility over time.

Bar Chart: Compares daily price percentage changes.

Portfolio Summary Table: Tracks investment value and ROI.

Condition-Based Alerts: Flags extreme market conditions.
 
 ### Future Enhancements
 
 Integrate real-time cryptocurrency data for dynamic updates.

Implement AI/ML-based predictive models for better accuracy.

Enhance visualization with additional market indicators.

Develop a mobile-friendly version of the dashboard.
 
 ### Conclusion
 
The CryptoCurrency Predictor dashboard provides an interactive, data-driven approach to understanding cryptocurrency market dynamics. By leveraging Power BI’s analytical capabilities, users can make data-backed trading decisions, monitor market trends, and optimize investment strategies.

