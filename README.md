# 📊 Trader Performance vs Market Sentiment Analysis

## 🎯 Objective
The goal of this project is to analyze how market sentiment (Fear vs Greed) influences trader behavior and performance.  
The analysis focuses on identifying patterns in profitability, trading activity, and risk-taking behavior to derive actionable insights.

---

## 📂 Datasets Used
1. **Bitcoin Market Sentiment Dataset**
   - Contains daily sentiment classification (Fear, Greed, etc.)
   - Link: https://drive.google.com/file/d/1PgQC0tO8XN-wqkNyghWc_-mnrYv_nhSf/view?usp=sharing


2. **Historical Trader Data (Hyperliquid)**
   - Trade-level data including PnL, trade size, direction, and timestamps and more
   - Link: https://drive.google.com/file/d/1IAfLZwu6rJzyWKgBToqwSmmVYU6VbjVs/view?usp=sharing


The datasets used in this project are not included in the repository due to size constraints.  
Please refer to the original dataset links provided in the assignment.

---

## ⚙️ Methodology

### 1. Data Cleaning
- Converted timestamps to datetime format  
- Aligned both datasets on daily level  
- Checked for missing values and duplicates  

### 2. Feature Engineering
- Daily PnL per trader  
- Win rate (based on positive PnL)  
- Average trade size (USD)  
- Trade frequency (number of trades per day)  
- Long ratio  

### 3. Data Integration
- Merged trader data with sentiment data using date  

---

## 📈 Key Insights

- Trader performance is highest during **Fear (~5328)**, followed by **Extreme Greed (~5161)** and **Extreme Fear (~4619)**  
- Performance declines during **Greed (~3318)** and **Neutral (~3438)** phases  
- Traders show **higher activity during Fear periods**, indicating panic-driven behavior  
- **High-risk traders** (larger trade sizes) outperform low-risk traders across all conditions  
- **High-frequency traders** outperform low-frequency traders, especially in volatile markets  
- **Consistent traders (win rate > 60%) significantly outperform others across all sentiment conditions**

---

## 🎯 Strategy Recommendations

### Strategy 1: Fear Market Strategy
- Reduce overtrading and focus on high-conviction trades  
- Maintain moderately larger position sizes to capture volatility opportunities  

### Strategy 2: Greed Market Strategy
- Maintain consistency and controlled risk exposure  
- Focus on trade quality rather than quantity  

---

## ▶️ How to Run

1. Clone the repository:
```bash
git clone <your-repo-link>
```
2. Install dependencies:
```bash
pip install -r requirements.txt
```
3. Run the notebook:
```bash
jupyter notebook Trader_Sentiment_Analysis.ipynb
```

---
## 📌 Notes
- Average trade size is used as a proxy for risk (leverage data not available)

---

## ✅ Conclusion

Trader performance is influenced not only by market sentiment but also by behavioral factors such as trade frequency, risk-taking, and consistency.
While volatile conditions provide more opportunities, disciplined and consistent traders outperform across all market environments.
