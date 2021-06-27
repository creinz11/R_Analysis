# MechaCar Statistical Analysis

## Linear Regression to Predict MPG

1) Which variables/coefficients provided a non-random amount of variance to the mpg values in the dataset?
   
Of the coefficients tested, three produced a non-random amount of variance to MPG (Vehicle Weight, Vehicle Angle and AWD. Vehicle length and Ground Clearance produced the highest rate of variability to MPG.
   
2) Is the slope of the linear model considered to be zero? Why or why not?

If there is a significant  relationship between our independent and dependent variable, the slope will not be zero. Our P-value is 0.0000000000535, well abovwe the 0.05 significance level.

4) Does this linear model predict mpg of MechaCar prototypes effectively? Why or why not?

Our Multiple R-Squared Value is 0.7149. This R-Squared value means that the model correclty predicts MPG correctly 71.49% of the time. Generally speaking, any R-Squared value greater than 0.70 is considered to be a strong positive correlation. Based on this guidance, our linear model is effective.

## Summary Statistics on Suspension Coils

1) The design specifications for the MechaCar suspension coils dictate that the variance of the suspension coils must not exceed 100 pounds per square inch. Does the current manufacturing data meet this design specification for all manufacturing lots in total and each lot individually? Why or why not?

Data in our Suspension_Coil.csv file provided 150 datapoints across three production lots. Lot 1 and Lot 2 are well within the design specifications. Lot 1 and Lot 2 have similar means, and medians. THe variance in Lot 1 was 0.9795918, and the variance in Lot 2 was 7.4693878, both well within the 100 PSI Variance guidance. Lot 3 has a variance of 170.2861224, which does not meet production requirements. 

## T-Tests on Suspension Coils
1) Briefly summarize your interpretation and findings for the t-test results. Include screenshots of the t-test to support your summary.

For the hypothesis that the PSI of production lots sampled from a population in which the mean PSI was 1500 (and the distribution of PSI is insufficiently close to normal for the t-test to be adequately applicable), then the value of t differs from 0 by an amount which has probability more than 0.05 of being attained if that hypothesis were true. We recorded p-values for the respective lots as follows (All lots: 0.06028, Lot1: p-value 1, Lot2: 0.6072, Lot3: 0.04168). On the whole, we fail to reject the null hypothesis and the mean PSI is 1500. If we look at specific production lots, we get a different story. Lot 1 and Lot 2 both registered p-values below our 0.05 significance threshold (fail to reject the null). Lot 3 registered a p-value of 0.04168 which IS above our significance level. For Lot 3, we will reject the null hypothesis and accept the alternative hypothesis indicating the mean PSI is not 1500. See t-test results for all suspension coils, and all three individual lots below.

## All Lots

<img width="428" alt="Screen Shot 2021-06-27 at 9 19 49 AM" src="https://user-images.githubusercontent.com/80016496/123548053-d8268980-d728-11eb-8264-6d7971078187.png">

## Lot 1

<img width="496" alt="Screen Shot 2021-06-27 at 9 20 21 AM" src="https://user-images.githubusercontent.com/80016496/123548072-ec6a8680-d728-11eb-804d-43a9e8523a39.png">

## Lot 2

<img width="512" alt="Screen Shot 2021-06-27 at 9 20 59 AM" src="https://user-images.githubusercontent.com/80016496/123548095-01471a00-d729-11eb-9324-cc160e650473.png">

## Lot 3

<img width="500" alt="Screen Shot 2021-06-27 at 9 21 33 AM" src="https://user-images.githubusercontent.com/80016496/123548117-158b1700-d729-11eb-9015-d772f319bd5d.png">


## Study Design: MechaCar vs Competition

As technology progresses, and cars improve overall performance, safety ratings continue to be an essential part to successfully selling vehicles in large quantities. An important differentiator between the MechaCar and the competition would be how well the car performs in crash tests. For illistrative purposes, we will start with one specific test, which we can then replicate for other aspects of the National Highway Traffic Safety Administration's testing protocol. The below statistical analysis could be conducted on the Front crash Test data of the MechaCar vs. competitors. The metric we will be testing is Injury Measures. Injury Measures can be defined below:

Sensors in the dummy — or dummies, in the case of passenger-side small overlap — are used to determine the    likelihood that a driver or passenger would sustain various types of injuries in a similar real-world crash. Measures recorded by sensors in the head, neck, chest, legs and feet of the dummy indicate the level of stress or strain on that part of the body (source: IIHS.org)

### Hypotheses

HO: The MechaCar does not perform better in the Front Crash Test than the competitons comparable car
HA: The MechaCar does perform better in the Front Crash Test than the competitions comparable car

### Testing & Data

In order to effectively test the above analysis, we would first need the full technical report of vehicles from the National Highway Traffic Safety Administration's lab. This data can theoretically be sourced for free for all vehicles on the NHTSA's website. Once receiving the data, we would load our CSV's into R. We would conduct a variety of t-tests ons pecific metrics in order to get afull picture of the MechaCar's safety vs. the competiton.
