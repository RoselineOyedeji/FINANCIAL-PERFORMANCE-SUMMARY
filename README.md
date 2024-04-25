
# Sales Performance-Dashboard

### Dashboard Link : https://app.powerbi.com/view?r=eyJrIjoiYWNhM2RiNmYtOGVkOC00OTQ1LThjZTItYzMyMTFlNWQzNjJiIiwidCI6ImRmODY3OWNkLWE4MGUtNDVkOC05OWFjLWM4M2VkN2ZmOTVhMCJ9

## Insights and Objectives

This dashboard helps businesses understand their sales performance better. It helps the business know if they are making sales or losing sales, if they are making profit or not. Through different periods, they get to know where they had highest sales, profit and quantity sold, & thus they can improve their business by identifying these area. It also lets them know the sales difference delay & percentage change, thus since by using this dashboard they have identified this areas, they can further work on factors that facilitate sales growth.

Since, there is growth in sales and profit in all of the year, thus in all they must keep working on improving their business. 

`Also since they sold out more of furnishings to consumers, corporate offices, and to home offices, thus they must try to stock it more to meet customers demand and avoid stockouts.`


### Steps followed 

- Step 1 : Load data into Power BI Desktop, dataset is a xlsx file.
- Step 2 : Open power query editor & in view tab under Data preview section, check "column distribution", "column quality" & "column profile" options.
- Step 3 : Also since by default, profile will be opened only for 1000 rows so you need to select "column profiling based on entire dataset".
- Step 4 : It was observed that none of the columns had errors & empty values except the state column which had few blanks & a column named "Row ID" which has a wrong incremental value.
- Step 5 : In power query, another Row ID was created with the use of "add columns indexes" starting from 1.
- Step 6 : Since the data has one table containing all the informations, a dimension's tables was created.
- Step 7 : In the table view, under the calculation pane a new table was created named "Calendar"
- Step 8 : In the report view, under the view tab, theme was selected.
- Step 9 : In the report view, a measures table was also created.
- Step 10 : Visual filters (Slicers) were added for four fields named "Year", "Region", "Segment" & "Shipping Method".
- Step 11 : Three card visuals were added to the canvas, one representing total revenue, total profit & other representing quantity sold with previous year and change in percentage.
           Using visual level filter from the filters pane, basic filtering was used & blank values were unselected for consideration into revenue calculation.
           
           Although, by default, while calculating total revenue, profit and quantity sold blank values are ignored.
- Step 10 : A line and clustered chart was also added to the report design area representing the current and previuos year revenue by month. While creating this visual, measure named "Sales py line and Sales py% line" was also added to the line y axis bucket, thus making it show a line to display the sales difference and %change. 
- Step 11 : A clustered column was added to visualize the current and previous year revenue of different product,

  (a) Bookcases

  (b) Chairs
  
  (c) Furnishings
  
  (d) Tables
  
In our dataset, a field parameter was created which was added to our barchart displaying top 10 states and cities.

All blanks have been ignored while calculating all measures.

- Step 12 : In the report view, under the insert tab, two circle shapes were added to the canvas, one of them was used to represent current year & the other for previous year.
- Step 13 : In the report view, under the insert tab, a blank button was inserted to display a welcome text. 
- Step 14 : Calculated column was created in which to show top 10 state.

for creating new column following DAX expression was written;
        City = 
            TOPN (
                10,
    		SUMMARIZE (
        	DimRegion,
        	DimRegion[City],
        	"TotalSales", [Total sales]
    		),
    [TotalSales], DESC
)

- Step 15 : Two new pages were created named "Profit" and "Quantity Sold"
All that was on the sales page was moved to the profit and quantity sold page, only that the information on it is now based on profit and quantity sold respectively.
- Step 16 : A bookmark navigator was created to help navigate to each of the pages.

`Snap of Sales py line measure`

![Sales py line](https://github.com/RoselineOyedeji/SALES-PERFORMANCE-DASHBOARD/assets/161141258/523e3079-0ab2-417f-b8a2-8b80dbb68ae7)

 `Snap of Sales py% line measure`

![Sales py% line](https://github.com/RoselineOyedeji/SALES-PERFORMANCE-DASHBOARD/assets/161141258/de3d64cf-4147-4c57-a01b-dc720847755f)



`Snap of the dashboard`

![Sales performance](https://github.com/RoselineOyedeji/SALES-PERFORMANCE-DASHBOARD/assets/161141258/83c75900-9fac-4beb-ae22-eeaca669a218)


# Insights

A single page report was created on Power BI Desktop & it was then published to Power BI Service.


# Sales Performance Dashboard.md.txt
Displaying # Sales Performance Dashboard.md.txt.
