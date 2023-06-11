# MechaCar_Statistical_Analysis

## Part 1: Linear Regression to Predict MPG

lm_model <- lm(mpg ~ vehicle_length + vehicle_weight + spoiler_angle + ground_clearance + AWD, data = MechaCar_mpg)
> summary(lm_model)

Call:
lm(formula = mpg ~ vehicle_length + vehicle_weight + spoiler_angle + 
    ground_clearance + AWD, data = MechaCar_mpg)

Residuals:
     Min       1Q   Median       3Q      Max 
-19.4701  -4.4994  -0.0692   5.4433  18.5849 

Coefficients:
                   Estimate Std. Error t value Pr(>|t|)    
(Intercept)      -1.040e+02  1.585e+01  -6.559 5.08e-08 ***
vehicle_length    6.267e+00  6.553e-01   9.563 2.60e-12 ***
vehicle_weight    1.245e-03  6.890e-04   1.807   0.0776 .  
spoiler_angle     6.877e-02  6.653e-02   1.034   0.3069    
ground_clearance  3.546e+00  5.412e-01   6.551 5.21e-08 ***
AWD              -3.411e+00  2.535e+00  -1.346   0.1852    
---
Signif. codes:  0 ‘***’ 0.001 ‘**’ 0.01 ‘*’ 0.05 ‘.’ 0.1 ‘ ’ 1

Residual standard error: 8.774 on 44 degrees of freedom
Multiple R-squared:  0.7149,	Adjusted R-squared:  0.6825 
F-statistic: 22.07 on 5 and 44 DF,  p-value: 5.35e-11

The linear regression analysis identifies which variables in the dataset predict the mpg (miles per gallon) of MechaCar prototypes. The summary of the linear regression model provides valuable insights into the relationship between the variables and the mpg values.
![image](https://github.com/Newlie2/MechaCar_Statistical_Analysis/assets/115044466/42cf35ac-b382-4642-9c2a-2d799912063c)


## Part 2: Create Visualizations for the Trip Analysis

total_summary
# A tibble: 1 × 4
  mean_PSI median_PSI var_PSI sd_PSI
     <dbl>      <dbl>   <dbl>  <dbl>
1    1499.       1500    62.3   7.89
> 
> lot_summary
# A tibble: 3 × 5
  Manufacturing_Lot mean_PSI median_PSI var_PSI sd_PSI
  <chr>                <dbl>      <dbl>   <dbl>  <dbl>
1 Lot1                 1500       1500    0.980  0.990
2 Lot2                 1500.      1500    7.47   2.73 
3 Lot3                 1496.      1498. 170.    13.0
	  
The design specifications for the MechaCar suspension coils dictate that the variance of the suspension coils must not exceed 100 pounds per square inch (PSI).
By examining the total_summary dataframe, we can determine whether the current manufacturing data will satisfy the design specifications.

## Part 3: T-Tests on Suspension Coils

 t_test_all_lots

	One Sample t-test

data:  Suspension_Coil$PSI
t = -1.8931, df = 149, p-value = 0.06028
alternative hypothesis: true mean is not equal to 1500
95 percent confidence interval:
 1497.507 1500.053
sample estimates:
mean of x 
  1498.78 
![image](https://github.com/Newlie2/MechaCar_Statistical_Analysis/assets/115044466/a4f5347e-16c5-458e-ae7e-96b0d239ceb2)
	  
![image](https://github.com/Newlie2/MechaCar_Statistical_Analysis/assets/115044466/1f34b7f3-9801-4252-8e4a-a4e82051e1bd)

![image](https://github.com/Newlie2/MechaCar_Statistical_Analysis/assets/115044466/5de0ba74-2c0e-437d-ae00-b0fd0b0e9ea1)

The t-tests on the suspension coils was used to determine if the PSI (pounds per square inch) values for all manufacturing lots and each lot individually are statistically different from the population mean of 1,500 pounds per square inch.
	  
## Part 4: Design a Study Comparing the MechaCar to the Competition
To compare the performance of MechaCar vehicles against vehicles from other manufacturers, we will design a statistical study that focuses on the metric of fuel efficiency.
With the statistical test, we will need the following data:
Highway fuel efficiency (MPG) data for a sample of MechaCar vehicles.
Highway fuel efficiency (MPG) data for a sample of vehicles from other manufacturers.
This study will provide valuable insights into the performance of MechaCar vehicles in terms of fuel efficiency and help consumers make informed decisions when considering their vehicle choices.
In coclusion, by analyzing the data using a two-sample t-test, we can determine if MechaCar vehicles have a significantly different average highway fuel efficiency compared to their competition. 
