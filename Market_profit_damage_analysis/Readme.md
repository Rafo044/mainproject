
#  Market Profit and Damage Analysis

This project looks at supermarket sales data to understand two main questions:
1. Which product categories have the highest sales?
2. How much profit or loss do we have in each category?

The dataset includes sales, profit, discount, and leftover product amounts for different product categories. I used Python to clean the data and create interactive charts with Plotly.

---

Dataset Overview

The dataset contains information on:

- Product categories
- Sales in the last 3 months
- Discounts applied
- Profit per entry
- Date of sale
- Type and amount of product wastage (e.g., `Wastage`, `Supplier Return`, `No Action`)

| Column Name            | Description                              |
|------------------------|------------------------------------------|
| `Kateqoriyalar`        | Product category                         |
| `Endirim`              | Discount rate                            |
| `Son 3 aylıq satış`    | Sales for the last 3 months              |
| `Mənfəət`              | Profit made from sales                   |
| `Tarix`                | Date of the sale                         |
| `Qalıq məhsul`         | Reason for remaining stock or loss       |
| `Qalıq məhsul miqdarı` | Quantity of unsold or returned products  |


There were some missing values at the end of the file, so I removed them before analysis.

---

## What I Did

1. I cleaned the data:
   - Removed empty rows
   - Fixed the date format
   - Changed sales numbers to numeric

2. I grouped the data by category and found:
   - Average sales
   - Total profit
   - Total remaining product amounts

3. I created charts to visualize everything:
   - Line chart for sales
   - Pie chart for profit by category
   - Bar chart comparing profit and leftover product

---

## Sample Charts

These charts help to see which categories are working well and which have problems.

- **Sales by category (line + bar chart)**
- **Profit by category (pie chart)**
- **Profit vs leftover comparison (grouped bar chart)**




---

## 💻 Tools Used

- Python  
- pandas  
- plotly  
- Excel (for the dataset)

---



 Some Results

    Dairy & Eggs, Meat & Poultry, and Confectionary had higher sales.

    But Heavy Household, Textile, and Light House had more leftover items.

    The company could focus on reducing product waste in those categories.


 ## Files in This Project
 market profit and damage analysis/
│
├── supermarket.xlsx         # raw data
├── analysis.py              # Python code
├── README.md                # this file
└── images/                  # saved plots (optional)
    ├── sales_line_chart.png
    ├── profit_pie_chart.png
    └── damage_comparison_bar.png


This project was first written in Azerbaijani. I translated and explained it in English to share on GitHub. The dataset is made-up (not real) and only used for practice and learning.

Thanks for checking this project!
