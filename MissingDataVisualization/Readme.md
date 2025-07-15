# Folder structure 
```markdown

MissingDataVisualization/
├── missingdata.ipynb
├── README.md
└── images/
├── line_plot_nan.png
├── seaborn_heatmap.png
├── plotly_heatmap.png
└── missingno_matrix.png
```
#  Missing Data Visualization

This project shows different ways to visualize missing values (NaN) using different Python libraries. Sometimes just checking for `.isnull()` is not enough — it's helpful to actually see where the missing data is.

---

##  What I Wanted to Do

- Create some arrays with `np.nan` values
- Try different visualization tools to see how they show missing data

---

##  Steps and Methods

### 1. Line Plot with NaNs (`matplotlib`)
I created a simple line plot using `matplotlib` with missing values in `x` and `y`. It shows gaps where data is missing.

```python
plt.plot(x, y, marker='o')
```

It helps to understand how missing values break a normal plot.

---

### 2. Heatmap with `seaborn`
I stacked the `x` and `y` arrays using `np.array()` and used a heatmap.

```python
sns.heatmap(data, cmap='viridis', cbar=True)
```

This heatmap highlights the values and the gaps where `NaN` is.

---

### 3. Heatmap with `plotly`
Plotly's version of the heatmap is interactive.

```python
fig = px.imshow(data)
fig.show()
```

Good for exploring data with hover tools.

---

### 4. Missingno Matrix Plot
The `missingno` library is built for missing data visualization. But it works with pandas DataFrames, so I converted the array:

```python
df = pd.DataFrame(data)
mso.matrix(df)
```

It shows exactly where values are missing — especially useful for bigger datasets.

---

## Libraries Used

- `numpy`
- `pandas`
- `matplotlib`
- `seaborn`
- `plotly`
- `missingno`

---


=
```markdown
![Line chart](images/line_nan.png)
```
---

##  Notes

- The data is made up — just for demo.
- This is a quick way to explore how missing data can be shown.
- Good as a small utility or warm-up project.

---

