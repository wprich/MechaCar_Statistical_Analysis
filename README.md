# MechaCar_Statistical_Analysis

## Linear Regression to Predict MPG

This first analysis using R took at a look at the predicting the MPG of a vehicle using variables from other cars.  These variables or data was used to create a linear model in the y = m * x + b format.  This model was saved to a variable called 'mod'.  The summary function was then used on the mod variable to get a clear and concise grouping of information ready for interpretation.

![MechaCar_MPG_LM](https://github.com/wprich/MechaCar_Statistical_Analysis/blob/main/Images/MechaCar_MPG_LM.png)

By looking at the summary statistics, we can see that the intercept is labled as 103.964, this simply tells us that, according to the data, the gas tank for most cars should last around 104 miles.  This makes sense since a car that could go 0 miles on a full tank of gas makes no sense.  Then other factors will take effect, such as the vehicles height, weight etc.  Interestly, it seems that the vehicles length has more impact than the vehicles weight when it comes to calculating the MPG.  Lastly, this model shows that we can reject our null hypothesis that our slope should be 0 since our p-value is 5.35e-11, which is significantly less than 0.05.
