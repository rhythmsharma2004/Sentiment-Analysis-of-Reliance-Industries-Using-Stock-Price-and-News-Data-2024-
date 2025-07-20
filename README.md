# 📈 Sentiment Analysis of Reliance Industries Using Stock Price and News Data (2024)

---

## 🧾 Overview
This project investigates the correlation between news sentiment and stock price behavior of Reliance Industries Ltd. (India’s largest conglomerate). It merges manually curated news sentiment data with official stock prices and conducts a 360° analysis using Python and Power BI.

---

## 🔍 Data Collection
### 1. Stock Price Data  
- **Source:** NSE official website  
- **Duration:** January 1, 2024 – December 31, 2024  
- **Fields:** Date, Open, High, Low, Close, Volume  
- **Format:** `Reliance Stock Price.csv`

### 2. News Data  
- **Source:** MoneyControl, Investing.com, etc. (manually curated)  
- **Fields:** Date, Headline, Link  
- **Saved as:** `Reliance News with Sentiment.xlsx`

---

## 🛠 Methodology

### Part 1: Sentiment Analysis (Python)  
- Processed news headlines to compute a **Sentiment Score** (–1 to +1) and a **Sentiment Category** (Positive, Neutral, Negative).  
- Output used to illustrate daily sentiment.

### Part 2: Data Merging  
- Merged sentiment output with daily stock data by `Date`.  
- Missing dates filled with zero sentiment.  
- Exported to `Merged_Data.csv`.

### Part 3: Visualization (Power BI)  
Loaded `Merged_Data.csv` and built a dashboard with:

1. **News Count by Quarter & Sentiment** (Clustered Column)  
   - Insights: Q1 & Q3 had more positive news.

2. **Close Price vs Sentiment Score** (Dual-Axis Line)  
   - Insights: Price trends positively correlated with sentiment.

3. **Sentiment Category Distribution** (Pie Chart)  
   - Insights: ~80% Neutral, ~16% Positive.

4. **Volume vs Sentiment Score** (Scatter Plot)  
   - Insights: High volume clustered around extreme sentiment.

5. **Close Price vs 7-Day Moving Average**  
   - Using DAX `Moving Avg 7D` measure.  
   - Insights: Smoothed trends validated daily sentiment-price correlation.

---

## 📊 Key Insights
- **Quarterly correlation:** Stock price rises aligned with positive sentiment spikes in Q1 & Q3.  
- **Neutral dominance:** ~75–80% of articles were neutral—market is often sentiment-neutral.  
- **Volatility on negative sentiment:** Negative news quarters triggered higher price volatility.  
- **Volume-sentiment link:** Extreme sentiment often coincided with high trading volumes.  
- **Trend validation:** 7-day moving average confirmed correlation between sentiment and price trend.

---

## 🧩 Files in This Repository
- `Reliance Stock Price.csv` – NSE daily stock data  
- `Reliance News with Sentiment.xlsx` – Raw news data  
- `python/` – Python script(s) for sentiment analysis  
- `Merged_Data.csv` – Combined dataset  
- `PowerBI_Report.pbix` – Power BI dashboard file  
- `report.pdf` – Full project report with details, visuals and discussions

---

## 🏗️ Setup & Reproduction

1. Clone the repository:
   ```bash
   git clone https://github.com/YourUsername/reliance-sentiment-analysis.git
   cd reliance-sentiment-analysis
