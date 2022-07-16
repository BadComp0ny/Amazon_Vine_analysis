# Amazon_Vine_Analysis
Growing as a Data Science Analyst with ETL, Pyspark, AWS RDS and pgAdmin.

![image1](/Images/AVR.png)

## Overview
The purpose of this module was to utilize existing skills to begin the ETL process on big data and identify if the Amazon Vine Reviewer program results in a skewed number of positive reviews.
The tasks assigned to each student was as follows.
- Choose one category from a list of provided categories to compile reviews and create a database of all reviews for the selected category.
- Create a multiple Dataframes using this information
- Load the DataFrames to pgAdmin
- Utilize pySpark to extract the same data
- Recreate the tables loaded to pgAdmin in pySpark
- compile tables to better identify if this review process is skewed.
- Analyze the data and create a written review

## Results
I initially compiled the data and performed analysis on the Digital Video Games category and found that everything worked until it came tile to identify vine reviews for this category.  At this time it was found that out of all of the reviews there were no vine reviews for this product.  Naturally this would result in no skewing of the data but in an effort to better perform the analysis I went back and chose the pet product reviews. Prior to completing the first set of work I validated that there were vine reviews for this section and found over 10,000 vine reviews for this product.

- Initial count of reviews = 2.6M
- Initial count of Vine reviews = 10,615

I then limited the review to only look at items with a review total in excess of 20 total votes and then further refined this list to include only ones where over half of the votes had been identified as helpful.
IMAGE
This reduced the total population of reviews to 38,010.

Of the remaining reviews the breakdown was as follows

**Paid Reviews** = 170

**Non-Paid Reviews** = 37,840

**Paid 5-Star reviews** = 65

**Non-Paid Reviews** = 20,612

**% of Paid 5-Star Reviews** = 38.24%

**% of Non-Paid 5-Star Reviews** = 54.47%
