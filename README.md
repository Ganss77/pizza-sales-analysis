Pizza Sales Analysis

A sales analysis of a pizzeria's 2015 performance by Oleh Handzia, using SQLite and Tableau to turn order data into recommendations for the business owner.

Task

The provided dataset consists of four related tables describing orders, order lines, pizza variants, and pizza types. The project examines revenue, demand by month/day/hour, product performance, and basket size to identify opportunities for promotions and menu optimisation.

Data

Period: 1 January–31 December 2015; orders are recorded on 358 days.

Source tables: orders, order_details, pizzas, and pizza_types.

Prepared dataset: sales_lines.csv — 48,620 rows and 12 fields; one row represents an order line, not necessarily one pizza.

Coverage: 21,350 orders, 49,574 pizzas sold, 32 pizza types, and 5 sizes.

Schema and field definitions: docs/data_dictionary.md.

Data Quality and Preparation

Joined the four source tables using their primary/foreign keys and checked key uniqueness and matching relationships.

Checked missing values: the prepared dataset has no empty values across its 12 fields.

Converted price to a numeric type and quantity to an integer; derived month, weekday, and hour from order dates and times.

Used SUM(quantity) for pizza volume: counting rows alone would undercount sales by 954 pizzas.

Used decimal division for average basket size: 2.32 pizzas per order, rather than the integer-truncated result of 2.

Kept the seven days without recorded orders as a limitation; no sales were imputed.

Key Questions and Answers

Queries and original conclusions are available in SQL Lite.txt. The results below use the corrected decimal basket average and peak-to-trough month comparison reported in the presentation.

#

Question

Answer

1

What is the overall sales performance?

$817,860.05 revenue from 21,350 orders and 49,574 pizzas; average order value $38.31 and average basket 2.32 pizzas.

2

How does revenue vary by month?

July leads at $72,557.90; October is lowest at $64,027.60. The peak is approximately 13% above the low.

3

When is demand highest and lowest?

Friday averages 70.8 orders/day, versus 50.5 on Sunday. Lunch and evening are the main peaks; 14:00–16:59 is quieter.

4

Which pizzas lead by revenue and volume?

Thai Chicken generates the most revenue ($43,434.25); Classic Deluxe sells the most pizzas (2,453 units). Brie Carré ranks last on both measures.

5

Which sizes generate the most revenue?

L: 45.9%, M: 30.5%, S: 21.8%; XL and XXL together contribute only 1.8%.

6

Which menu items should be reviewed?

Brie Carré contributes 1.42% of revenue with 490 units sold. The bottom five pizzas together generate 8.8% of revenue.

7

How important are larger orders?

Orders with 4+ pizzas are 18.2% of orders but contribute 39.4% of revenue. Their average ticket is $83.14, versus $28.35 for smaller orders.

8

Where could promotions have the greatest impact?

A hypothetical 10% uplift in afternoon sales adds $18.2K/year; the same uplift on Sunday–Monday adds $20.7K/year. Combined: approximately $38.9K (+4.8%).

Tools

SQLite: data preparation, joins, aggregations, CTEs, window functions, and date/time calculations.

Tableau: interactive visual analysis and dashboard creation.

HTML, CSS, and JavaScript: a 17-slide presentation with charts, SQL queries, an ER diagram, and an embedded dashboard.

Business Recommendations

Test afternoon Happy Hours during 14:00–16:59. This window generates $182.2K annually; a 10% uplift represents approximately $18.2K in additional revenue.

Test family and office bundles on Sunday–Monday. Larger baskets already contribute 39.4% of revenue; a 10% uplift across these days represents approximately $20.7K annually.

Review the menu's long tail, starting with Brie Carré. Its 1.42% revenue share makes it the first candidate for a controlled removal test; review the other four weakest items before changing them.

Promotion estimates are scenarios, not forecasts. Check margins and measure results before rolling out offers.

Limitations and Next Steps

One year of data: year-over-year growth and recurring seasonality cannot be confirmed. Add another year for comparison.

Seven days without recorded orders: closures or missing records are not confirmed. Investigate before interpreting daily averages.

No cost data: the analysis measures revenue, not profitability. Add ingredient and operating costs.

No customer or channel identifiers: repeat purchases and delivery versus dine-in cannot be analysed. Enrich future data collection.

Untested recommendations: run 4–6-week controlled promotion tests and monitor revenue, margin, and basket size; test menu changes separately.

Links

Dashboard: Tableau Public

Presentation: presentation (1).html — download and open in a browser; internet is needed for fonts and Tableau.

PDF report: presentation (1).pdf

Tableau workbook: Pizza date.twbx

SQL queries: SQL Lite.txt

Prepared data: sales_lines.csv

Author: Oleh Handzia — Tableau Public
