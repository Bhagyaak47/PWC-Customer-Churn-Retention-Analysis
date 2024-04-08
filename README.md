# PwC-Customer-Retention-and-Churn-Analysis

PwC Power BI Virtual Case Experience Task 2- Customer Retention and Churn Analysis Dashboard

# Problem Statement  
  
In this project Create a dashboard in Power BI for the PhoneNow Company that reflects the Churn analysis and Customer Information for further decision making and strategies for customer retention. The telecom Retention Manager has scheduled a meeting with the engagement partner at PwC to cover these points:

- Customers in the telecom industry are hard-earned: we don’t want to lose them
- The retention department is here to get customers back in case of termination
- Currently, we get in touch after they have terminated the contract, but this is reactionary: it would be better to know in advance who is at risk
- We have done customer analysis with Excel: it has always ended in a dead-end  
- We would like to know more about our customers: visualised clearly so that it’s self-explanatory for our management.

# Dataset:

The dataset used for this task was presented by https://www.theforage.com

#  DAX Formulas: 
- % Churn Rate = DIVIDE(CALCULATE(COUNT(Churn[Churn]),Churn[Churn]="Yes"),COUNT(Churn[Churn]),0)
- % of Senior Citizen = DIVIDE(CALCULATE(COUNT(Churn[SeniorCitizen]),Churn[SeniorCitizen]=1,Churn[Churn]="Yes"),CALCULATE(COUNT(Churn[SeniorCitizen]),Churn[Churn]="Yes"),0)
- % Dependants = DIVIDE(CALCULATE(COUNT(Churn[Dependents]),Churn[Dependents]= "Yes",Churn[Churn]="Yes"),CALCULATE(COUNT(Churn[Dependents]),Churn[Churn]="Yes"),0)
- % Partner = DIVIDE(CALCULATE(COUNT(Churn[Partner]),Churn[Partner]="Yes",Churn[Churn]="Yes"),CALCULATE(COUNT(Churn[Partner]),Churn[Churn]="Yes"),0)
- % Phone Service = DIVIDE(CALCULATE(COUNT(Churn[PhoneService]),Churn[PhoneService]="Yes",Churn[Churn]="Yes"),CALCULATE(COUNT(Churn[PhoneService]),Churn[Churn]="Yes"),0)
- % Tech Support = DIVIDE(CALCULATE(COUNT(Churn[TechSupport]),Churn[TechSupport]="Yes",Churn[Churn]="Yes"),CALCULATE(COUNT(Churn[TechSupport]),Churn[Churn]="Yes"),0)
- % Streaming TV = DIVIDE(CALCULATE(COUNT(Churn[StreamingTV]),Churn[StreamingTV]="Yes",Churn[Churn]="Yes"),CALCULATE(COUNT(Churn[StreamingTV]),Churn[Churn]="Yes"),0)
- % Online Security = DIVIDE(CALCULATE(COUNT(Churn[OnlineSecurity]),Churn[OnlineSecurity]="Yes",Churn[Churn]="Yes"),CALCULATE(count(Churn[OnlineSecurity]),Churn[Churn]="Yes"),0)
- % Online Backup = DIVIDE(CALCULATE(COUNT(Churn[OnlineBackup]),Churn[OnlineBackup]="Yes",Churn[Churn]="Yes"),CALCULATE(COUNT(Churn[OnlineBackup]),Churn[Churn]="Yes"),0)
- Device Protection = DIVIDE(CALCULATE(COUNT(Churn[DeviceProtection]),Churn[DeviceProtection]="Yes",Churn[Churn]="Yes"),CALCULATE(COUNT(Churn[DeviceProtection]),Churn[Churn]="Yes"),0)
- % Yes-Multiple Lines = DIVIDE(CALCULATE(COUNT(Churn[MultipleLines]),Churn[MultipleLines]="Yes",Churn[Churn]="Yes"),CALCULATE(COUNT(Churn[MultipleLines]),Churn[Churn]="Yes",Churn[MultipleLines]<> "No phone service"),0)
- % No- Multiple lines = DIVIDE(CALCULATE(COUNT(Churn[MultipleLines]),Churn[MultipleLines]="No",Churn[Churn]="Yes"),CALCULATE(COUNT(Churn[MultipleLines]),Churn[Churn]="Yes",Churn[MultipleLines]<> "No phone service"),0)


# Data Cleaning/ Preparation:

- The data consists of over 7000 rows and 23 columns.
- Divided the tenure(in months) to different groups in years such as 0-1 year, 2-3 years etc
- Loaded the dataset in PowerBI and the remaining dataset was clean enough to perform the analysis directly.


# Questions to be answered :
- Customers who left within the last month
- Services each customer has signed up for phone, multiple lines, internet, online security, online backup, device protection, tech support, and streaming TV and movies
- Customer account information: how long as a customer, contract, payment method, paperless billing, monthly charges, total charges and the number of tickets opened in the categories of administrative and technical
- Demographic info about customers – gender, age range, and if they have partners and dependents.

![PWC Customer Churn_001](https://github.com/Bhagyaak47/PWC-Customer-Churn-Retention-Analysis/assets/152842490/4ecc2c6f-94f2-4cbd-9207-375d4d3da85e)

![PWC Customer Churn_002](https://github.com/Bhagyaak47/PWC-Customer-Churn-Retention-Analysis/assets/152842490/02cc916a-025b-421d-84eb-e30851c408af)


# Insights :

- The customer information report is filtered by whether we want the churned customers or total customers.
- Total customers are 7083 out of which 1869 are churned customers. The churn rate is 26.5% which has to be reduced further.
- We have retained 73.5% of our customers where the total monthly charges are almost 455K and yearly charges are 16M.
- The total tech tickets issued are 2955 and the total admin tickets raised are 3632.
- There are a total of 3058 tech and admin tickets combined which are raised by the churned customers. The company should look into that to solve the issues in the services to retain the customers in the future.
- Gender distribution doesn't play an important role in the churn rate as they are almost equal.
- Marital status and dependency don't have any major impact on the churn rate.
- There are majority customers in the 0-1 tenure bracket i.e. majority customers have purchased the monthly packages which can also be seen in the contract where month-to-month contracts are almost 55% percent.
- Also, the month-to-month churn rate is almost 42% whereas it is the lowest for 2-year contracts.
- As monthly customers are more, evidently the monthly charges are also the highest.
- But the total charges of two-year contracts are the highest mainly because of the low churn rate and high monthly leaving customers.
- 54% of churn customers purchased the monthly packages.
- Also, most of our customer target is young people who comprise most of our customer age groups.
- 2.86 M revenue was lost due to the churn rate.
- Also, we lost 380 customers last month.
- A large percentage i.e. 90% of the churning customers have a phone service therefore phone service should be checked for any issues.
- Streaming services don't have much impact on the churn rate.
- Majority of the churned customers did not subscribe to services like online backup(28%), security(16%) and Tech support(17%).

  # Recommendations
- Most of the billing was done in a paperless way i.e. our online transactions systems have to be in good condition at all times.
- Those who paid by electronic check comprised of most churned customers therefore the electronic payment method and its tickets should be checked to identify the issues and resolve them which can help to retain the customers in the long run.
- A large percentage i.e. 90% of the churning customers have a phone service therefore phone service should be checked for any issues.
- We can encourage the customers who have brought internet services via fiberoptic and DSL to purchase services like online backup, security and Tech support to retain them.
- We can define some monthly or quarterly schemes to retain the monthly churned customers.


