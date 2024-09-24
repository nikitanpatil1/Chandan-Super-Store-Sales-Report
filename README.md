# Chandan Super Store Sales Report

### Dashboard Link : https://app.powerbi.com/links/SFI5k0uF0f?ctid=8f38f329-bce4-4c5f-8621-694d67cff284&pbi_source=linkShare

### Report Link (Web) : https://app.powerbi.com/view?r=eyJrIjoiNjQzYWU5NGUtMGE0ZS00ZjA3LWJkMzItZDg5ZTc2NzlkNzMyIiwidCI6IjhmMzhmMzI5LWJjZTQtNGM1Zi04NjIxLTY5NGQ2N2NmZjI4NCJ9

## Problem Statement

This dashboard helps the Chandan Super Store understand their sales, profits and customer better.Sales are the major factor of any business for its growth and success. This report is the visual representation of two years data compared with each other to understand the sales of the store. The steps and insights are shared in this report.

### Steps followed 

- Step 1 : Load data into Power BI Desktop, dataset is a csv file.
- Step 2 : Open power query editor & in view tab under Data preview section, check "column distribution", "column quality" & "column profile" options.
- Step 3 : It was observed that in none of the columns errors & empty values were present except column named "Returns" and there were two empty columns which were later deleted in data cleaning process.
- Step 4 : In "Returns" the value for "orders not returned customers" was given as "N#A" which would be difficult to process. So the value of the customers who have not returend any order till date was modified to "0".
- Step 5 : There was no need for the data processing step at that movement so the next step was executed i.e data visualization. 
- Step 6 : In the report view, under the view tab, theme was selected.
- Step 7 : Three clustered bar charts were added which consist of 1) Sales by category which are divided into three parts "Office Supplies, Technology, Furniture". 2) Sale by sub-category (i.e top ten) which differs based on the region. 3) Sales by ship mode which are divided into four parts "Standard class, Second class, First class, Same day".
- Step 8 : Then two stacked area charts were added which show us the Profit by months and Sales by months with respect to both the years which we have used for analysis.
- Step 9 : Then three donut charts were added to show 1) Sales by region divided into "Central, South, East, West". 2) Sales by segment divided into "Home office, Consumer, Corporate". 3) Sales by payment mode divided into "Card, Cash on delivery, Online".
- Step 10 : Visual filters (Slicers) were added using Regions which included these four regions "Central", "East", "South" & "West". 
- Step 11 : Four card visuals were added to the canvas,  representing total sales, total orders, total profit and average ship days i.e days required to ship the order.

- Step 12 : In order to show the average days required to ship the order, The  "Average ship days" were calculate using the Dax expression.

for creating new column following DAX expression was written;
       
       AvgDelivery = 
       DATEDIFF('SuperStore_Sales_Dataset'[Order Date],'SuperStore_Sales_Dataset'[Ship Date],DAY)

 - Step 13 : The report was then published to Power BI Service.
 
![publish](https://github.com/user-attachments/assets/f76883cc-ff0a-4ca1-8ed6-aecddd75f871)

# Snapshot of Dashboard (Power BI DESKTOP)

![fulldashboard](https://github.com/user-attachments/assets/35eb6d40-10be-4e15-a679-ef2effbe29f5)

 # Report Snapshot 

![report](https://github.com/user-attachments/assets/30008b62-b827-4479-8c77-7d2ca5922784)

# Insights

A single page report was created on Power BI Desktop & it was then published to Power BI Service.

Following inferences can be drawn from the dashboard;

### [1] Sales by Region

   Central = 3,41,007 (21.78 %)

   East = 4,50,234 (28.75 %)

   South = 2,52,121 (16.1 %)

   West = 5,22,441 (33.37 %)

    Thus, higher number of sales are done in west region then followed by East, Central and South.
           
 ### [2] Sales by Category and Sub-Category.

In Sales by Category its seen that
       
       Most of the items sold or the orders are from the Office Supplies Category .

While in Sales by Sub-Category its seen that
       
       Phones are the top most item ordered from the Sub-Category section .
  
  ### [3] Sales by Segment 
  
   Home Office = 19 %

   Consumer = 48 %

   Corporate = 33 %

    From this observation we get to know that majority of orders come from Consumer Segment.

 ### [4] Sales and Profit by Month w.r.t both the years
 
 ### Sales by Month
 
 By comparing the sales of both the years simultaneously we get the insights such as.

         1) The  increase and decrease of sales pattern in graph has been same for both the years.

         2) The number of sales have been increased in the year 2020 in comparison with the previous year i.e 2019.

         3) September, November and December are the most favourable months for higher sales.

         4) While it is seen that there is decline in sales in the months such as January, February, June, July, August.
 
 ### Profit by Month
 
 By comparing the profit of both the years simultaneously we get the insights such as.

         1) In the month of october even though there was decline in sales, the store has earned major profit in that month itself.

         2) Though the store had higher sales in the month of november, still it was not able to make any profit in that month 
            rather the profit was drastically decreased.

         3) Top months when store made great profits were March, May, October and December.

         4) While it is seen that there is decline in profits in the months such as February, April, August and November.
         
### [5] Sales by Payment and Ship Mode

In Payment Mode its observed that
  
    Highest number of customer prefers "Cash On Delivery" as a payment option with wooping count of 43 %. 

In Ship Mode its observed that
  
    Highest number of customer prefers "Standard Class" as a shipping option.
