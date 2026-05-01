# Trader Performance vs Market Sentiment — Write-up

## Methodology

The analysis was conducted to understand how market sentiment influences trader behavior and performance.

1. **Data Cleaning & Preparation**
   - Converted timestamps into a standard datetime format
   - Created a common `date` column for both datasets
   - Checked for missing values and duplicates
   - Standardized column names for consistency

2. **Feature Engineering**
   Trade-level data was aggregated into daily metrics per account using:
   - **Daily PnL**: Total profit/loss per day
   - **Win Rate**: Percentage of profitable trades
   - **Average Trade Size (USD)**: Proxy for risk-taking behavior
   - **Trade Count**: Number of trades per day
   - **Long Ratio**: Proportion of long (BUY) trades

3. **Data Integration**
   - Merged trader metrics with market sentiment data using the `date` column
   - This enabled analysis of trader performance under different sentiment conditions

4. **Segmentation**
   Traders were categorized into groups for deeper analysis:
   - **Risk-based**: High vs Low (based on average trade size)
   - **Frequency-based**: High vs Low (based on trade count)
   - **Consistency-based**: Consistent vs Inconsistent (based on win rate > 60%)

---

## Key Insights

1. **Performance vs Sentiment**
   - Trader performance varies significantly with market sentiment
   - Highest average PnL is observed during **Fear (~5328)**, followed by **Extreme Greed (~5161)** and **Extreme Fear (~4619)**
   - Performance declines during **Greed (~3318)** and **Neutral (~3438)** phases
   - This indicates that **volatile market conditions provide more trading opportunities than stable environments**

2. **Behavioral Patterns**
   - Traders show **higher trading activity during Fear periods**, suggesting panic-driven behavior
   - Average trade sizes are also larger during volatile conditions, indicating increased risk-taking

3. **Risk-Based Segmentation**
   - High-risk traders (larger trade sizes) consistently outperform low-risk traders
   - The performance gap is most significant during volatile market conditions

4. **Frequency-Based Segmentation**
   - High-frequency traders outperform low-frequency traders across all sentiment conditions
   - The gap is especially large during Fear periods, suggesting active trading strategies are more effective in volatile markets

5. **Consistency-Based Segmentation**
   - Consistent traders (win rate > 60%) significantly outperform inconsistent traders across all sentiment conditions
   - Example: During Greed, consistent traders achieve ~9562 PnL compared to ~1354 for inconsistent traders
   - This shows that **discipline and strategy execution are more important than market sentiment alone**

---

## Strategy Recommendations

1. **Fear / Extreme Fear Markets**
   - Reduce overtrading and focus on high-conviction trades
   - Maintain moderately larger position sizes to capture volatility opportunities
   - Avoid panic-driven trading decisions

2. **Greed / Extreme Greed Markets**
   - Maintain discipline and consistency in trading strategy
   - Focus on trade quality rather than quantity
   - Avoid excessive trading despite positive sentiment

3. **General Strategy**
   - Prioritize **consistency (win rate)** over aggressive trading
   - Control trade frequency to avoid overtrading
   - Use **trade size as a controlled risk factor** (leverage data not available)

---

## Conclusion

The analysis demonstrates that trader performance is influenced not only by market sentiment but also by behavioral factors such as risk-taking, trading frequency, and consistency.

While volatile conditions provide more opportunities, **consistent and disciplined traders outperform across all market environments**, highlighting that strategy and execution are more critical than sentiment alone.
