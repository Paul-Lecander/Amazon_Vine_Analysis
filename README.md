## Overview
</br>

In this challenge, the company "SellBy" wants to know if the reviews left by members of the Amazon Vine program are worth the cost paid to Amazon.
The Amazon Vine program sends products to members who are then required to write reviews for said product.</br>


The goal of this challenge was to take reviews from Amazon's Vine program and perform the ETL process using PySpark.
After the transformation, the data was connected to an AWS RDS instance and subsequently uploaded into pgAdmin.
Finally, the data was analyzed using panda data frames to compare the number of five-star reviews left by members of the Vine programs and normal customers. </br>  

## Results

Some important metrics to look at when determining if SellBy should invest in the Amazon Vine program are the percentage of reviews
written by Vine reviewers and if they are the highest obtainable rating.</br>

In this dataset there was a total of 792,113 reviews and of those reviews, only a total of 8,556 reviews were rated five stars.
Out of the 8,556 five-star reviews, only 74 of those were left by members of the Amazon Vine program.</br>

This leaves the much more significant portion (99.1% or 8482 reviews) to be reviewed by those who were not part of the Amazon Vine program.</br>
![vine_fivestar](https://github.com/Paul-Lecander/Amazon_Vine_Analysis/blob/main/Images/vine_fivestar.png)</br>
![nonvine_fivestar](https://github.com/Paul-Lecander/Amazon_Vine_Analysis/blob/main/Images/nonvine_fivestar.png)</br>
![fivestar_percentage](https://github.com/Paul-Lecander/Amazon_Vine_Analysis/blob/main/Images/fivestar_percentage.png)</br>

## Summary

There is a possibility of positivity bias because reviewers got free product and could see that as a good experience because it was free; however, there was a very small subset of reviewers that were part of the Vine program.
To determine if positivity bias, there could be a query done to see how many Vine members left a review that was not five stars.
