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

### [1] Cluster Bar Chart Created to distribute Payment Method, where Electronic checks (57%) are the highest mode of payments by clients, continued by email check (16%), bank transfer (14%) & Credit Card (12%).

### [2] Donut Cart identifies Amoung paperless billing 74.91% people chose this mode of payment and 25.09% people prefered not to chose paperless billing.

### [3] Stacked Bar Chart Showes hightest mode of subscription is Month-To-Month 88.55%, 8.88% prefer yearly subscription and only 2.57% People chosen Two year subscription.

### [4] Added a card to to show case Average Monthly charge, charged by Phonenow is $ 74.44 where total average amount to a customer is $1531.80








        
