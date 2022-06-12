# MechaCar_Statistical_Analysis

## CHALLENGE OVERVIEW
---
This project goal is to review the production data for insights that may help the manufacturing team on solving the productions problems that are blocking the team to progress by performing the analysis listed below:
- Perform multiple linear regression analysis to identify which variables in the dataset predict the mpg of MechaCar prototypes
- Collect summary statistics on the pounds per square inch (PSI) of the suspension coils from the manufacturing lots
- Run t-tests to determine if the manufacturing lots are statistically different from the mean population
- Design a statistical study to compare vehicle performance of the MechaCar vehicles against vehicles from other manufacturers. For each statistical analysis, you’ll write a summary interpretation of the findings.

## FEATURES AND DATA SOURCES
- Data Source: [MechaCar_mpg.csv](https://github.com/Bruno-OGSilva/MechaCar_Statistical_Analysis/blob/cca52460cf746099a036cadcc4fbf88822f34f18/MechaCar_mpg.csv) & [Suspension_Coil.csv](https://github.com/Bruno-OGSilva/MechaCar_Statistical_Analysis/blob/cca52460cf746099a036cadcc4fbf88822f34f18/Suspension_Coil.csv)
- Programming Files: `MechaCarChallenge.R`
-  Data Tools: `tidyverse`, `dplyr`, `ggplot2`
-  Software: `RStudio`, `R`

## Challenge Deliverables
- Deliverable 1: Linear Regression to Predict MPG
- Deliverable 2: Summary Statistics on Suspension Coils
- Deliverable 3: T-Test on Suspension Coils
- Deliverable 4: Design a Study Comparing the MechaCar to the Competition


## Results
---

### Deliverable 1: Linear Regression to Predict MPG

- Techinical Analysis

![](https://github.com/Bruno-OGSilva/MechaCar_Statistical_Analysis/blob/cca52460cf746099a036cadcc4fbf88822f34f18/Assets/Deliverable%201-I.png)

- Output

![](https://github.com/Bruno-OGSilva/MechaCar_Statistical_Analysis/blob/cca52460cf746099a036cadcc4fbf88822f34f18/Assets/Deliverable%201-II.png)

#### Summary of results

- Which variables/coefficients provided a non-random amount of variance to the mpg values in the dataset?

The vehicle length, ground clearance, and the y intercept coefficients are statistically likely to provide a non-random amount of variance to the mpg values in the dataset as their p-values are much smaller than our significance level of 0.05%.

- Is the slope of the linear model considered to be zero? Why or why not?

We can reject the null hypothesis of our regression analysis test that the slope of the linear model is not considered to be zero. The p-value for this model is 5.35e-11, which is smaller than the assumed significance level of the 0.05% threshold.

- Does this linear model predict mpg of MechaCar prototypes effectively? Why or why not?

The linear model has an r-squared value of 0.7149, which means approximately 71.5% of all mpg predictions will be correct when using this model. Consequently, this multiple linear regression does predict mpg of MechaCar prototypes effectively.



### Deliverable 2: Summary Statistics on Suspension Coils

- Output

![](https://github.com/Bruno-OGSilva/MechaCar_Statistical_Analysis/blob/cca52460cf746099a036cadcc4fbf88822f34f18/Assets/Deliverable%202-I.png)

![](https://github.com/Bruno-OGSilva/MechaCar_Statistical_Analysis/blob/cca52460cf746099a036cadcc4fbf88822f34f18/Assets/Deliverable%202-II.png)

#### Summary of results

- The design specifications for the MechaCar suspension coils dictate that the variance of the suspension coils must not exceed 100 pounds per square inch. Does the current manufacturing data meet this design specification for all manufacturing lots in total and each lot individually? Why or why not?

The sample population of manufacturing lots as a whole has a suspension coil PSI variance of ~62.3, which is comfortability within the range of the 100 PSI variance requirement. Nevertheless, Lot 3 does not meet the design specification, as it has a variance of 170 PSI.

### Deliverable 3: T-Test on Suspension Coils

- Output

1. All Manufacturing Lots
![](https://github.com/Bruno-OGSilva/MechaCar_Statistical_Analysis/blob/cca52460cf746099a036cadcc4fbf88822f34f18/Assets/Deliverable%203-I.png)

2. Lot 1
![](https://github.com/Bruno-OGSilva/MechaCar_Statistical_Analysis/blob/cca52460cf746099a036cadcc4fbf88822f34f18/Assets/Deliverable%203-II.png)

3. Lot 2
![](https://github.com/Bruno-OGSilva/MechaCar_Statistical_Analysis/blob/cca52460cf746099a036cadcc4fbf88822f34f18/Assets/Deliverable%203-III.png)

4. Lot 3
![](https://github.com/Bruno-OGSilva/MechaCar_Statistical_Analysis/blob/cca52460cf746099a036cadcc4fbf88822f34f18/Assets/Deliverable%203-IV.png)

#### Summary of results

Although we failed to reject the null hypothesis of the all manufacturing lots since the p-value is 0.06, which is higher than the common significance level of 0.05, when we look into the 3 Lots separately, Lot 3 does not meet our significance level, thus it should be rejected.

### MechaChar vs Competition

It would be interesting to perform a statistical study on maintenance costs comparing MerchaCar vs competitors.

1. Metrics: Maintenance Cost over the time.
2. Null hypothesis:  the mean maintenance costs of each car player over the lifecycle of the vehicle are equal.
3. Alternative hypothesis: At least one of the means is different from all other groups
4. Statistical test: two-way ANOVA test
5. Data: Miles drive, Car Manufacturer and Maintenance Cost

