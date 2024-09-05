# Customer Retention (PhoneNow)

### Dashboard Link : 

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

 

# Insights

# single page report was created on Power BI Desktop & it was then published to Power BI Service.

Following inferences can be drawn from the dashboard;


Part 1 - ###Demographic###

### [1] Card Created to distribute Agents, Where Customer ID Minus where churn data is yes = 1869 (Customer At risk) 
   
thus, Customer ID - Churn data (yes) = 1869.

     
        DAX %       
### [A] Percentage Of seniors
        Percentage Of seniors = DIVIDE(CALCULATE(COUNT('01 Churn-Dataset'[SeniorCitizen]), '01 Churn-Dataset'[SeniorCitizen]=1, '01 Churn-Dataset'[Churn]="Yes"), CALCULATE(COUNT('01 Churn-Dataset'[SeniorCitizen]),'01 Churn-Dataset'[Churn]="Yes"),0) 
    
### [B] Partner in Percentage
        Partner in %Percentage = DIVIDE(CALCULATE(COUNT(churn[Partner]), churn[Partner]="Yes", churn[Churn]= "Yes"), CALCULATE(COUNT(churn[Partner]), churn[Churn]="Yes"),0) 

### [C] Dependents in Percentage
        DIVIDE(CALCULATE(COUNT('01 Churn-Dataset'[Dependents]), '01 Churn-Dataset'[Dependents]="Yes"), CALCULATE(COUNT('01 Churn-Dataset'[Dependents]), '01 Churn-Dataset'[Churn]="Yes"),0) 

  
### [2] Subscription time
New column has been edited, By Transforming data and Giving Conditional column to the Visualization 

 
![Subscription time](https://github.com/user-attachments/assets/8df0d709-1c42-4479-8fc3-8c60e25f1df5)



Part 2 - ###Payment Method###

### [1] Cluster Bar Chart Created to distribute Payment Method, where Electronic checks are the highest mode of payments by clients, countniued by email check , bank transefer & credit  ard


### [2] Donut Chart supported to sagregate paperless billing where we have found out 25.09% People do not use paperless billing where in 74.91 people use paperless billing as a payment method.

### [3] Multi row card supported us with total average charges client pays on monthly bases is 74.44 per month with a average total of 1531.80 in total;


### [4] Clustered bar Chart played an important to create (Payment method Table), with the help of contracts in Y axis and selecting percent of grand total (COUNT) we've got 3 rows
Month-to-month - 88.55%
one Year - 8.88%
Two Year - 2.57%



Part 3 - ###Services Customer signed Up for ###

7 Power Queries has been added to the dax to created complicated CALCULATive percentage system

![Percentage of Subscription](https://github.com/user-attachments/assets/d55b72f7-3099-4ed7-b6ea-fa5c2912c113)

Each one has its own uniquie and fundamental importance/
      
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


        
        
