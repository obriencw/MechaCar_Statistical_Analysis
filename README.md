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
![t-test suspension](/t_test.PNG)

## Study Design: MechaCar vs Competition