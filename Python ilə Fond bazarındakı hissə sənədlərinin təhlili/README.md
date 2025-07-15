# Stock Market Price Analysis

This project is about analyzing how the stock prices of some well-known tech companies changed over the past few months.

I used real data from Yahoo Finance for four companies:
- Apple (AAPL)
- Microsoft (MSFT)
- Netflix (NFLX)
- Google (GOOG)

---

##  What I Tried to Understand

While working on this, I focused on these questions:

- How did each stock perform over time?
- Which companies had more stable prices, and which ones were more volatile?
- Do any of them follow similar price patterns?
- Is there any clear connection between the prices of two companies?

---

##  What I Did

- Downloaded 3 months of stock data using the `yfinance` library
- Plotted the daily closing prices for each company to see how they moved
- Calculated **moving averages** (10-day and 20-day) to spot trends
- Measured **volatility** (standard deviation) to see how much prices fluctuate
- Looked at **correlation** between companies, especially Apple and Amazon

---

## Some Observations

- Apple and Google stocks looked more stable compared to Netflix and Microsoft.
- Moving averages helped to smooth out the noise and understand general direction.
- The volatility plot showed that Netflix had the most ups and downs.
- There was a strong correlation between Apple and Amazon — when one goes up, the other often follows.

---

##  Tools and Libraries

I used:
- `pandas` for data manipulation
- `yfinance` to get stock data
- `plotly` for all visualizations (interactive charts)

---

## Files in the Project

- `yfinance.ipynb`: The notebook where I did everything
- `README.md`: This file you are reading


---

##  Example Visuals

I included:
- Line plots showing how prices changed
- Area plots per company
- Volatility lines


---


This project was helpful for me to better understand how stock data works and how to explore it. I focused more on the big picture rather than too many technical details.


