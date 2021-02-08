# Amazon_Vine_Analysis
----------------------------------------------------------------------------------

## Overview
Perform retrospective analysis on historical data, analytical verification of current automotive specifications and study design of future auto testing.  

## Data Sources and Coding File
Data for analysis was provided in two csv files ([MPG](MechaCar_mpg.csv) and [Suspension](Suspension_Coil.csv)).  

https://s3.amazonaws.com/amazon-reviews-pds/tsv/amazon_reviews_us_Video_Games_v1_00.tsv.gz

## Results

![Fig_1](Vine_Summary_DF.PNG)

Performed a multiple linear regression to determine the effect of the following 5 measured variables on fuel efficiency (measured in mpg): vehicle length, vehicle weight, spoiler angle, ground clearance and drive train (AWD or not).  

The best-fit model is described by the following:  MPG = 6.267xvehicle_length + 0.001245xvehicle_weight +0.06887xspoiler_angle 3.546xground_clearance - 3.411xAWD - 104.

Analyzing the model's coefficients (inputs), we find that vehicle length and ground clearance have a statistically significant impact on fuel economy (MPG).  Therefore, with this knowledge, we know the slope of the model is not zero because the individual contributors to the model's slope (6.267xvehicle_length and 3.546xground_clearance) are significant and non-zero.  

Although, the analysis with 5 predictors does model fuel economy fairly well (r-squared = 0.7149), it appears the model is not complete.  It is likely that other unmeasured predictors (variables) contribute to fuel economy as well.  

## Summary

![Fig_2](MechaCar_Statistical_Analysis/Screenshots/Suspension_central_tendancy.PNG)

The design specifications for the MechaCar suspension coils dictate that the variance of the suspension coils must not exceed 100 psi. The above analysis demonstrates that, with a variance of 62.29 psi, the aggregate falls within design specification.  


![Fig_3](MechaCar_Statistical_Analysis/Screenshots/Suspension_by_Lot.PNG)

Both Lot 1 and 2 meet design specification.  However, Lot 3 is well outside suspension coil specification with a variance of 170.29 psi (> 100 psi).  

## T-Tests on Suspension Coils

![Fig_4](MechaCar_Statistical_Analysis/Screenshots/ttest_PSI_allLots.PNG)

