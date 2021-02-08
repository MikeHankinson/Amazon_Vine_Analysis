# Amazon_Vine_Analysis
----------------------------------------------------------------------------------

## Overview
The Amazon Vine program is a service that allows manufacturers and publishers to receive reviews for their products. Companies pay a small fee to Amazon and provide products to Amazon Vine members, who are then required to publish a review. Two sets of Amazon video game reviews were analyzed in this study; those written by the paid Amazon Vine program subscribers and those written outside of the Vine program.   

## Data Sources and Coding File
Data for analysis was obtained from an [Amazon AWS S3 data repository](https://s3.amazonaws.com/amazon-reviews-pds/tsv/amazon_reviews_us_Video_Games_v1_00.tsv.gz).

## Analysis Methodology
Customer reviews were imported from an Amazon AWS S3 data repository into a user-specific AWS S3 account.  A database was created in pgAdmin and tied to an Amazon AWS RDS server.  Project data was extracted and transformed using a Google Colab Notebook, [Amazon_Reviews_ETL](Amazon_Reviews_ETL.ipynb).  

Using PySPark and Pandas, data was filtered, parsed and coalesced into a format to evaluate and determine if there exists a bias towards reviews written as part of the Vine program.  The evaluation was performed using a Google Colab Notebook, [Vine_Review_Analysis](Vine_Review_Analysis.ipynb). 

## Results
The figure below is the resulting Vine Summary Data Frame. Clearly, the volume of non-Vine reviews dwarfs that of those within the Vine program.  In order to determine bias, this study evaluated 5-Star reviews from within and outside the program.  With this data sample, there was a fairly significant difference of 5-Star grades for video games between the two data sub-sets.  Vine reviewers were more inclined to provide the highest rating (51.1% of reviews) as compared to non-vine reviewers (38.7% reviews). 

Further analysis should be performed for each star grade bucket (1-5) to further support the bias claim.  

 ![Sudy Summary](Vine_Summary_DF.PNG)

