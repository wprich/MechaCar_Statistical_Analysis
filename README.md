# MechaCar_Statistical_Analysis

## Linear Regression to Predict MPG

This first analysis using R took at a look at the predicting the MPG of a vehicle using variables from other cars.  These variables or data was used to create a linear model in the y = m * x + b format.  This model was saved to a variable called 'mod'.  The summary function was then used on the mod variable to get a clear and concise grouping of information ready for interpretation.

![MechaCar_MPG_LM](https://github.com/wprich/MechaCar_Statistical_Analysis/blob/main/Images/MechaCar_MPG_LM.png)

By looking at the summary statistics, we can see that the intercept is labled as 103.964, this simply tells us that, according to the data, the gas tank for most cars should last around 104 miles.  This makes sense since a car that could go 0 miles on a full tank of gas makes no sense.  Then other factors will take effect, such as the vehicles height, weight etc.  Interestly, it seems that the vehicles length has more impact than the vehicles weight when it comes to calculating the MPG.  Lastly, this model shows that we can reject our null hypothesis that our slope should be 0 since our p-value is 5.35e-11, which is significantly less than 0.05.

## Summary Statistics on Suspension Coils

The client wished to know if the variance for the suspension coils was greather than 100 lbs/inch for quality assurance reasons.  After performing the analysis utilizing the summarise function in R, we attained the data needed to make the decision.  At first glance, in the total summary picture, it would seem the variance is indeed less than the 100 lbs/inch threshold.  However, upon digging and grouping the summary statistics by the log where the coil was produced, it shows that Lot 3 has a variance of 170, which is a great deal over the allowable tolerance.  Management would then need to address these issues or more data would need to be collected to determine if outliers may be causing this issue or if the production of the coils needs to be addressed.  
![Suspension Total Summary](https://github.com/wprich/MechaCar_Statistical_Analysis/blob/main/Images/Suspension_Total_Summary.png)

![Suspension Lot Summary](https://github.com/wprich/MechaCar_Statistical_Analysis/blob/main/Images/Suspension_Lot_Summary.png)

## T-Tests on Suspension Coils

This next item on the agenda was to perform a t-test on the data for the suspension coils.  The purpose of this test was determine how different the mean of the overall data and then the means for each individual lot was compared to the population mean of 1500.  While the t score and p value for the lot 1 comparison were zero and 1 respectively, the other two lots and the overall were enough to determine that there was a problem at one of the lots.  Lot 2 had a p value of 0.6 and a t score of 0.5174 which suggests there some variation but not much to warrant a drastic concern.  Lot 3 on the other hand had a p value of 0.04168 and a t score of -2.0916 and the overall t test showed the sample had a p value of 0.06028 and a t score of -1.8931.  This tells us that Lot 3 is pulling the data and is contributing to a greater degree of variance than the other two.  This would suggest that Lot 3 has a production problem.

![T Test Comparison Summary](https://github.com/wprich/MechaCar_Statistical_Analysis/blob/main/Images/T_Test.png)

## Study Design: MechaCar vs Competition

These comparisons and tests were looking at just the MPG and suspension coils of MechaCar.  While these are factors that a consumer may consider when purchasing a car, there are other metrics that can be utilized to gain insight and predict spending habits.  One is the cost of Mechacar versus the competition.  How much does MechaCar cost to manufacture versus the competition?  This has a direct correlation to the price of the car and since most consumers want to know the price of something first and foremost, this seems like a keen piece of the puzzle that should be explored.  One way to do this is compare the price of the parts used in Mechacar against the parts used in cars of similar make and model.  By doing this, we can then isolate a single variable, labor, as the variable to be tested.  This is key since we have no idea what the competition is paying their workers to assemble, ship, and put the finishing touches on their cars.  By isolating labor and testing the sample mean price of cars similar to MechaCar with a t test, we can test how much the higher or lower the price of the cars are due to the labor.  The null hypothesis could be that workers compensation does not have an impact on the cars price.
