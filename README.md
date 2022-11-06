# Amazon_Vine_Analysis

## Overview
### This project looks at reviews for video games.  The purpose was to determine if there was any bias from paid reviews to give 5 star ratings.  I used Pyspark to import data and filtered into several tables then written in a SQL database.  I then focused on 1 table containing all the review information for the video games and the ratings given.  From this data I calculated the following:
•	Number of total reviews
•	Number of 5 star rating reviews, both paid and unpaid
•	Percentage of 5 star ratings to both total reviews and total 5 star reviews for both paid and unpaid.
### To get these numbers I created the following dataframes
### Total Votes – greater than or equal to 20

![total_votes_dataframe](https://user-images.githubusercontent.com/106286533/191333542-416f8424-483f-4fa7-9eab-a797d3309432.png)

### Helpful Votes – filtered the total votes dataframe where the percentage of helpful votes was greater than or equal to 50%

![helpful_votes_dataframe](https://user-images.githubusercontent.com/106286533/191333610-6d5233f5-abe6-46e7-9b12-97ce054b213e.png)

### Paid – filtered the helpful votes dataframe where a review was written as part of the vine program

![paid_reviews_dataframe](https://user-images.githubusercontent.com/106286533/191333669-9f6d3171-2021-42ac-81b0-c1f92f7a89e3.png)

### Unpaid - filtered the helpful votes dataframe where a review was written but not part of the vine program

![unpaid_reviews_dataframe](https://user-images.githubusercontent.com/106286533/191333711-61223062-1571-44d2-93b7-1f45f84c8f3c.png)


## Results
### The dataframe I focused on was for all reviews both vine(paid) and non-vine(unpaid).

![vine_dataframe](https://user-images.githubusercontent.com/106286533/191333768-f3de1b0e-ed5d-4b14-9b50-4f100c3f778f.png)

•	There were 1,785,997 total reviews written and of those only 4,291 were Vine review and the remaining 1,026,924 were Non-Vine reviews.  

![bullet1](https://user-images.githubusercontent.com/106286533/191333845-608da77b-43f4-4443-8fcc-65df06126ab2.png)

•	There were 1,026,924 5 star rating reviews.  Vine reviews had 1,607 5 star ratings and Non-Vine had 1,025,317.

![bullet2](https://user-images.githubusercontent.com/106286533/191333878-35de698b-b5e7-4867-90d3-5e9c812ea856.png)

•	37% of submitted Vine Reviews were 5 star ratings.

![bullet3](https://user-images.githubusercontent.com/106286533/191334129-b4d15ac1-4510-401b-bac1-3e8415c01b73.png)

•	57.54% of submitted Non-Vine Reviews were 5 star ratings.

![bullet4](https://user-images.githubusercontent.com/106286533/191334179-50f0491d-ff93-49e0-86e3-cb789d770983.png)


## Summary
### Based on the results of my analysis I do not believe the Vine program has any positivity bias.  A larger percentage of Non-Vine users gave 5 star ratings on their reviews than Vine users.  In addition, I would suggest using the .describe() function to analyze and plot the Vine and Non-Vine reviews.  Using the key features such as mean, median, mode and upper/lower quartiles could show if our results have merit.
