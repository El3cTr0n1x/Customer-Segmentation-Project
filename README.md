**Data Analytics Customer Segmentation**

_Goal of the project:_

The purpose of this project is to conduct a Customer Segmentation Analysis for an Automobile bike Company. Customer segmentation is performed by developing a RFM Model. RFM (Recency, Frequency, Monetary) analysis is a behavior-based approach grouping customers into segments. It groups the customers on the basis of their previous purchase transactions. In this analysis the customer segment was divided into 11 groups. The analysis will help in determining which customers segments should be targeted in order to enhance sales revenue for the company. A Sales Dashboard for Customer Segmentation is developed using Tableau and the data quality assessment and analysis is done using Python.

Link to the tableau dashboard: https://public.tableau.com/views/BritishAirwaysReviewAnalysis_17099944735610/Dashboard1?:language=en-GB&:sid=&:display_count=n&:origin=viz_share_link

_Analysis Approach_

1. Data Quality Assessment and Data Cleaning

The first step towards generating useful insights from the data was the data prepartion, quality assessment and data cleaning step. After the cleaning process exploratory data analysis on the dataset and identification customer purchasing behaviours to generate insights can be performed.

In the data cleaning step the data quality of the following datasets were first assesed. After a data quality assessment the following data quality issues was observed and the necessary process to mitigate the issue was followed :

- CustomerDemographics.xlsx :
  
1 Irrelevent column was present and such columns were dropped from the dataset.
  
There were 5 columns were missing values were present. For such columns based on the volumne of the missing values either the records were dropped or appropiate values were imputed at places of missing values

For gender column there was no standardisation of data. Based on the values available the column data was standardised to remove data inconsistency.

The Date of Birth column was transformed to create a new feature column 'Age' and 'Age Group' to check for discrepency of age distribution. An outlier was observed and the record was removed.

Checked whether there are duplicate records present in the dataset. In this dataset there were no duplicate records.

- NewCustomerList.xlsx :

5 Irrelevent column was present and such columns were dropped from the dataset.

There were 4 columns were Missing values were present. For such columns based on the volumne of the missing values either the records were dropped or appropiate values were imputed at places of missing values

The Date of Birth column was transformed to create a new feature column 'Age' and 'Age Group' to check for discripency of age distribution.

There was no data inconsistency.

Checked whether there are duplicate records present in the dataset. In this dataset there were no duplicate records.

- Transaction_data.xlsx :

The product_first_sold_date column is not in datetime format. The data type of this column was changed from int64 to datetime format.

There were 7 columns were Missing values were present. For such columns based on the volumne of the missing values either the records were dropped or appropiate values were imputed at places of missing values

A new feature column 'Profit' was created which is basically the difference between list price and standard price.

There was no data inconsistency.

Checked whether there are duplicate records present in the dataset. In this dataset there were no duplicate records.

- CustomerAddress.xlsx :

For states column there was no standardisation of data. Based on the values available the column data was standardised to remove data inconsistency.

There were certain customer IDs from Customer Dempgraphics table which were getting dropped in the Address table.

2. Exploratory Data Analysis on Customer Segments

After the data cleaning process, exploratory analysis on the dataset is performed and the following insights are obtained :

- New vs Old Customers Age Distribution

Most New customers are aged between 40-49 also for Old Customers the most of them are aged between 40-49

The lowest number of customers for both the types of customers is present in the age bracket under 20 and above 80 age groups.

The automobile company is popular among New Customers among the age groups 20-29 and 40-49.

A steep drop in customers is observed in the 30-39 age group among the New Customers

Old Customers by Age Distribution and New Customers by Age Distribution

![image](https://github.com/El3cTr0n1x/projects-github-repo-DQA/assets/134670747/01c33ed2-a252-4e21-b414-939efcf1c7b4)  ![image](https://github.com/El3cTr0n1x/projects-github-repo-DQA/assets/134670747/fff6f301-b2d2-40e9-932e-afc1e9545a91)


     
- Bike purchases over last 3 years by Gender

Most bike puechases are done by Female over the last 3 years. Approximately 51% of the bike purchases are done by Female compared to 49% of the purchases being done by Male.

The Female purchases are 10,000 more than that of Male purchases (numerically).

![image](https://github.com/El3cTr0n1x/projects-github-repo-DQA/assets/134670747/6ad781b9-4599-4e49-810d-ce78ba5417be)


- New vs Old Customers Job Industry Distribution

Most New customers are from the Manufacturing and Financial Services sector (approx 20% of the New Customers).

The lowest number of customers are from the Agriculture and Telecom sector approx 3%.

Similar trend is observed among Old Customers as well.

![image](https://github.com/El3cTr0n1x/projects-github-repo-DQA/assets/134670747/c13a6ad0-e743-4a05-baf3-52d7bbed6b2f)  ![image](https://github.com/El3cTr0n1x/projects-github-repo-DQA/assets/134670747/904d5ffc-b843-4d17-bf05-40eb36437489)

    	
- Wealth Segmentation by Age Category

Across all age categories the largest number of customers are from 'Mass Customer' Segment

The next category comes from the 'High Net Worth' customers.

In the age group 40-49, Affluent segment out performs the High Net Worth customers in terms of number of customers.

![image](https://github.com/El3cTr0n1x/projects-github-repo-DQA/assets/134670747/5550c71d-356f-4aae-af76-a4323ffa3404)  ![image](https://github.com/El3cTr0n1x/projects-github-repo-DQA/assets/134670747/22eaef85-ef58-47b0-84c0-d195b457880c)


- Cars owned by States

New South Wales has the largest number of people who do not own a car.

In Victoria the proportion is quite even.

In Queensland the number of people owning a car is greater than who do not have a car.

![image](https://github.com/El3cTr0n1x/projects-github-repo-DQA/assets/134670747/293b1655-b99e-49ba-84f1-f2f5034f0b9e)


3. RFM Analysis and Customer Segmentation

In this stage of analysis the customer segmentation was done by developing an RFM Model. The RFM (Recency, Frequency, Monetary) analysis is a behavior-based approach grouping customers into segments. It groups the customers on the basis of their previous purchase transactions.

In this analysis the customer segment was divided into 11 groups. The groups being :

Platinum Customers

Very Loyal Customers

Recent Customers

Potential Customers

Lost Customers

Losing Customers

Late Bloomer

High Risk Customers

Evasive Customers

Becoming Loyal

Almost lost Customers

As of the current state of the Automobile business the current distribution of customers segments is depicted below: ![image](https://github.com/El3cTr0n1x/projects-github-repo-DQA/assets/134670747/cdd0f845-289d-4059-9a1e-0c219ec1a6aa)

4. RFM Analysis: Scatter Plots

Recency vs Monetary :

The visualization shows that recent customers have purchased more products and generated relatively more revenue than the customers who visited a while ago.

![image](https://github.com/El3cTr0n1x/projects-github-repo-DQA/assets/134670747/605e696b-e6c5-464b-b92d-94973ee70641)

Frequency vs Monetary :

The visualization shows that customers belonging to Platinum/ Very Loyal/ Becoming Loyal Customer Segments have a greater frequency and generate greater monetary for the business

![image](https://github.com/El3cTr0n1x/projects-github-repo-DQA/assets/134670747/5560e6a5-5d6d-4e5d-a318-763b3a593fb5)

_Conclusion_

This project aims to optimize sales strategies and marketing efforts by gaining insights from customer segmentation analysis. The developed Tableau dashboard facilitates decision-making to target specific customer groups effectively and enhance overall sales revenue.

Feel free to explore the repository to understand the analysis process and contribute to further improvements.

-Abhay

