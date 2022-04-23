# Amazon_Vine_Analysis

## Overview

### Purpose

This project was intended to analyze Amazon reviews written for digital video game purchases by memebers of the Amazon Vine paid program. PySpark was utilized to perform th ETL process while connecting to an AWS RDS instance and loading data into pgAdmin. PySpark, Pandas, and SQL were used in this project but a focus was placed on PySpark to determine if there is any bias toward favorable reviews from Vine members in the dataset. This was done to form a report to send to stakeholders. 

## Results

![count](https://user-images.githubusercontent.com/94864663/164930952-842abb91-0405-41d3-971c-5ced38e0a0c6.png)

- A total count reveals that there were 0 Vine reviews in the data for digital video game purchases with 145,431 non-Vine reviews. 



- Therfore, filtering for reviews where toal votes is equal to or greater than 20 shows 0 Vine reviews and 3,342 non-Vine reviews. 

![count2](https://user-images.githubusercontent.com/94864663/164932099-7e4a23df-e1c1-47aa-81a1-41e291949ca1.png)

- Of these results, 1685 non-Vine reviews were voted helpful by the majority, meaning that the ratio of votes for being helpful and the total votes the review got was over 50%. 

- Of these non-Vine reviews, 631 were 5-star reviews, meaning about 37.4% of non-Vine majority helpful reviews with 20 or more votes were 5-star reviews. With no Vine reviews it is difficult to compare the Vine and non-Vine reviews. 

![sum](https://user-images.githubusercontent.com/94864663/164932563-1e3afef4-a3f2-499c-837a-83fbf9d65fde.png)



## Summary

Looking at the data for digital video game purchases, the data does not show any reviews from the Vine program therefore it is not possible to compare the Vine and non-Vine reveiws accurately. While there is no bias towards reviews in the Vine program, the data shows a severe bias for non-Vine reviews considering only non-Vine reviews were found in the data. 

With a larger data set icluding at least some paid Vine reviews we can perform an analysis of means and determine if a bias exists statisically using a t-test. In the test, the number of total reviews, number of those reviews being 5-stars, and the percentages can all be compared between unpaid and paid reviews. For an example, looking at just the percentages of 5-star reivews, we could test a null hypothesis claiming there will be no differnec between the percentage of non-Vine 5-star reviews and Vine 5-star reviews. If there was a bias for either, we would need to determine if it is statistically signigicant before we reject the null and claim a bias. 
