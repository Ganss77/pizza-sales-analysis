# pizza-sales-analysis[README.md](https://github.com/user-attachments/files/33098311/README.md)
# Pizza Sales Analysis

An end-to-end analysis of a pizzeria's 2015 sales using **SQLite** and **Tableau**, with findings presented as a business report for the owner.

The goal is to identify sales patterns, best-selling products, underperforming menu items, and opportunities to grow revenue through targeted promotions.

**[Explore the Tableau dashboard](https://public.tableau.com/shared/HPGKQJQDC)** · **[View the PDF report](presentation%20%281%29.pdf)**

## Tools & Workflow

- **SQLite:** join four related tables, prepare the data, and answer eight analytical questions using aggregations, CTEs, window functions, and date/time calculations.
- **Tableau:** build an interactive dashboard to explore revenue trends, demand patterns, product performance, and order sizes.
- **HTML, CSS & JavaScript:** present the results in a 17-slide report with charts, SQL queries, an ER diagram, and an embedded Tableau dashboard.

The prepared dataset contains **48,620 sales lines** and **12 fields**. Pizza volume is calculated using `SUM(quantity)`, not the number of rows.

## Key Metrics

| Metric | Result |
|---|---:|
| Total revenue | $817,860.05 |
| Total orders | 21,350 |
| Pizzas sold | 49,574 |
| Average order value | $38.31 |
| Average pizzas per order | 2.32 |

## Key Findings

- **Sales are relatively stable throughout the year.** July has the highest revenue ($72.6K) and October the lowest ($64.0K), a gap of approximately 13% relative to October.
- **Demand peaks on Fridays and around lunch and dinner.** Friday averages 70.8 orders per day, compared with 50.5 on Sunday. The 14:00–16:59 window is quieter between the main daily peaks.
- **Large pizzas lead the revenue mix**, contributing 45.9% of total revenue.
- **Group orders have a disproportionate impact.** Orders containing 4+ pizzas represent 18.2% of orders but generate 39.4% of revenue, with an average ticket of $83.14.
- **Brie Carré is the weakest menu item**, with 490 pizzas sold and only 1.42% of total revenue. The five lowest-revenue pizzas together account for 8.8%.

## Business Recommendations

1. **Test afternoon promotions** during 14:00–16:59. A 10% revenue increase in this window would add approximately **$18.2K per year**.
2. **Test family and office bundles on Sunday–Monday.** A 10% revenue increase across these days would add approximately **$20.7K per year**.
3. **Review the menu's long tail**, starting with Brie Carré, and test a smaller menu while monitoring revenue and customer response.

The combined promotional upside is approximately **$38.9K annually (+4.8% of revenue)**. This is a scenario, not a forecast; the offers require testing and margin checks.

## Repository Files

| File | Description |
|---|---|
| [`sales_lines.csv`](sales_lines.csv) | Prepared, joined sales dataset used for analysis. |
| [`SQL Lite.txt`](SQL%20Lite.txt) | SQL queries and analytical conclusions. |
| [`Pizza date.twbx`](Pizza%20date.twbx) | Packaged Tableau workbook. |
| [`presentation (1).html`](presentation%20%281%29.html) | Interactive presentation; download and open in a browser. |
| [`presentation (1).pdf`](presentation%20%281%29.pdf) | PDF version of the 17-slide report. |

To explore the project, start with the **Tableau dashboard** or **PDF report**, then review the SQL and dataset. Open the `.twbx` file in Tableau Desktop or Tableau Public. The HTML presentation needs an internet connection for Google Fonts and the live Tableau dashboard.

## Limitations

The data covers one year, with orders recorded on 358 of 365 days. It does not include ingredient costs, profit margins, customer identifiers, or sales channels. Recommendations therefore focus on revenue and should be validated through controlled tests before implementation.

## Author

**Oleh Handzia** — Data Analytics Student  
[Tableau Public](https://public.tableau.com/app/profile/oleh.handzia) · [GitHub](https://github.com/Ganss77)
