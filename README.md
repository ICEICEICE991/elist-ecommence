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
  * Using Excel, I spend a limited time taking a quick look at some of the broad trends within the data to see what notable insights can be pulled  for the finance and product team. and determine which section need using more time and more complicated the tool like python and SQL
    
- <b>Part 2: Targeted Insights</b>

  * With the aid of SQL, I capture more detail and more insight for my team including finance an marketing  I pull out more targeted insights for the finance and marketing team, highlighting things like MacBook sales, refund rates, and best-performing marketing channels.

- <b>Part 3: Visualizations</b>
  * Leveraging Tableau, I create a interactive dashboard for the finance and product teams (as well as the sales and operations teams to a lesser extent) to monitor metrics of interest on an ongoing basis.

- <b>Part 4: Recommendations & Next Steps</b>
  * Suggestions on things to take a look at going forward, report to the senior, and recommend more insight to my senior manager.


# Data Structure & Initial Checks
Here is the Entity Relationship Diagram:
The data are four tables and consists of information on orders, order statuses, customers, and geographic information.


<img width="750" alt="Entity Relationship Diagram showing orders, order statuses, customers, and geographic information tables" src="<img width="1039" alt="Screenshot 2024-10-29 at 3 51 03 PM" src="https://github.com/user-attachments/assets/65f1e09b-af4f-4a3e-b911-a5df79e5b9fe">

