
# Business Insights 360

## Project Overview

AtliQ Hardware is rapidly growing company in the recent years, and they have decided to implement the data analytics using PowerBi in their company for the first time to surpass their competitors in the market and to make data driven decisions. This project is hoped to give answers to the questions of stakeholder in terms all the aspects like finance, sales, marketing and supply chain.

Worked on this project by following the Codebasics PowerBi Course, Link to the course is [here](https://codebasics.io/courses/power-bi-data-analysis-with-end-to-end-project)

[Live report link](https://app.powerbi.com/reportEmbed?reportId=ecd4d5c9-a692-447f-8474-9a5e2628c683&autoAuth=true&ctid=88f944d0-1278-45f9-88d8-dc81b5f77b17)


## Tech Stacks

- SQL
- PowerBi Desktop
- Excel
- DAX language
- DAX studio (for optimizing the report)
- Project charter file

## PowerBI Learnings

- Key questions to ask before starting a project
- Creating calculated columns
- Building measures using DAX
- Developing effective data models
- Utilizing bookmarks to toggle between visuals
- Implementing page navigation with buttons
- Preventing division by zero using the DIVIDE function
- Creating a date table with M language
- Designing dynamic titles based on applied filters
- Leveraging KPI indicators for performance tracking
- Applying conditional formatting with icons or background colors in visuals
- Employing data validation techniques
- Understanding Power BI Services
- Publishing reports to Power BI Service
- Configuring a personal gateway for automatic data refresh
- Creating and managing Power BI Apps
- Collaboration, workspaces, and managing access permissions in Power BI Service
- And more! 

## Business terminologies

- Gross price
- Pre-invoice deductions
- Post-Invoice deductions
- Net Invoice sale
- Net sales
- Net profit
- COGC - cost of goods sold
- YTD - Year to Date
- YTG - Year to Go
- Direct
- Retailer
- Distributors
- Consumer

## Company back ground


AltiQ Hardware, a rapidly expanding company with a global presence, specializes in selling computers and computer accessories through three key channels:
- Retailers
- Direct Sales
- Distributors

Recently, the company encountered an unexpected loss after opening a store in America. This decision was primarily based on surveys, intuition, and basic Excel analysis. Meanwhile, competitors have established robust analytics teams to perform detailed analysis and drive data-informed decisions. Recognizing this gap, AltiQ Hardware is compelled to build its own analytics team to generate actionable insights and make strategic, data-driven decisions to remain competitive in the industry.

## Few Questions asked prior to start building the report and dashboard

- What is the primary objective of creating this Power BI dashboard?
- How will the success of this project be evaluated?
- What is the timeline or deadline for completing the project?
- Are stakeholders expecting a preview before the final release?
- What are the stakeholders' expectations from this project?
- What concerns do stakeholders have regarding the development of this dashboard?
- Who will use this dashboard, and for what specific purposes?
- What outcomes do stakeholders anticipate upon the project's completion?
- What potential challenges could arise during the development of this project?
- What resources or data are required to build the dashboard?
- Do stakeholders have any specific inputs regarding the design or visual aspects of the dashboard?

Following the project kickoff meetings, the data engineering team provided the requested data to the data analytics team. Let’s dive in and explore it.

## Dataset Understanding

Having a clear understanding of the available data is crucial for effective analysis. Before diving into the analysis, take time to familiarize yourself with the data at hand.

- Dimension Table: Contains static data such as customer and product details.
- Fact Table: Includes transaction-related data.

	- gdb041:
		- dim_customer
			- 27 distinct markets (ex India, USA, spain)
			- 75 distinct customers thorough out the market
			- 2 types of platforms
				- Brick & Motors - Physical/offline store
				- E-commerce - Online Store (Amazon, flipkart)
			- Three channels
				- Retailer
				- Direct
				- Distributors

		- dim_market
			- 27 distinct markets (ex India, USA, spain)
			- 7 sub-zones
			- 4 regions
				- APAC (Asia Pacific)
				- EU (Europe)
				- NA (North America)
				- LATAM (Latin America)

		- dim_product
			- Divisions
				- P&A
					- Peripherals
					- Accessories
				- PC
					- Notebook
					- Desktop
				- N&S
					- Networking
					- Storage
			- There are 14 different categories, Like Internal HDD, keyboard
			- There are different variants available for the same product

		- fact_forecast_monthly
			- This table is used to forecast the customer’s need in advance, which can help in
				- Higher customer satisfaction
				- Reduced cost in warehouses for storage purpose
			- The table is denormalized by data engineering team, as it is a data warehouse which is aimed to be used for analytical work.
			- All the date of the month will be replaced by the start date of the month
			- It will have all the column names and in the end it will have the forecast quantity need of the customer

		- fact_sales_monthly
			- This table is more or less is same as fact_forecase_monthly table, but the last column has the value of sold quantity instead of forecast value.

	- gdb056:
		- freight_cost
			- This table has details of travel cost and other cost for each market with fiscal year
		- gross_price
			- Has the details of gross prices with product code
		- manufacturing_cost
			- Has the details of manufacturing cost with product code with year
		- Pre_invoice_dedutions
			- Has the details of pre invoice deductions percentage for each cutomer with year
		- Post_invoice_deductions
			- Post invoice deductions and other deductions details

## Importing data into PowerBi

- data from MySQL database is imported to PowerBi by connecting to MySQL database via Database access credentials

## Data Model

- Data modeling is crucial and serves as the foundation of the report. All visuals will be built upon the data model.
- Poor data modeling affects the over all performance of the report.
- Snowflake Data Model modelling approach is followed in this project.
![Image](https://github.com/user-attachments/assets/01de765e-f94c-43a7-b02f-d7809babdfde)

## Dashboard design

Based on the mockups received as requirements, the team will begin designing the visuals and create measures as needed.

## Home View

In the Home view, all the view buttons will be accessible. The user can navigate to a specific view page by clicking the corresponding button.

- info
- Finance View
- Sales View
- Marketing View
- Supply chain View
- Executive View
- Support

## Home Page
![Image](https://github.com/user-attachments/assets/92dcd0cb-0a4d-4b85-b31e-a6beeb48d82c)

## Finance Page
![Image](https://github.com/user-attachments/assets/28c40c83-c255-464d-8bd4-43aab72e21e5)


## Sales Page
![Image](https://github.com/user-attachments/assets/a9b1add1-53e5-40c2-bf3c-34bbe12b917a)

## Marketing Page
![Image](https://github.com/user-attachments/assets/a100c66b-304b-4368-884c-0f5c4b0da009)

## Supply Chain Page
![Image](https://github.com/user-attachments/assets/ca286565-fce3-46aa-b989-4e60b1b6fa5c)

## Executive Page
![Image](https://github.com/user-attachments/assets/05146949-5f29-4a82-89db-3fb4cdb2f170)

## Project outcome

This report enables data-driven decision-making and helps answer numerous "why" questions based on various situations.









