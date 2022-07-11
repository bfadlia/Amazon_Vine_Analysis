# Amazon_Vine_Analysis

## Overview

In this project we check Amazon US Book reviews. We are trying to analyze if subscribing to a Vine program will be helpful. The vine review program is an incentive model in which customers are gifted free stuff when they write good reviews. We used PySpark for the ETL step of the data to an AWS RDS. Some transformation was done on the data in PySpark. Then I exported the vines data as CSV file and performed additional analysis in Jupyter Notebook.




## Results

- The conditions of having 20 total reviews and half of these reviews helpful to be included in the dataset resulted in an empty dataset regarding paid vine custormers in the book reviews data. 

- Paid Vine reviews
  - 0 reviews satisfy the 20+ reviews with half of them being helpful
  - Of course there are no 5 star reviews either in that dataset
  - Percentage of five star reviews in this subset can't be calculated or we'll have division by zero problem

- Unpaid reviews
  - 403,807 total reviews
  - 242,889 5-star reviews
  - Approximately 60.15% of unpaid reviews were 5-star

- ![IMAGE_DESCRIPTION](/Images/output.png)

## Summary

- In conclusion, when looking at book reviews dataset, all customers who used the paid Vine program did not satisfy the inclusion criteria of the dataset of having at least 20 reviews and having at least half of those being helpful reviews. This prevented meaning comparison of different counts between paid and unpaid reviews as the paid side was always zero and its percentage calculation would have resulted in division by zero

- On the unpaid side, more than 60% of the reviews were favorable 5 stars.

- To have more meaningful comparison between the paid and unpaid reviews, I experimented with changing the inclusion criteria requiring only one review instead of the minimum 20 and not limiting by weather it was helpful or not. However I still got only two paid reviews, one of which was 5 stars. It was still not reasonable to draw any conclusions based on such a tiny sample. I will continue with the conclusion that the Vine program subscription is irrelevant when evaluation book reviews.

- Below is a snapshot of the additional analysis when I changed the inclusion criteria

- ![IMAGE_DESCRIPTION](/Images/output2.png)

