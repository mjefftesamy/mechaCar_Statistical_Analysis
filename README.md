# Purpose of Analysis

Using data analytics and r programming, reviewed MechaCar production data to provide insights to the manufacturing team. The following data analytics were performed with analysis results detailed for each topic:

-- Multiple linear regression analysis to identify which vairables in the dataset predict the MPG (miles per gallon) of MechaCar prototypes.

-- Collection of summary statistics on PSI (pounds per square inch) of the suspension coils from the manufacturing lots.

-- T-tests to determine if the suspension coil manufacturing lots are statistically different from the mean population.

-- Designing a statistical study to compare vehicle performance of the MechaCar vehicles against vehicles from other manufacturers.


# Analysis Results and Challenges:
### Analysis Results
##### Linear Regression to Predict MPG

Using the lm() function, a multiple linear regression is performed including all six variables in the mpg test results dataset to determine the coefficient of determination (r-squared).
 

1-Which variables/coefficients provided a non-random amount of variance to the mpg values in the dataset? Vehicle length, ground clearance and intercept provide non-random amounts of variance to the mpg values in the dataset based on the p-values calculated for each variable. That means the vehicle length and ground clearance have statistically significant impact on MPG and, because the intercept is statistically significant, there are other variables and factors that contribute to the variation in MPG that have not been included in the model.

2-Is the slope of the linear model considered to be zero? Why or why not? The slope of the linear model is not considered to be zero because the p-value of this model is 5.35e-11, which is much smaller than the presumed significance level of 0.05. Therefore we can reject the null hypothesis of the slope being zero.

3-Does this linear model predict mpg of MechaCar prototypes effectively? Why or why not? The linear model has an r-squared value of 0.71 indicating that approximately 71% of the time the linear model will predict the mpg values effectively, the remaining 29% could be due to instrumental error and/or external factors.


# Multiple Linear Regression Model Summary
![Dev1_lm](https://user-images.githubusercontent.com/63277310/125365482-577ba600-e342-11eb-8efa-e5a43824782b.png)

# Summary Statistics on Suspension Coils
![Dev1 _lm_summary](https://user-images.githubusercontent.com/63277310/125365511-65c9c200-e342-11eb-974b-a2cde0893c5a.png)

# PSI Statistical Total Summary
![Dev2_total_summary](https://user-images.githubusercontent.com/63277310/125365754-d375ee00-e342-11eb-86cb-ffd9f3a6658e.png)

# PSI Statistical Lot Summary
![Dev3_Lot_Summary](https://user-images.githubusercontent.com/63277310/125365786-e4266400-e342-11eb-9b9c-39d75cc5759a.png)

The design specifications for the MechaCar suspension coils dictate that the variance of the suspension coils must not exceed 100 pounds per square inch.
Based on that requirementment criteria, Manufacturing Lot1 with a variance of 0.98 PSI and Lot2 with a variance of 7.47 PSI meet the design specification individually.
However, Manufacturing Lot3 does not meet this requirement with a variance of 170.29 PSI, which exceeds the requirement. But altogether, the aggregate combination of the three manufacturing lots meets the specification with a variance of 62.29 PSI as shown in the summary dataframes above.

# T-Tests on Suspension Coils
Shown by the total summary and lot summary images above, both Manufacturing Lot1 and Lot2 have mean and median values that do not vary substantially from the population mean of 1500 pounds. With a p-value for Manufacturing Lot1 = 1 and a p-value for Lot2 = 0.61, the null hypothesis fails to be rejected for both Lot1 and Lot2, supporting the means for both lots are statistically similar to the population mean. But Manufacturing Lot3 has as p-value of 0.042 which indicates that there is statistical evidence which supports that the PSI for this manufacturing lot is slightly different from the population mean of 1500 pounds per square inch.

# T-Test Comparing All Manufacturing Lots Against Mean PSI
![Dev4_ttest_all](https://user-images.githubusercontent.com/63277310/125365855-06b87d00-e343-11eb-88fa-f5969d6a8f2b.png)

# T-Test Comparing Manufacturing Lot#1 Against Mean PSI
![Dev3_ttest_lot1](https://user-images.githubusercontent.com/63277310/125366720-aa565d00-e344-11eb-8040-457f87338cad.png)

# T-Test Comparing Manufacturing Lot#2 Against Mean PSI
![Dev5_ttest_lot2](https://user-images.githubusercontent.com/63277310/125366755-c0641d80-e344-11eb-9d91-1ebc45c90706.png)

# T-Test Comparing Manufacturing Lot#3 Against Mean PSI
![Dev6_ttest_lot3](https://user-images.githubusercontent.com/63277310/125366784-ceb23980-e344-11eb-8159-660d16a5104b.png)


# Study Design: MechaCar vs. Competition
To quantify how the MechaCar performs against the competition, additional statistical analysis can be performed. Of particular interest to start would be analysis into cost to provide consumers with supplemental information that further compares MechCar to competitors in this aspect.

# Hypotheses
Null Hypotheses (Ho): MechaCars have no difference in cost in comparision to competitors

Alternate Hypothesis (Ha): MechaCars have a difference in cost in comparsion to competitors.

# Statistical Tests
A multiple linear regression can be performed to better predict the cost (dependent variable) impact from multiple other variables such as fuel efficiency, horsepower, and engine size (independent variables).

Depending on the multiple linear regression results, a t-test (on one or multiple variables) to compare the MechaCar population to the competitors population. For example, comparision on the cost, fuel efficiency, and horsepower can be performed to see how the competitor mean population compares to MechaCar's mean population to understand if the two populations are similar.

Similarly, since there may be multiple variables of interest, ANOVA test can be performed to avoid increasing testing error that may be caused by executing numerous t-tests, if multiple variables are compared. The ANOVA test will be able to look at the entire collection of mean values to provide a ratio on variability between groups relative to variability within the groups to understand if one or more of the variables (e.g. fuel efficiency, horsepower, or engine size) is different or all variables are consistent with the cost mean.

# Data Required
A dataset of MechaCars and competitors cars makes, models, fuel efficiency, horsepower, engine size, and cost would be required where cost is considered a normally distributed dependent variable for the statistical analysis.

Challenges and Difficulties Encountered
No challenges were encountered during the analysis.



