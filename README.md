# Elist-Ecommence Analysis
<img width="1203" alt="Screenshot 2024-10-22 at 5 00 54 PM" src="https://github.com/user-attachments/assets/342c7d74-230a-4574-9748-0fae89ec77fc">

Analyzing Elist from 2019-2022. An interactive Tableau dashboard's link is [here](https://public.tableau.com/app/profile/libang.xia/viz/ElistE-CommerceOverview/Dashboard1).

# Project Summary

# Table of Contents
<a id='table_of_contents'></a><br>
[Project Summary](#section_1)<br>
[Part 1: Trends (Excel)](#section_2)<br>
[Part 2: Targeted Insights (SQL)](#section_3)<br>
[Part 3: Visualizations (Tableau)](#section_4)<br>
[Part 4: Recommendations & Next Steps](#section_5)<br>


<a id='section_1'></a>
# Project Summary
Elist Electronics, established in 2018, is a global e-commerce company that sells popular electronic products worldwide via its website and mobile app.

The company has significant amounts of data on its sales, marketing efforts, operational efficiency, and loyalty program that has been previously underutilized.
Hence, I analyze those data to investigate the trend and sales growth by starting with the analysis of the key metrics such as 
Sales, order, revenue, Average order value( AOV), Year of growth year (YoY), Market Channel, Product Popularity, Refund Rate, Efficiency Shipping. Also how to 
improve the loyalty program  to assess its effectiveness in overall sales, AOV, and total orders.


This project thoroughly analyzes and synthesizes this data in order to uncover critical insights that will improve Elist's commercial success.
Insights and recommendations are provided on the following key areas:

In this project, I analyzed a dataset to investigate trends and growth rates in revenue, average order value (AOV), product popularity, marketing channels, refund rates, and shipping efficiency. Additionally, I closely examined their recently launched loyalty program to assess its effectiveness in overall sales, AOV, and total orders.

This project consists of four parts:
- <b>Part 1: Trends</b>
  * Using Excel, I spend a limited time taking a quick look at some of the broad trends within the data to see what notable insights can be pulled  for the finance and product team. and determine which section need using more time and more complicated the tool like python and sql
  * 
- <b>Part 2: Targeted Insights</b>

  * With the aid of SQL, I capture more detail and more insight for my team include finance an marketing  I pull out more targeted insights for the finance and marketing team, highlighting things like MacBook sales, refund rates, and best performing marketing channels.

- <b>Part 3: Visualizations</b>
  * Leveraging Tableau, I create a interactive dashboard for the finance and product teams (as well as the sales and operations teams to a lesser extent) to monitor metrics of interest on an ongoing basis.

- <b>Part 4: Recommendations & Next Steps</b>
  * Suggestions on things to take a look at going forward, report to the senior, and recommend more insight to my senior manager.


# Data Structure & Initial Checks
Here is the Entity Relationship Diagram:
The data are four tables and consists of information on orders, order statuses, customers, and geographic information.


<img width="750" alt="Entity Relationship Diagram showing orders, order statuses, customers, and geographic information tables" src="https://imgur.com/L3Fh37t.png">

You can view the data in greater detail [here](https://github.com/sean-atkinson/elist_ecommerce_analysis/tree/main/data).
<a id='section_2'></a>


 # Part 1: Exploratory Data Analysis (Excel)
[(Back to table of contents)](#table_of_contents)<br><br>
<b>Summary of Trends</b>:

**Sales Trend Analysis**:
   - Created a pivot table to show sales trends monthly.
   - Analyzed **Year-over-Year (YoY)** and **Month-over-Month (MoM)** growth rates.
   - Visualized trends using line charts to display revenue fluctuations over time.

<b>Yearly</b>
- **Sales Surge in 2020**: Sales peaked in 2020, likely due to increased demand driven by the pandemic, which significantly impacted customer shopping behavior.
- **December 2020 High**: December 2020 recorded the highest monthly revenue, reaching $8.63 million, with an average order value of 298, highlighting the impact of pandemic-related demand shifts on customer spending.
- **Sustained Decline in 2021**: Orders continued to decline YoY for seven consecutive months in 2021. Revenue hit a historic low in November 2022, with the company generating just over $78K. While revenue slightly recovered in subsequent months, it followed typical holiday season patterns rather than indicating a robust recovery.
-**Sharp Decline in 2022**:
Order Volume: Total orders in 2022 were down to 18,964, a 40% decrease.
Revenue: Year-over-year revenue dropped by 44% in 2022.
Industry-Wide Downturn: The challenging sales figures in 2022 align with broader trends in the e-commerce industry. According to Statista, factors such as an economic downturn, market saturation, reduced marketing effectiveness, and supply chain disruptions contributed to an unprecedented contraction in e-commerce revenue forecasts for 2022.

<b>Seasonality</b>
- Sempter and october tend to perform excellent, most likely duo the Back to School season, student demand increasing.
- Winter and spring tend to perform better, most likely due to holiday sales and special promotions.
- There's a noticeable sales uptick in the first half of 2020, most likely due to the pandemic.

<b>Products</b>
- Airpods and 4K gaming monitor have consistently been our best-selling product in terms of total orders. 
- In 2022, Airpods and a gaming monitor made up around 70% of all orders.
- Bose Soundsport Headphones have consistently performed poorly. We've only sold 25 pairs over 3 years.

<b>Loyalty Program</b>
- We recommend continuing to expand this. When the program started in 2019, members were spending an average of $29 less than non-members. In 2022, loyalty program members now spend an average of $34 more and 9 percent total order more  than non-members per purchase.
- By the end of 2022, loyalty program members generated 27% more revenue 10% more orders than non-members. This is largely attributed to their higher receptiveness to our marketing efforts. The fact that they are loyalty members makes them more open to receiving emails from us, as demonstrated by spending 217% more than non-members through that channel in 2022. via direct method 10% more than non-members through that channel in 2022. via social method 20% more than non-members through that channel in 2022. 


<b>Technical Analysis:</b><br>
For this section, I used Pivot Tables, lookup function, conditional formatting, aggregation functions, and statistical analysis to clean, analyze, and summarize my insights for the finance and product teams.

Here is an example of the pivot table used for seasonality insights:

<img width="750" alt="Excel pivot table showing totals and growth rates for monthly sales, AOV, and orders" src="https://imgur.com/Uns8sPD.png">


# Part 2: Targeted Insights (SQL)
[(Back to table of contents)](#table_of_contents)<br><br>
<b>Summary of Targeted Insights</b>:

<b>North American MacBook sales (all year)</b>
- Average of 30 units sold per month.
- Average monthly sales are $47.8K.

<b>Refund rates</b>
- For 2020, the monthly refund rate was 3.1%.
- In 2021, the lowest amount of returns for Apple products was 6 (in November). The highest was 33 (in March).
- Across all years, Macbook Airs had the highest refund rate at 4.2% followed by ThinkPads (3.8%) and iPhones (3.5%).

<b>Account creation methods (Jan-Feb 2022)</b>
- Accounts created on tablets had the highest average order value at $287 (but only 25 purchases were made on tablets).
- Desktop was the account creation method that led to the most new customers, with 2,487, which is more than three times the number of new customers generated by the next closest method, mobile, with 701.

<b>Time to purchase (all years)</b>
- Average of 51 days between account creation and first purchase.

<b>Marketing channels (all years)</b>
- Direct - highest number of orders.
- Emails - second highest number of orders.

<b>Technical Analysis:</b><br>
For this analysis, I used SQL and BigQuery. In regards to SQL, I used aggregation functions, window functions, joins, filtering, CASE expressions, common table expressions (CTEs), and in a couple instances the QUALIFY clause to use row_number() to filter results.

You can find my SQL queries [here](https://github.com/sean-atkinson/elist_ecommerce_analysis/blob/main/sql/elist_sales_trends_queries.sql).

Here is an example of a query result that uses the aforementioned qualify clause:
```sql
-- Creating a brand category and totaling the amount of refunds per month
-- Filtering to the year 2020
WITH highest_num_refunds_cte AS (
    SELECT
        CASE
            WHEN LOWER(orders.product_name) LIKE '%apple%' OR LOWER(orders.product_name) LIKE '%macbook%' THEN 'Apple'
            WHEN LOWER(orders.product_name) LIKE '%samsung%' THEN 'Samsung'
            WHEN LOWER(orders.product_name) LIKE '%thinkpad%' THEN 'ThinkPad'
            WHEN LOWER(orders.product_name) LIKE '%bose%' THEN 'Bose'
            ELSE 'Unknown'
        END AS brand,
        DATE_TRUNC(order_status.refund_ts, MONTH) AS month,
        COUNT(order_status.refund_ts) AS num_refunds
    FROM 
        elist.orders AS orders 
    JOIN 
        elist.order_status AS order_status 
    ON 
        orders.id = order_status.order_id
    WHERE 
        EXTRACT(YEAR FROM order_status.refund_ts) = 2020
    GROUP BY 
        1, 2
)
-- Getting the highest month and corresponding number of refunds for each brand in 2020 
SELECT
    brand, 
    month, 
    num_refunds
FROM 
    highest_num_refunds_cte
QUALIFY 
    ROW_NUMBER() OVER (PARTITION BY brand ORDER BY num_refunds DESC) = 1
ORDER BY 
    1;
```
And here is its result:
| brand    | month      |   num_refunds |
|:---------|:-----------|--------------:|
| Apple    | 2020-06-01 |            56 |
| Samsung  | 2020-04-01 |             7 |
| ThinkPad | 2020-04-01 |             9 |
| Unknown  | 2020-05-01 |            25 |



<a id='section_4'></a>



# Part 3: Visualizations (Tableau)

[(Back to table of contents)](#table_of_contents)<br><br>

<b>Summary of Insights:</b>

<b>Orders</b>
- Airpods, Gaming monitors, and Macbook Air have accounted for over 80% of all orders from 2019-2022.
- Every product except webcams, and charging caple packs saw its total orders peak around the start of the pandemic. Paradoxically, total orders for webcams rose in the following years. This is something we should investigate further.

<b>Sales by Region</b>
- top 3 region are the unite state , Canada, and Great British, we can see that Elish Ecommerce focus on americam
-  we have more change to explore the Asia and Africa region
-  intesrting thing the top 3 aov country are not amrican state coutyr which are AO,PG,YE
-  • North America grew in importance in 2022, increasing revenue share to 55% and order share to 53% among known region sales.
• Sales and average order value (AOV) fell across all regions in 2022. North America remains the largest AOV with $242,39% above Latin America, the lowest performer.
• Europe, the Middle East, and Africa saw a significant increase in order volume share in 4Q22, climbing from 26% to 33% quarter-over-quarter among known region sales.
-
- 

<b>Shipping times</b>
- iphone and bose have latest day to ship to the customer,the aveage of those product shipday are 6 days. unlikeyly airpod 3.5days
- iPhones and Bose headphones have, relative to all other products, incredibly high variability when it comes to shipping times. One might wonder if this is a chicken and egg situation, considering their sales. Are the shipping times for iPhones and Bose headphones all over the place because we rarely sell them (and consequently don't have much stock on hand)? Or do we rarely sell iPhones and Bose headphones because customers find our shipping times to be too unpredictable?  



<b>Technical Analysis:</b><br>
In this section, I primarily used Tableau. SQL and BigQuery were also used to create a dataset for Tableau. My Tableau dashboard incorporates filters, tables, line graphs, and area charts.

You can find the SQL code for the dataset I created in BigQuery [here](https://github.com/sean-atkinson/elist_ecommerce_analysis/blob/main/sql/elist_dataset_tableau_query.sql).

Here is a peek of what the Tableau dashboard for this part of my analysis looks like:

<img width="750" alt="Tableau dashboard showing tables, line graphs, and area charts for total sales, total orders, and average time to ship" src="https://imgur.com/DpPG33J.png">

An interactive version of the above Tableau dashboard can be found [here](https://public.tableau.com/app/profile/sean.atkinson/viz/ElistOrdersDashboard_16896324404540/ordersdashboard).

A copy of my Tableau workbook can be found [here](https://github.com/sean-atkinson/elist_ecommerce_analysis/tree/main/tableau).

<a id='section_5'></a>

You can find more detailed analysis in [this downloadable Excel workbook](https://github.com/sean-atkinson/elist_ecommerce_analysis/blob/main/excel/elist_orders_case_study.xlsx).

<a id='section_3'></a>
