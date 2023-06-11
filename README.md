# MechaCar_Statistical_Analysis

Part 1: Linear Regression to Predict MPG

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

image.png

Part 2: Create Visualizations for the Trip Analysis

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


Part 3: T-Tests on Suspension Coils

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

  image.png
  image.png
  image.png

  Part 4: Design a Study Comparing the MechaCar to the Competition