You can view the data in greater detail [here](https://github.com/ICEICEICE991/elist-ecommence/tree/main/elist_data).
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


### Excel Pivot Table Showing Totals and Growth Rates for Monthly Sales, AOV, and Orders

<img width="686" alt="Excel pivot table showing totals and growth rates for monthly sales, AOV, and orders" src="https://github.com/user-attachments/assets/5bb8b2b7-8157-4aed-a06c-a221e416eb73">


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

<b>Customer Onboarding and First Purchase Time Analysis (all years)</b>
- Average of 51 days between account creation and first purchase.

<b>Marketing channels (all years)<b>
- Direct - highest number of orders.
- Emails - second highest number of orders.

<b>Technical Analysis:</b><br>
-For this analysis, I used SQL and BigQuery. In regards to SQL, I used aggregation functions, window functions, joins, filtering, CASE expressions, common table expressions (CTEs), and in a couple instances the QUALIFY -clause to use row_number() to filter results.

<b>Lifetime Value (LTV) Analysis by Customer Segment:</b><br>

Objective: Identify high-value customer segments to help marketing and customer success teams focus retention efforts.

<b>Insights:<b>
-Identify segments with the highest LTV.
-Share with the Marketing Team to tailor retention and upsell strategies.
-Share with the Customer Success Team to prioritize high-value segments for personalized support.

<b>Customer Churn Analysis:</b><br>

Objective: Determine churn rate by analyzing customers who have not made a purchase within a specified period (e.g., past 6 months).
SQL Analysis:
Identify inactive customers based on the time since their last purchase:

Insights:
-Calculate churn rate and identify customers at risk of churning.
-Share with the Retention Team to run re-engagement campaigns.

<b>Average Order Value (AOV) by Marketing Channel:</b><br>

Objective: Compare AOV across marketing channels to optimize marketing spend.

Insights:
-Identify channels with the highest AOV, which may justify a higher marketing spend.
-Share with the Marketing Team to allocate budgets more effectively.

<b>Product Sales Performance by Region:</b><br>

Objective: Identify top-performing products in each region to inform regional inventory and marketing strategies.
SQL Analysis:
Calculate total sales and units sold per product by region:

Insights:
-Highlight which products perform best in each region.
-Share with Regional Marketing and Inventory Teams to stock and promote products according to regional demand.

<b>Repeat Purchase Rate:</b><br>

Objective: Measure repeat purchase rates to understand customer loyalty and retention.
SQL Analysis:
Calculate the percentage of customers with more than one order:

Insights:
-Determine the overall repeat purchase rate.
-Share with Customer Success and Marketing Teams to develop loyalty programs or re-engagement strategies for one-time buyers.

<b>Time to Fulfillment Analysis:</b><br>

Objective: Measure the average time from purchase to delivery and identify delays in the fulfillment process.
SQL Analysis:
Calculate the time (in days) between order and delivery dates:

Insights:
-Identify any patterns in delayed orders and share with the Operations Team.
-Track which regions or products experience delays to optimize logistics.





Here is an example of a query result that uses the aforementioned qualify clause:
```sql
-- Creating a brand category and totaling the amount of refunds per month
-- Filtering to the year 2020
WITH refund_counts_cte AS (
    SELECT
        CASE
            WHEN LOWER(orders.product_name) LIKE '%airpod%'  THEN 'Airpod'
            WHEN LOWER(orders.product_name) LIKE '%macbook%' THEN 'Macbook'
            WHEN LOWER(orders.product_name) LIKE '%iphone%' THEN 'iPhone'
            WHEN LOWER(orders.product_name) LIKE '%samsung%' THEN 'Samsung'
            WHEN LOWER(orders.product_name) LIKE '%thinkpad%' THEN 'ThinkPad'
            WHEN LOWER(orders.product_name) LIKE '%bose%' THEN 'Bose'
            WHEN LOWER(orders.product_name) LIKE '%monitor%' THEN 'Monitor'
            ELSE 'Unknown'
        END AS brand,
        DATE_TRUNC(order_status.refund_ts, MONTH) AS month,
        COUNT(order_status.refund_ts) AS num_refunds
    FROM 
        elist.orders AS orders 
    JOIN 
        elist.order_status AS order_status 
    ON 
        orders.id = order_status.id  -- Adjust the join to use 'id' instead of 'order_id'
    WHERE 
        EXTRACT(YEAR FROM order_status.refund_ts) = 2020
    GROUP BY 
        1, 2  -- Grouping by brand and month
),
-- Ranking refunds per brand to get the highest month per brand
ranked_refunds_cte AS (
    SELECT
        brand,
        month,
        num_refunds,
        ROW_NUMBER() OVER (PARTITION BY brand ORDER BY num_refunds DESC) AS rnk
    FROM 
        refund_counts_cte
)
-- Selecting the highest refund month for each brand
SELECT
    brand, 
    month, 
    num_refunds
FROM 
    ranked_refunds_cte
WHERE 
    rnk = 1
ORDER BY 
    brand;

```
And here is its result:
| brand    | month      | num_refunds |
|----------|------------|-------------|
| Airpod   | 2020-06-01 |          45 |
| Macbook  | 2020-09-01 |          13 |
| Monitor  | 2020-05-01 |          25 |
| Samsung  | 2020-04-01 |           7 |
| ThinkPad | 2020-04-01 |           9 |
| iPhone   | 2020-09-01 |           1 |


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



Here is a peek of what the Tableau dashboard for this part of my analysis looks like:

<img width="1076" alt="Screenshot 2024-11-06 at 2 16 02 PM" src="https://github.com/user-attachments/assets/1c135e76-f860-4812-a863-f090c5240073">


An interactive version of the above Tableau dashboard can be found [here](https://public.tableau.com/app/profile/libang.xia/viz/ElistE-CommerceOverview/Dashboard1).

A copy of my Tableau workbook can be found [here](https://public.tableau.com/app/profile/libang.xia/viz/ElistE-CommerceOverview/Dashboard1).

<a id='section_5'></a>

You can find more detailed analysis in [this downloadable Excel workbook](https://github.com/sean-atkinson/elist_ecommerce_analysis/blob/main/excel/elist_orders_case_study.xlsx).

<a id='section_3'></a>
# Part 4: Recommendations & Next Steps
[(Back to table of contents)](#table_of_contents)<br><br>

- - <b>Focus on Retaining Loyalty Members: Rather than solely expanding the loyalty program, prioritize retaining existing members, as acquiring new ones through channels outside of email is challenging. Enhancing member benefits could boost engagement and spending. We can take inspiration from Best Buy’s model, where loyalty members receive perks such as free two-day shipping and early access to limited-stock products. These benefits not only encourage repeat purchases but also generate additional revenue through membership fees.

- <b>Expand Revenue-Generating Product Lines: With computer hardware and Apple products accounting for 70% of sales and 80% of orders, consider diversifying our product assortment within these high-performing categories. Adding more computer hardware options could capture more market share and increase overall revenue.

- <b>Introduce Additional Services for Hardware Products: For high-value items like Apple products and computer hardware, consider offering services such as AppleCare, extended warranties, free repairs, or screen replacements. These add-ons could improve customer satisfaction and foster loyalty, especially given the significance of hardware sales to our business.

- <b>Reevaluate Low-Performing Products: Bose headphones and iPhones contribute only 1% of total sales. To boost their performance, consider bundling these products with other items or offering flash sales targeting customers outside the Apple ecosystem. For example, market noise-canceling Bose headphones to frequent travelers or offer promotions like “Buy a Laptop, Get a Free Bose Headphone” to encourage purchases.

- <b>Integrate Key Financial Metrics into Product Analysis: To gain a clearer picture of profitability, incorporate metrics such as customer acquisition costs and cost of goods sold (COGS) into our analysis. This will help us calculate customer lifetime value (LTV) and identify which products drive the highest net profits. Insights from this analysis could help us reverse declining sales by focusing on the most profitable products.

- <b>Investigate Shipping Volatility: Analyze the fluctuations in shipping times, especially for iPhones and Bose headphones. If the shipping volatility is impacting customer satisfaction and sales, consider whether replacing these products with others that better align with our top customer segments would be more beneficial.

<a id='section_6'></a>
# Addendum: Notes on Data Cleaning
[(Back to table of contents)](#table_of_contents)<br><br>
Please note that as a part of the data cleaning stage, 15,200 entries were identified as duplicates in the initial Excel data. To maintain the integrity and reliability of my insights, these duplicates were removed from the final dataset used for my analysis. Therefore, the original list of entries, which initially consisted of 108,127 entries, was reduced to 92,927 after removing the identified duplicates. This decision was essential to ensure the validity of the observations made for this project.
