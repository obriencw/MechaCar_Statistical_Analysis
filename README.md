# MechaCar_Statistical_Analysis

For this analysis, we utilized RStudio to perform retrospective analysis of historical data, analytical verification and validation of current automotive specifications and study design of future product testing for a new protype vehicle called MechaCar.  In this analysis, we chose to focus on the following areas:
- Identify which variables in the dataset predict the the mpg of MechaCar prototypes
- Collect summary statistics on the pounds per square inch (PSI) of the suspension coils from the manufacturing lots.
- Determine if the manufacturing lots are statistically different from the mean population.
- Compare vehicle performance of the MechaCar vehicles against vehicles from other manufacturers.
## Linear Regression to Predict MPG
Using RStudio, we were able to design a linear model that predicts the mpg of MechaCar protypes using the following variables: vehicle length, vehicle weight, spoiler angle and ground clearance.  When we analyze the summary statistcs from our linear model in the chart below, we are particularly concerned with the p-value which is represented by "Pr(>|t|)".  Of the variables analyzed, vehicle length and ground clearance had p-values that were considered unlikely to provide random amounts of variance meaning that both factors had a significant impact on mpg while vehicle weight and spoiler angle did not.  In this analysis, the slope of the linear model is not considered to be 0 because the p-value of the f-statistic was 5.35e-11.  Because the multiple R-squared value from our model is 0.7149 this means that our model accurately predicts mpg of MechaCar prototypes 71.49% of the time so we would claim that our model does accurately predict the mpg of MechaCar protypes.
![Summary Linear Model](/Summary_MechaLm.PNG)


## Summary Statistics on Suspension
The MechaCar design specifications for their suspension coils dictate that the variance of the suspension coils must not exceed 100 PSI.  To determine if MechaCars design specifications were being met, we used RStudio to create summary statistics from the data we had on MechaCars suspension coils to produce the charts below.  These charts display the variance in the PSI for each different manufacturing lot individually and all manufacturing lots combined respectively.  When we analyze the lot summary chart, we can see that both Lot1 and Lot2 are will under the 100 PSI threshold in variance at 0.98 PSI and 7.47 PSI respectively, which meets the design specifications of MechaCar.  On the other hand, Lot3 is well over the 100 PSI threshold at 170.29 PSI and fails to meet the design specifications for MechaCar.  
![Lot Summary](/lot_summary.PNG)

However, when we analyze the total summary chart we can see that when we combine the suspension coil data from all three manufacturing lots, the total variance is 62.29 PSI, which meets the design specifications for MechaCar.

![Total Summary](/total_summary.PNG)


## T-Tests on Suspension Coils
When we perform a t-test on our suspension coil data for all manufacturing lots we see that we get a p-value of 0.06.  Since this number is higher than our significance level of 0.05, we claim that there is no statistical difference in the population mean of 1500 PSI.
![t-test suspension](/t_test.PNG)

When we perform a t-test on each individual manufacturing lot, we get varying results.  Lot 1 had a p-value of 1 which means this particular manufacturing lot is not statistically different from the population mean of 1500 PSI.  This data is supported by our previous analysis where we found that Lot 1 had the lowest variance in PSI of all the manufacturing lots.
![Lot 1 T-test](/lot1_ttest.PNG)

Looking at Lot 2, we see that the p-value was higher than that of Lot 1 but still above our 0.05 significance level so we claim that the PSI for Lot 2 is not statistically different from the population mean.

![Lot 2 T-test](/lot2_ttest.PNG)

Examining Lot 3 reveals a p-value of 0.04 which is less than our 0.05 significance level which indicates that the PSI of the suspension coils manufactured on Lot 3 are statistically different from the population mean of 1500 PSI.  This is also supported by our earlier analysis which showed that Lot 3 had a much higher variance than Lot 1 and Lot 2.
![Lot 3 T-test](/lot3_ttest.PNG)

## Study Design: MechaCar vs Competition
When considering the potential that the MechaCar prototype could have on the consumer market, we would want to consider how the MechaCar vehicles perform against vehicles of other manufacturers.  One thing that we believe is important to car buyers is having a vehicle that gets good miles per gallon (mpg).  Nobody likes stopping at the gas pump more than they have to and and vehicles with higher mpg are better more environmentally friendly.  To test this, we would like to compare vehicle sales of vehicles with similar class, and engine size to the MechaCar vehicle.  For this test, our metrics would be the city mpg of the of the mpg ratings of the other manufacturer's vehicles.  In this case, our null hypothesis would be that the city mpg rating has no affect on vehicle sales.  The test we would like to use in this case is a linear regression model and the data we would need to complete this test is the city mpg rating of competing vehicle manufacturers as well as the total sales figures for those vehicle models.