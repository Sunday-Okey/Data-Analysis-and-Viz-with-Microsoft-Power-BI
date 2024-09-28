# Data Analysis and Visualization with Microsoft Power BI Nanodegree Program

This is a repository is for projects in Udacity's Data Analysis and Visualization with Microsoft Power BI Nanodegree Program that covers the necessary skills needed to become a 
successful data analyst such as data wrangling, data pre-processing, visualization and analysis using Microsoft Power BI as the primary tool.

Each project contains a detailed report documenting the project business problem, description, processes and findings.

## The Power BI Pipeline
1. Access the Data Sources

First, we need to access the data sources needed for the report. These may exist in various file formats and it's not unusual to have to gather them from various siloed teams around the organization.

2. Extract, Transform, and Load with Power Query

From there we use the Power Query engine (which is included in Power BI) to Extract, Transform, and Load (ETL) the source data. The goal in this step is to both clean up the data and also morph it into the shape that we need for our data model.

3. Create a Data Model

When we use Power Query to save and apply queries in Power BI, these queries become tables in the data model layer. Note in the diagram of the pipeline (shown below) that each query points to a corresponding data table. This is meant to reflect that the data and transformations that occur in Power Query align to the data in each of these tables (we'll look at the details of how this happens later on). You can also see in the diagram that our tables are connected to form the data model. These relationships allow calculations to flow between tables, and allow us to build a more efficient model than we would get if we simply lumped all the data together in one giant table.

4. Generate a Power BI Report

Finally, with our data cleaned up, transformed, and connected within the data model, we can use all of this to generate what we've been wanting all along—a Power BI report that presents the data in a visual and user-friendly manner.

![image](https://github.com/user-attachments/assets/086a164f-ece4-43b2-ab6f-b6393d5a16b6)


## Nanodegree Courses:

| Project No. | Project                                            |
|-------------|----------------------------------------------------|
| 01          | Build a Data Model for Seven Sages Brewing Company |
| 02          | Building a Power BI Report for Waggle              |
| 03          | Market Analysis Report for National Clothing Chain |
