# Customer Retention (PhoneNow)
![Power BI](https://img.shields.io/badge/Power%20BI-F2C811?style=flat&logo=powerbi&logoColor=black)

### Customer Retention (PhoneNow)


### Dashboard Link : https://app.powerbi.com/groups/me/reports/11e1a7fa-014f-4479-bc96-486565cc57f8/8effac9d9d3a47ad6a3e?experience=power-bi

## Problem Statement -
A few weeks after presenting your dashboard to the management, the Retention Manager from the telecom reaches out to you directly.

In addition, to better understand the data, the telecom Retention Manager has scheduled a meeting with the engagement partner at PwC to cover these points:

The retention department is here to get customers back in case of termination 
Currently, we get in touch after they have terminated the contract, but this is reactionary: it would be better to know in advance who is at risk 
We would like to know more about our customers: visualised clearly so that it’s self-explanatory for our management
The Retentions Manager has provided some information in the resources.

###The Retentions Manager has provided some information in the resources:-

       Create a dashboard in Power BI for Claire that reflects all relevant Key Performance Indicators (KPIs) and metrics in the dataset. Get creative! 

Janet, Retention Manager here at PhoneNow. Before you start working on our dashboard, let me provide you with some inputs
• Customers who left within the last month
• Services each customer has signed up for: phone, multiple lines, internet, online security, online backup, device protection, tech 
support, and streaming TV and movies
• Customer account information: how long as a customer, contract, payment method, paperless billing, monthly charges, total charges 
and number of tickets opened in the categories administrative and technical
• Demographic info about customers – gender, age range, and if they have partners and dependents

[PhoneNow inputs.pdf](https://github.com/user-attachments/files/16829838/PhoneNow.inputs.pdf)

 

## CHURN ANALYSIS 
![Churn dashboard](https://github.com/user-attachments/assets/24eea047-0b79-4887-b066-5bca3f2da673)

# Single page report was created on Power BI Desktop & it was then published to Power BI Service.

Following inferences can be drawn from the dashboard;


**Part 1 - Demographic**

###[1] Card Created for Distributing Agents: The number of customers identified as "at risk" (i.e., those with churn data marked as "yes") is 1,869.

   
### [A] Percentage Of seniors
        DIVIDE(CALCULATE(COUNT('01 Churn-Dataset'[SeniorCitizen]), '01 Churn-Dataset'[SeniorCitizen]=1, '01 Churn-Dataset'[Churn]="Yes"), CALCULATE(COUNT('01 Churn-Dataset'[SeniorCitizen]),'01 Churn-Dataset'[Churn]="Yes"),0) 
    
### [B] Partner in Percentage
        DIVIDE(CALCULATE(COUNT(churn[Partner]), churn[Partner]="Yes", churn[Churn]= "Yes"), CALCULATE(COUNT(churn[Partner]), churn[Churn]="Yes"),0) 

### [C] Dependents in Percentage
        DIVIDE(CALCULATE(COUNT('01 Churn-Dataset'[Dependents]), '01 Churn-Dataset'[Dependents]="Yes"), CALCULATE(COUNT('01 Churn-Dataset'[Dependents]), '01 Churn-Dataset'[Churn]="Yes"),0) 

![KPI Analysis](https://github.com/user-attachments/assets/179597db-1445-48b5-99ac-edbf6f68c91f)

### [2] Subscription time
The new column has been updated by transforming the data and applying a conditional column for improved visualization.
 
![Subscription time](https://github.com/user-attachments/assets/8df0d709-1c42-4479-8fc3-8c60e25f1df5) ![Coloum Conditioning ](https://github.com/user-attachments/assets/6d773aa3-924d-4b35-b4e2-80a35460df1b)


**Part 2 - Payment Method**

[1] Cluster Bar Chart
A clustered bar chart has been created to display payment methods, with electronic checks being the most common payment method among clients, followed by email checks, bank transfers, and credit cards.

[2] Donut Chart
A donut chart has been used to analyze paperless billing. It shows that 25.09% of people do not use paperless billing, while 74.91% of people use it as a payment method.

[3] Multi-Row Card
A multi-row card indicates that the average monthly charges paid by clients are $74.44, with a total average charge of $1,531.80.

Additional Information
The clustered bar chart was instrumental in creating the payment method table. By plotting the number of contracts on the Y-axis and selecting the percentage of the grand total (count), we obtained the following distribution:

Month-to-month: 88.55%
One year: 8.88%
Two years: 2.57%



**Part 3 - ###Services Customer signed Up for ###**

7 Power Queries has been added to the DAX to created complicated Calculative percentage system
![Singup Screenshot](https://github.com/user-attachments/assets/62eb4ffa-1804-49c9-a8ac-798da7e127c4)

Each one has its own uniquie and fundamental importance

      
### [1] Percentage Of Phone Service %
        DIVIDE(CALCULATE(COUNT('01 Churn-Dataset'[PhoneService]),'01 Churn-Dataset'[PhoneService]="Yes",'01 Churn-Dataset'[Churn]="Yes"),CALCULATE(COUNT('01 Churn-Dataset'[PhoneService]),'01 Churn-Dataset'[Churn]="Yes"),0) 
### [2] Percentage Of Streaming Tv %
        DIVIDE(CALCULATE(COUNT('01 Churn-Dataset'[StreamingTV]),'01 Churn-Dataset'[StreamingTV]="Yes",'01 Churn-Dataset'[Churn]="Yes"),CALCULATE(COUNT('01 Churn-Dataset'[StreamingTV]),'01 Churn-Dataset'[Churn]="Yes"),0)
### [3] Percentage Of Streaming movies %
        DIVIDE(CALCULATE(COUNT('01 Churn-Dataset'[StreamingMovies]),'01 Churn-Dataset'[StreamingMovies]="Yes",'01 Churn-Dataset'[Churn]="Yes"),CALCULATE(COUNT('01 Churn-Dataset'[StreamingMovies]),'01 Churn-Dataset'[Churn]="Yes"),0
### [4] Percentage Of DeviceProtection %
        = DIVIDE(CALCULATE(COUNT('01 Churn-Dataset'[DeviceProtection]),'01 Churn-Dataset'[DeviceProtection]="Yes",'01 Churn-Dataset'[Churn]="Yes"),CALCULATE(COUNT('01 Churn-Dataset'[DeviceProtection]),'01 Churn-Dataset'[Churn]="Yes"),0) 
### [5] Percentage Of online backup %
        DIVIDE(CALCULATE(COUNT('01 Churn-Dataset'[OnlineBackup]),'01 Churn-Dataset'[OnlineBackup]="Yes",'01 Churn-Dataset'[Churn]="Yes"),CALCULATE(COUNT('01 Churn-Dataset'[OnlineBackup]),'01 Churn-Dataset'[Churn]="Yes"),0)
### [6] Percentage Of security %
        DIVIDE(CALCULATE(COUNT('01 Churn-Dataset'[OnlineSecurity]),'01 Churn-Dataset'[OnlineSecurity]="Yes",'01 Churn-Dataset'[Churn]="Yes"),CALCULATE(COUNT('01 Churn-Dataset'[OnlineSecurity]),'01 Churn-Dataset'[Churn]="Yes"),0)
### [7] Percentage Of Tech support %
        DIVIDE(CALCULATE(COUNT('01 Churn-Dataset'[TechSupport]),'01 Churn-Dataset'[TechSupport]="Yes",'01 Churn-Dataset'[Churn]="Yes"),CALCULATE(COUNT('01 Churn-Dataset'[TechSupport]),'01 Churn-Dataset'[Churn]="Yes"),0)


Also; Pie chart helped us in a calculation where we've got the division between Internet Service and count of internet service  Where Fiber optics users are 69.40% & DSL users 25.56%.  



## CUSTOMER RISK ANALYSIS
![Risk anaylsis](https://github.com/user-attachments/assets/c6fde3d7-2fa2-4ffa-9955-3ab2a1980f46)

# Single page report was created on Power BI Desktop & it was then published to Power BI Service.

Following inferences can be drawn from the dashboard;


### [CARD] Total Customer by selecting CustomerID dataset
### [CARD] Churn Rate %
        DIVIDE (CALCULATE(COUNT('01 Churn-Dataset'[Churn]), '01 Churn-Dataset'[Churn] = "yes" ),CALCULATE ( COUNT ('01 Churn-Dataset'[Churn]), ALLSELECTED ('01 Churn-Dataset'[Churn] ) ))

### [Gauge] Count of Churn for Yes = 
        CALCULATE(COUNTA('01 Churn-Dataset'[Churn]), '01 Churn-Dataset'[Churn] IN { "Yes" })
### [Multi Row Card] created by adding Admin Tickets and tech tickets from the dataset shared us the total Number of tickets.

  ![KPI 2](https://github.com/user-attachments/assets/84b91072-20b8-4a49-a8f0-d65dd7fa81d0)

  ### Few Slicers Added to the Churn Column (Left Row) in the Filter Widgets to Enhance Filtering Capabilities
[Slicer] Risk of Churn: This slicer provides Yes/No options to filter data based on whether customers are identified as at risk of churn. It allows users to easily view and analyze data related to high-risk and low-risk customers.

[Slicer] Internet Service: This slicer includes options such as DSL, Fiber Optics, and No Internet Service. It helps in filtering the data by the type of internet service, making it easier to compare churn rates and other metrics across different types of internet services.

[Slicer] Months Subscribed: This slicer features a range from 0 to 72 months, with a slider for adjusting the date range. It simplifies filtering customers based on their subscription duration, providing flexibility to view data for specific periods.

[Slicer] Contract Type: This slicer includes options for Monthly, Yearly, and Two-Year contracts. It assists in analyzing how different contract types affect customer behavior and churn rates, and helps to identify preferences for contract durations.

***************************************************

Churn by type of internet (Clustered column Chart)

       X Axis  - internet Service + Y Axis Churn rate %

Customers by Internet Service (Pie Chart)

       Legend(internet Service) + Values (Count of customerID)

Sum of monthly charges (Pie Chart)

       Legend(internet Service) + Values (Sum Of monthly charge)   

Type of Contract (Line and Cluster column chart)

       X Axis(Contracts) + Column Y Axis (Churn rate %) + Line Y - Axis(Count of customer)

Year of Contract (Line and Cluster column chart)

       X Axis(Tenure) + Column Y Axis (Churn rate %) + Line Y - Axis(Sum of monthly charge)
 


Snippet :

I strengthened my PowerBI skills to better understand clients and their data visualisation needs.
Demonstrated expertise in data visualization through the creation of Power BI dashboards that effectively conveyed KPIs, showcasing the ability to respond to client requests with well-designed solutions.
Strong communication skills reflected in the concise and informative email communication with engagement partners, delivering valuable insights and actionable suggestions based on data analysis.
Leveraged analytical problem-solving skills to examine HR data, particularly focusing on gender-related KPIs, and identified root causes for gender balance issues at the executive management level, highlighting a commitment to data-driven decision-making.
