# Amazon_Vine_Analysis

## Overview

Since your work with Jennifer on the SellBy project was so successful, you’ve been tasked with another, larger project:
analyzing Amazon reviews written by members of the paid Amazon Vine program. The Amazon Vine program is a
service that allows manufacturers and publishers to receive reviews for their products. Companies like SellBy pay a
small fee to Amazon and provide products to Amazon Vine members, who are then required to publish a review.
In this project, you’ll have access to approximately 50 datasets. Each one contains reviews of a specific product, from
clothing apparel to wireless products. You’ll need to pick one of these datasets and use PySpark to perform the ETL
process to extract the dataset, transform the data, connect to an AWS RDS instance, and load the transformed data into
pgAdmin. Next, you’ll use PySpark, Pandas, or SQL to determine if there is any bias toward favorable reviews from Vine
members in your dataset. Then, you’ll write a summary of the analysis for Jennifer to submit to the SellBy stakeholders.

## Deliverables:
- Perform ETL on Amazon Product Reviews
- Determine Bias of Vine Reviews
- A Written Report of the Analysis

## Resources
- PySpark, AWS RDS, pgAdmin, Google Colaboratory, Postgres, SQL, Jupyter Notebook

## Results

This dataset had well over 3 million recorded reviews.  To filter down this dataset into a more manageable size we used the following filters:
- Count of total vottes equal or greater than 20
- Percent of helpful votes to total votes equal or greater than 50%

This reduced the total number of reviews in the dataset to 50.7k, allowing us to answer specific questions.

### 1. How many Vine reviews and non-Vine reviews were there?
- Vine members made up only 2.1% (1080) of the reviews, and the remaining 97.9% were from non-vine members (49,659)

<img width="1000" alt="ratings total" src="https://user-images.githubusercontent.com/104927745/193429235-acf37175-7a04-46ad-8d7e-92d72b58315c.PNG">

<img width="1000" alt="non paid" src="https://user-images.githubusercontent.com/104927745/193429233-c000217e-4a79-43e4-8c5b-eb233f366774.PNG">

<img width="1000" alt="percent votes" src="https://user-images.githubusercontent.com/104927745/193429234-908566bd-beb3-4c1d-877c-90cf0b9ec301.PNG">

### 2. How many Vine reviews were 5 stars?  How many non-vine reviews were 5 stars?
- Vine members gave 454 out of 1,080 reviews with a 5 star rating
- While non-vine members gave 23,034 out of 49,659 a 5 star rating

### 3. What percentage of Vine reviews were 5 stars?  What percentage of non-vine reviews were 5 stars?
- 42% of Vine member reviews were rated as 5 stars
- Whereas 46.4% of the reviews for non-vine members were rated as 5 stars

## Summary

In looking at these results, Vine members did not show any significant bias towards their products.  We can thus infer that Vine customers might be slightly more critical when submitting their reviews as compared to non vine-members.  This is an assumption which would require further analysis of the data as a whole, versus starting out by filtering it by "helpful" vs "total votes".  
