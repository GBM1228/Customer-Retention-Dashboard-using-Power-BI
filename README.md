# PwC Switzerland Power BI Job Simulation on Forage-Customer Retention

<img width="651" alt="2024-09-16 (1)" src="https://github.com/user-attachments/assets/53f87fe3-9e06-4232-a495-eaa248a91440">


As  my 4th and final task for the Virtual Internship on Power BI from PwC, I have design a dashboard focused on Customer Retention.
As a Data Analyst, my role was to Define proper KPIs, Create a dashboard for the retention manager reflecting the KPIs, 
Write a short email to him (the engagement partner) explaining my findings, and include suggestions as to what needs to be changed

## Table Of Contents

[Problem Statement](#ProblemStatement)

[Data Sourcing](#DataSourcing)

[Data Preparation](#DataPreparation)

[Data Visualization](#DataVisualization)

[Data Analysis](#DataAnalysis)

[Insights](#Insights)

[Recommendation](#Recommendation)

## Problem Statement

The purpose of this analysis is to:

1. Define proper KPIs

2. Create a dashboard for the retention manager reflecting the KPIs
3. Write a short email to him (the engagement partner) explaining my findings, and include suggestions as to what needs to be changed

## Data Sourcing

The Dataset used for this analysis was given by [Pwc switzerland](https://www.pwc.ch/en/careers-with-pwc/students/virtual-case-experience.html)


[Dataset](https://github.com/user-attachments/files/17015869/02.Churn-Dataset.xlsx)

## Data Preparation

Data transformation was performed using Power Query, followed by loading the refined dataset into Microsoft Power BI Desktop for in-depth analysis and reporting.

The dataset for diversity and inclusion has 24 columns and 7,044 rows.

|Column Name|
|---|
|customerID	|
|Gender|
|SeniorCitizen|
|Partner|
|Dependents|
|Tenure|
|PhoneService|
|MultipleLines|
|InternetService|
|OnlineSecurity|
|OnlineBackup|
|DeviceProtection|	
|TechSupport|
|StreamingTV|
|StreamingMovies|
|Contract|
|PaymentMethod|
|MonthlyCharges|
|TotalCharges|
|NumAdminTickets|
|NumTechTickets|
|Churn|
|Senior Citizen (Yes/No)|

The following steps were taking for the data cleaning and transformation  :

* Promoting headers 

* Changing data types

* Replacing text values 

* Removing unnecessary columns

* Renaming Column name for clarity

## Data Visualization

Three phases was created for the Churn dataset, page1 for the Visualization, page2 & 3  for the insight and reconmendation based on the analysed churn dataset. 
Leading to a detailed and engaging visual representation:

##### Customer Retention Dashboard visulaizes the :

* Total Customer
* Total Churn
* Total Month Churn
* Churn Rate
* Total Revenue
* Total Monthly Revenue
* Churn by Services%
* Internet Service%
* Churn by Gender%
* Churn by Contract%
* Total Churn by Tenure
* Churn by Dependents%
* Churn by Payment Method%

<img width="651" alt="2024-09-16 (1)" src="https://github.com/user-attachments/assets/9a8bb4e8-8eea-4487-a9ec-9c8965a92bc9">

## Data Analysis

The measures listed below were created to track our progress towards our goals

* Total Customer = COUNT('01 Churn-Dataset'[customerID] )+0
* Total Churn = COUNTX(FILTER('01 Churn-Dataset', '01 Churn-Dataset'[Churn] = "Yes"), '01 Churn-Dataset'[customerID])+0
* Tech Support in % = DIVIDE(CALCULATE(COUNT('01 Churn-Dataset'[TechSupport]), '01 Churn-Dataset'[TechSupport]="Yes", '01 Churn-Dataset'[Churn]="Yes"),CALCULATE(COUNT('01 Churn-Dataset'[TechSupport]),'01 Churn-Dataset'[Churn]="Yes"),0)
* Streaming Tv % = DIVIDE(CALCULATE(COUNT('01 Churn-Dataset'[StreamingTV]), '01 Churn-Dataset'[StreamingTV]="Yes", '01 Churn-Dataset'[Churn]="Yes"),CALCULATE(COUNT('01 Churn-Dataset'[StreamingTV]),'01 Churn-Dataset'[Churn]="Yes"),0)
* Streaming Movies % = DIVIDE(CALCULATE(COUNT('01 Churn-Dataset'[StreamingMovies]), '01 Churn-Dataset'[StreamingMovies]="Yes", '01 Churn-Dataset'[Churn]="Yes"),CALCULATE(COUNT('01 Churn-Dataset'[StreamingMovies]),'01 Churn-Dataset'[Churn]="Yes"),0)
* Phone Service % = DIVIDE(CALCULATE(COUNT('01 Churn-Dataset'[PhoneService]), '01 Churn-Dataset'[PhoneService]="Yes", '01 Churn-Dataset'[Churn]="Yes"),CALCULATE(COUNT('01 Churn-Dataset'[PhoneService]),'01 Churn-Dataset'[Churn]="Yes"),0)
* Online Security % = DIVIDE(CALCULATE(COUNT('01 Churn-Dataset'[OnlineSecurity]), '01 Churn-Dataset'[OnlineSecurity]="Yes", '01 Churn-Dataset'[Churn]="Yes"),CALCULATE(COUNT('01 Churn-Dataset'[OnlineSecurity]),'01 Churn-Dataset'[Churn]="Yes"),0)
* Online Backup % = DIVIDE(CALCULATE(COUNT('01 Churn-Dataset'[OnlineBackup]), '01 Churn-Dataset'[OnlineBackup]="Yes", '01 Churn-Dataset'[Churn]="Yes"),CALCULATE(COUNT('01 Churn-Dataset'[OnlineBackup]),'01 Churn-Dataset'[Churn]="Yes"),0)
* Multiple lines = DIVIDE(CALCULATE(COUNT('01 Churn-Dataset'[MultipleLines]), '01 Churn-Dataset'[MultipleLines]="Yes", '01 Churn-Dataset'[Churn]="Yes"),CALCULATE(COUNT('01 Churn-Dataset'[MultipleLines]),'01 Churn-Dataset'[Churn]="Yes"),0)
* Last Month Churn = COUNTROWS(FILTER('01 Churn-Dataset', '01 Churn-Dataset'[Churn] = "Yes" && '01 Churn-Dataset'[Tenure] =1))
* Churn Rate = DIVIDE([Total Churn],[Total Customer])+0

* ## Insights

* <img width="659" alt="Customer Retention png 3" src="https://github.com/user-attachments/assets/9b4f362e-ed41-4bc1-a609-31109853ddce">

## Recommendation

<img width="672" alt="Customer Retention Png 2" src="https://github.com/user-attachments/assets/2100fcc4-b297-4c2c-ab79-f10eb2b5905c">


