# Amazon_Vine_Analysis
## Introduction
In this project we analyze Amazon reviews written by members of the paid Amazon Vine program. The Amazon Vine program is a service that allows manufacturers and publishers to receive reviews for their products. Companies like SellBy pay a small fee to Amazon and provide products to Amazon Vine members, who are then required to publish a review.We pick one of the datasets from approximately 50 datasets and use PySpark to perform the ETL process to extract the dataset, transform the data, connect to an AWS RDS instance, and load the transformed data into pgAdmin. 

## Perform ETL on Amazon Product Reviews

We use cloud ETL process, we create an AWS RDS database with tables in pgAdmin, pick a dataset from the Amazon Review datasets )and extract the dataset into a DataFrame. We transform the DataFrame into four separate DataFrames that match the table schema in pgAdmin. Then, upload the transformed data into the appropriate tables and run queries in pgAdmin to confirm that the data has been uploaded. 

<img width="1266" alt="Screen Shot 2022-04-14 at 11 50 24 PM" src="https://user-images.githubusercontent.com/72629108/163667024-18ff6342-40f6-434b-ac65-073bb413519a.png">

<img width="1266" alt="Screen Shot 2022-04-14 at 11 31 56 PM" src="https://user-images.githubusercontent.com/72629108/163667034-0cebda28-d2a1-4c8b-b865-927011eec576.png">

<img width="1266" alt="Screen Shot 2022-04-14 at 11 33 39 PM" src="https://user-images.githubusercontent.com/72629108/163667056-a8ce6d7f-bc2c-4c23-9f41-14d5e8451273.png">


<img width="1266" alt="Screen Shot 2022-04-14 at 11 42 18 PM" src="https://user-images.githubusercontent.com/72629108/163667068-5960808f-c5e8-47de-aa05-4aa04921ebe9.png">



## Determine Bias of Vine Reviews

Using PySpark, we determine if there is any bias towards reviews that were written as part of the Vine program. For this analysis, we determine if having a paid Vine review makes a difference in the percentage of 5-star reviews.

## Summary

 * Vine members made up only 0.07% (33) of the reviews whereas the remaining 96.75% were Non-Vine members (45246) and rest of the votes are anonymous.  15 Vine reviews out of 33 were 5 stars and 23639 out of 45246 non-Vine reviews were 5 stars.Reviews given by Vine members doesn't have much effect on ratings.So we can say that the reviews are not biased. 
 * 0.03% of Vine reviews were 5 stars and 50.55% of non-Vine reviews were 5 stars.
 * The percent of Paid 5 star to total Paid is 45.46 and percent of NonPaid 5 star to Total Non Paid is 55.25.Eventhough the number of vine members are not significant,the vine members did not show a bias in their reviews.
 
 
 

