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
- Interestingly, the first year of the pandemic (2020) saw the highest average order value of $298.
- Total orders were down to 19K in 2022 (from 31k in 2021).
- Revenue was down 44% year-over-year in 2022.
-  The concerning sales numbers of 2022 appear to reflect broader trends in the e-commerce industry. Factors such as the economic recession, an oversaturated market, decreased effectiveness of marketing campaigns, and supply chain issues were [identified by Statista](https://www.statista.com/chart/27982/e-commerce-revenue-and-forecasts/?ssp=1&setlang=en-CA&safesearch=moderate) as contributors to an unprecedented forecasted shrink in e-commerce revenue for 2022. Particularly notable were changes in digital marketing practices: [the privacy update in Apple's iOS 14.5, alongside a 47% increase in Facebook advertising costs](https://www.forbes.com/sites/forbestechcouncil/2022/03/14/e-commerce-trends-2022-what-the-future-holds/?ssp=1&setlang=en-CA&safesearch=moderate&sh=6ca444d258da), seems to have had a profound impact on e-commerce merchants.

<b>Seasonality</b>
- Winter and spring tend to perform better, most likely due to holiday sales and special promotions.
- There's a noticeable sales uptick in the first half of 2020, most likely due to the pandemic.

<b>Products</b>
- Airpods have consistently been our best-selling product in terms of total orders. 
- In 2022, Airpods and a gaming monitor made up a whopping 68% of all orders.
- Bose Soundsport Headphones have consistently performed poorly. We've only sold 25 pairs over 3 years.

<b>Loyalty Program</b>
- We recommend continuing to expand this. When the program started in 2019, members were spending an average of $29 less than non-members. In 2022, loyalty program members now spend an average of $34 more than non-members per purchase.
- By the end of 2022, loyalty program members generated 27% more revenue compared to non-members. This is largely attributed to their higher receptiveness to our marketing efforts. The fact that they are loyalty members makes them more open to receiving emails from us, as demonstrated by spending 217% more than non-members through that channel in 2022. It's worth noting that email marketing boasts a [47x ROI](https://cxl.com/blog/email-marketing-strategy/) and has remained relatively unaffected by changes in the marketing landscape.<br>


<b>Technical Analysis:</b><br>
For this section, I used Pivot Tables, conditional formatting, aggregation functions, and statistical analysis to clean, analyze, and summarize my insights for the finance and product teams.

Here is an example of the pivot table used for seasonality insights:

<img width="750" alt="Excel pivot table showing totals and growth rates for monthly sales, AOV, and orders" src="https://imgur.com/Uns8sPD.png">

You can find more detailed analysis in [this downloadable Excel workbook](https://github.com/sean-atkinson/elist_ecommerce_analysis/blob/main/excel/elist_orders_case_study.xlsx).

<a id='section_3'></a>
