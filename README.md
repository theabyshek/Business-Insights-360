# Business Insights 360°

### Project Overview
AtliQ Hardware (a hypothetical company) has experienced rapid growth in recent years and has decided to implement data analytics using Power BI for the first time. This initiative aims to outpace market competitors and facilitate data-driven decision-making. The project is expected to address stakeholder inquiries across various areas, including finance, sales, marketing, and supply chain.

I completed this project by following the Codebasics Power BI course, Link to the course is [here](https://codebasics.io/bootcamps/data-analytics-bootcamp-with-practical-job-assistance)

[Live Report Link](https://app.powerbi.com/view?r=eyJrIjoiNDIyMjc4ZjAtN2Q5My00YjU3LWE3OTItYzI4ZTc1NDE2Njg2IiwidCI6IjkyMGJmNGY2LTVlOGQtNDBhZC1iNmZiLTZjN2ZkZjcxYjY2OSJ9&pageName=ReportSection27e05ca5ad0738a527bd)

### Tech stacks
- SQL
- Power BI Desktop
- Excel
- DAX language
- DAX studio (for optimizing the report)
- Project charter file

### Power BI techniques Learnt
- What are all the questions should be asked before staring the project
- Creating calculated columns
- Creating measure using DAX language
- Data modeling
- Using Bookmarks to switch between two visuals
- Page navigation with buttons
- Using divide function to prevent zero division errors
- Creating date table using M language
- Dynamic titles based on the applied filters
- Using KPI indicators
- Conditional formatting the values in visuals using icons or background color
- Data validation techniques
- Power BI services
- Publishing reports to Power BI services
- Setting up personal gateway to set up the auto refresh of data
- Power BI App creation
- Collaboration, workspace, access permissions in Power BI services

### Company’s back ground
AtliQ Hardware is a rapidly expanding company that has recently established a global presence. It specializes in selling computers and computer accessories through these three different channels.

- **Retailers**
- **Direct**
- **Distributors**
  
Recently, the company encountered unexpected losses after opening a store in America, relying on surveys, intuition, and basic Excel analysis. Meanwhile, competitors have well-established analytics teams that drive data-based decisions. Consequently, AtliQ Hardware must develop its own analytics team to obtain data-driven insights and make informed decisions to better compete in the industry.

## Questions to ask before starting with dashboard

### Objective of Building the PowerBI Dashboard:
- What is the primary goal of creating this PowerBI dashboard?
### Success Criteria:
- How will the success of this project be evaluated?
### Project Deadline:
- What is the timeline for completing the project?
### Stakeholder Preview:
- Are stakeholders expecting a preview before the final release?
### Stakeholder Expectations:
- What are the stakeholders' hopes for the outcome of this project?
### Stakeholder Concerns:
- What concerns do stakeholders have regarding the development of this dashboard?
### Dashboard Users and Purpose:
- Who will be using this dashboard, and for what specific purposes?
### Stakeholder Expectations upon Completion:
- What are the stakeholders' expectations for the project's completion?
### Potential Risks:
- What potential issues could arise during the development of this project?
### Resources and Data Requirements:
- What resources and data are necessary to build this dashboard?
### Stakeholder Input on Design:
- Have stakeholders provided any input on the design and views of the dashboard?

After the project kick off meetings, the data engineering team has given the data as per the request of data analytics team, let’s explore them.

### Dataset Understanding
Gaining a thorough understanding of the available data is crucial before beginning any analysis. It is important to familiarize yourself with the data at hand to ensure a more effective analysis.

**Dimension table** : It will have the static data like details of customer and products

**Fact table** : It will have the data about the transactions

- gdb041:
    - dim_customer
        - **27** distinct markets (ex India, USA, spain)
        - **75** distinct customers thorough out the market
        - **2** types of platforms
            - Brick & Motors - Physical/offline store
            - E-commerce - Online Store (Amazon, flipkart)
        - Three channels
            - Retailer
            - Direct
            - Distributors
    - dim_market
        - **27** distinct markets (ex India, USA, spain)
        - 7 sub-zones
        - 4 regions
            - APAC
            - EU
            - nan
            - LATAM
    - dim_product
        - Divisions
            - P & A
                - Peripherals
                - Accessories
            - PC
                - Notebook
                - Desktop
            - N & S
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
- gdb056
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

### Importing data into PowerBi
Since the database used in this project is MySQL, we need to import the datasets into PowerBI by providing the necessary database access credentials.

### Data Model
- Data modeling is essential and serves as the foundation of the report, as all visuals are built upon it. 
- Poor data modeling can negatively impact the overall performance of the report. 
- Adhering to best practices in data modeling is crucial. 
- In this project, we have employed the Snowflake data modeling method.

<img src="https://github.com/Naveen-S6/Business_Insights_360/blob/main/Resources/Data_model.png" class="center">

### Dashboard designing
Based on the mock ups received as requirement, the team will start designing the visuals and create measure as and when required

**Home view**
In Home view, all the views button will be available. User will land on specific view page by clicking the button

- Info
- Finance View
- Sales View
- Marketing View
- Supply chain View
- Executive View
- Products
- Support

<img src="https://github.com/theabyshek/Business-Insights-360-/blob/main/Home%20page.png" class="center">

### Project Outcome
This report enables data-driven decision-making and can help address numerous "why" questions based on various situations.
