# Moving Average on GDP Time Series

This project focuses on visualizing the **Moving Average** over GDP data from 1929 to 1991. 
The idea is to better understand economic growth patterns over time by smoothing short-term fluctuations.

---

## What is Moving Average?

A **moving average** is a statistical technique used to smooth out time series data. 
It does so by averaging a defined number of past values, creating a "rolling" trend line. 
This is commonly used in finance, sales forecasting, and economic indicators like GDP

In simple words: it helps reduce noise and highlights the real direction of the data.

---

## Tools Used

- **Pandas** – for loading and handling time series data 
- **Matplotlib** – for plotting original and smoothed trends 
- **Python datetime** – to parse and handle the date column 

---

## Dataset Info

We use historical U.S. **GDP** data from 1929 to 1991 
The dataset contains two columns:
- `Year`: the year of the GDP record 
- `GDP`: gross domestic product value for that year 

We first parse the date column properly:

```python
df = pd.read_csv("GDPUS.csv", parse_dates=["Year"])
```

---

## Step 1 – Plot the Original Data

We begin by plotting the original GDP data over the years:

```python
plt.plot(df["Year"], df["GDP"], label="GDP per year")
plt.legend()
plt.show()
```

This shows us raw yearly values, but there’s too much fluctuation.

---

## Step 2 – Apply Moving Average

To see the general trend more clearly, we apply a 5-year rolling average:

```python
df["moving_average"] = df["GDP"].rolling(5).mean()
```

Then we plot both the original and the smoothed GDP curves:

```python
plt.plot(df["Year"], df["GDP"], label="GDP per year", color="green")
plt.plot(df["Year"], df["moving_average"], label="5-Year Moving Avg", color="purple")

plt.grid(True)
plt.xlabel("Year")
plt.ylabel("GDP and Moving Average")
plt.legend(loc="upper left")
plt.show()
```

---

## Sample Output

The chart shows the difference between the actual GDP values (which can jump up and down) and the 5-year moving average (which is much smoother).

This makes it easier to:
- detect overall economic trends 
- ignore short-term noise 
- see the general health of the economy over decades 

![Moving avarage](images/movingaverage1.png)
![Moving avarage](images/movingaverag2.png)

---



## Project Structure

```
gdp_moving_average/
│
├── gdp_moving_average.ipynb
├── GDPUS.csv
├── README.md
└── images/
    └── moving_average_gdp.png
```


This project is a simple but powerful example of how moving averages can reveal hidden trends in long-term data like GDP.


