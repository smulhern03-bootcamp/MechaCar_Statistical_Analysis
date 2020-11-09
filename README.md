# MechaCar_Statistical_Analysis

## Linear Regression to Predict MPG (Miles per Gallon)
![Linear Regression](https://github.com/smulhern03-bootcamp/MechaCar_Statistical_Analysis/blob/main/Images/Regression.PNG)

Which variables/coefficients provided a non-random amount of variance to the mpg values in the dataset?
Vehicle length and ground clearance are the only statistically significant variables.  Readers should not the interecept is statistically significant. This recommends variables may or may not be within our dataset and may still need to be collected or observed that could impact MPG.

Is the slope of the linear model considered to be zero? Why or why not?
For hypothesis test, the null hypothesis (H0) is that the slope of the line will be zero denoting no relationship between the dependent variable (MPG) and the various indepdendent variables.  The fact that two variables (length and ground clearance) were both statistically significant would translate to a line with a slope other than zero.  Using other statistical measures we can confirm that no, the slope should not be considered zero and the null hypothesis can be rejected. The p-value is 5.35e-11, which is significantly smaller than our assumed significance level of 0.05%. Therefore, we can state that there is sufficient evidence to reject our null hypothesis, which means that the slope of our linear model is not zero.

Does this linear model predict mpg of MechaCar prototypes effectively? Why or why not?
From our linear regression model, the r-squared value is 0.71, which means that roughly 71% of the relationship between the prototype dimensions and MPG is explaied using this model.  As 71% is above half (50%) and just below 75%, this model does effectively explain the relationship between the protoype diminsions and MPG.  This model could be further improved based upon the Intercept being statistially significant as explained above.  This is further illustrated in the Adjusted R-square value being slightly lower than the Multiple R-squared value - if more explanatory variables are added, the Adjusted R-square value should improve as random chance (variance) is explained away as variables.

## Summary Statistics on Suspension Coils

The overall variance of the lots (Lot 1, 2, 3) does meet the less than 100 pounds per square inch specification.  The total variance is 62.29, so well below the specification.
![Total Summary Statistics](https://github.com/smulhern03-bootcamp/MechaCar_Statistical_Analysis/blob/main/Images/total_summary.PNG)

Additionally, Lots 1 and 2 as seperate lots, also pass the requirement with variances of .98 and 7.47, respectively.  Lot 3, however, does not meet the requirement.  Lot 3's variance exceeded the 100 pounds per square inch limit with a variance of 170.282.

![Lot Summary Statistics](https://github.com/smulhern03-bootcamp/MechaCar_Statistical_Analysis/blob/main/Images/lot_summary.PNG)

## T-Tests on Suspension Coils
![Lot 1 T-Test](https://github.com/smulhern03-bootcamp/MechaCar_Statistical_Analysis/blob/main/Images/Lot%201%20T-Test.PNG)
Based upon T-Tests of Lot 1, our P-value is smaller than .05 so we can safely reject the null hypothesis and the means are not statisically similar.

![Lot 2 T-Test](https://github.com/smulhern03-bootcamp/MechaCar_Statistical_Analysis/blob/main/Images/Lot%202%20T-Test.PNG)
Based upon T-Tests of Lot 2, our P-value is smaller than .05 so we can safely reject the null hypothesis and the means are not statisically similar.

![Lot 3 T-Test](https://github.com/smulhern03-bootcamp/MechaCar_Statistical_Analysis/blob/main/Images/Lot%203%20T-Test.PNG)
Based upon T-Tests of Lot 3, our P-value is greater than .05 so we cannot reject the null hypothesis and the means are statisically similar.

## Study Design: MechaCar vs Competition
The following study proposal is created for the purpose of allowing the Company to understand how the MechaCar is performing compared to competitors products.  This study will miles per gallon (city vs highway), horse power, acceleration and weight.  For this study, the null hypothesis will be:

  H0: None of the variables tested perform better than the competition

In order to run this test, two sets of multiple linear regression will be ran - one set on MechaCar's data while the other set will be based upon competitor's data.  This test will allow us to see which of the variables has the most impact on our competition (assuming more variables won't be required).  After these we can compare the impact of our results to our competitor's results and create additional studies if necessary.

Data on MechaCar performance can be easily assessible from our internal data collection.  Our competitors have published data that can be easily obtained.
