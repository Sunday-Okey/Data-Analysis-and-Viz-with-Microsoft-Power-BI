# Data Model for Seven Sages Brewing Company

## The Challenge
Seven Sages have a common problem. They have a lot of data that is not centrally located and they need help getting everything organized so that they can
understand their corporate profitability. They know that their main flagship beer, the Bamboo Grove Maibock, is the most popular but it's unclear otherwise, how much
is being sold and what is ultimately the most profitable, and if some are perhaps even losing money. The Company is located in Washington State, but they also sell their beer
in British Columbia, so there's a currency exchange consideration as well, and they have a fiscal calendar. So for their data model, they need to have a fiscal calendar as 
well as a standard calendar incorporated within their date table.

The goal is create a `data model` and Power BI report for Seven Sages Brewing Company that combines information from all over the company. The data model will make it possible for the company's CFO to quickly review and analyze what beers sell well and which ones generate the highest profitability. In this project we will create a highly functional data model that can generate insight by customers and products, that incorporate currency rates and which accounts for both `fiscal and calendar` year.



## The Power BI Pipeline
#### 1. Access the Data Sources

First, we need to access the data sources needed for the report. These may exist in various file formats and it's not unusual to have to gather them from various siloed teams around the organization.

#### 2. Extract, Transform, and Load with Power Query

From there we use the Power Query engine (which is included in Power BI) to Extract, Transform, and Load (ETL) the source data. The goal in this step is to both clean up the data and also morph it into the shape that we need for our data model.

#### 3. Create a Data Model

When we use Power Query to save and apply queries in Power BI, these queries become tables in the data model layer. Note in the diagram of the pipeline (shown below) that each query points to a corresponding data table. This is meant to reflect that the data and transformations that occur in Power Query align to the data in each of these tables (we'll look at the details of how this happens later on). You can also see in the diagram that our tables are connected to form the data model. These relationships allow calculations to flow between tables, and allow us to build a more efficient model than we would get if we simply lumped all the data together in one giant table.

#### 4. Generate a Power BI Report

Finally, with our data cleaned up, transformed, and connected within the data model, we can use all of this to generate what we've been wanting all along—a Power BI report that presents the data in a visual and user-friendly manner.

![image](https://github.com/user-attachments/assets/086a164f-ece4-43b2-ab6f-b6393d5a16b6)

## Main Steps
Here are the main steps.

- **Source files**. Download and familiarize ourselves with the source files provided by SSBC.
- **Sketch the data model**. Sketch out the data model you intend to build.
- **Use Get Data**. Use Get Data to load the data from the source into Power BI.
- **Structure, combine, and clean the data**. Clean and format data so that it will work well in the data model.
- **Create date table**. Create a date table to support time intelligence.
- **Build relationships between our tables**. Build a relationship from each dimension to the relevant key on the fact table.
- **Write your measures**. To satisfy the CFO's requirements, we will need to write six measures—to calculate Sales, Cost of Sales and Gross Profit Margin in two different currencies.
 - **Create a report**. Build a basic visual report to display our findings.

## Data Sources

![image](https://github.com/user-attachments/assets/e725d3d1-c0f9-4b11-a061-95c30b13717a)

## Data wrangling with Power Query:

We utilized Power Query clean data and for pre-processing that involved:

- combining 12 monthly sales files into one unifined Sales query for better analysis.
- Merging Customer List (as of FY2021).txt and SSBC Product Offerings.pdf to Product_CP query to include all product relevalt features.
- Reviewed data types for each field to ensure that they are identified correctly
- Removed any or all blank rows
- Got rid of unnecessary columns
- Adressed any typos that will impact report results


## Creating Date Table:
A date table was created using Power Query that is set to update dynamically based on the fact table’s start and end data including future sales. The date table includes standard fields:

- Calendar month name and number
- Calendar year
- Fiscal period
- Fiscal year
- Fiscal quarter -Quarter - FY (e.g., Q1 - FY2020)

> Note: Seven Sages' Fiscal year begins on October 1st and runs until September 30th. For instance a transaction on Sept 20th 2020 would fall in FY 2020, but a transaction on October 20th would fall in FY 2021


## Create Data Model (build relationships between tables):

![image](https://github.com/user-attachments/assets/57ab2abf-bb2d-4da2-8f2f-4eef3e737949)


### Fact Table

- Sales

### Dimension Tables
- Products
- Customers
- Calendar
- Exchange Rates

## Measures

## Writing DAX Measures:
To satisfy the Company's requirements, we will need to write six measures—to calculate Sales, Cost of Sales and Gross Profit Margin in two different currencies. The following measures have been created using DAX, are present on the data model, and are clearly labeled:

- Total Sales ($USD)
- Cost of Sales ($USD)
- Gross Profit Margin (%)
- Total Sales ($CAD)
- Unit Sales by Product (%, USD)
- Gross Profit by Product (%,USD)

## Report

To satisfy the requirements, the report will have three tabs, one summarizing sales by customer and customer type across quarters and would be labeled Sales and GPM. The second will simply summarize the percentages of gross profit and unit sales by product and would be labeled Gross Profit and Unit Sales. Both tabs have brief executive summary at the bottom. Next, we will dig in a little deeper and figure out what product type is most profitable per serving for serving for SSBC.

The PDF report can be found on SSBC-Report file provided on this repo.

![image](https://github.com/user-attachments/assets/5509634d-443c-4d77-a480-9c92df8bf56c)



![image](https://github.com/user-attachments/assets/7558066a-2604-4bdc-82fb-4db12f5e1eb8)


![image](https://github.com/user-attachments/assets/a5b690c9-e513-4097-bbbd-41d117d43392)


![image](https://github.com/user-attachments/assets/e40b8e19-6508-4f3a-88e8-31daa6cf303d)

The Report can be viewed live here

[View Live Here](https://app.powerbi.com/groups/me/reports/adef93f6-02f3-4343-8ec3-d95f2a2f2604/bc0fc33648195482638f?experience=power-bi)



