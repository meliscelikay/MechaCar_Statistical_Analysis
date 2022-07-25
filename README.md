# MechaCar_Statistical_Analysis
## Project Overview
The purpose of this project is to provide analysis for AutoRUs’s new prototype vehicle, Mechacar, and help them improve production process which has been problematic. I used R to demonstrate 4 Deliverables needed for this project: 
-	Run Linear Regression analysis to predict MPG
-	Summary Statistics on Suspension Coils 
-	Perform T-Test on Suspension Coils 
-	Design study comparing Mechacar vs competition 

## Resources
- Dataset: [MechaCar_mpg.csv](https://github.com/meliscelikay/MechaCar_Statistical_Analysis/blob/f4ac1144a141932eef84fa5eaba3ec4e97c0cce6/Resources/MechaCar_mpg.csv), [Suspension_Coil.csv](https://github.com/meliscelikay/MechaCar_Statistical_Analysis/blob/f4ac1144a141932eef84fa5eaba3ec4e97c0cce6/Resources/Suspension_Coil.csv)
- Software:  RStudio 2022.07.0+548

## Linear Regression to Predict MPG

![Linear Regression to Predict MPG.png](https://github.com/meliscelikay/MechaCar_Statistical_Analysis/blob/f4ac1144a141932eef84fa5eaba3ec4e97c0cce6/Resources/Linear%20Regression%20to%20Predict%20MPG.png)

*1.* Which variables/coefficients provided a non-random amount of variance to the mpg values in the dataset?

This dataset shows a non-random amounts of variance effect on the MPG of the MechaCar are the **vehicle_length** and the **ground_clearance**.

*2.* Is the slope of the linear model considered to be zero? Why or why not?

The slope of the linear model is not considered to be zero as the **p-Value** of `5.35e-11` which is significantly lower than the **significance level = 0.05%** and thus the null hypothesis must be rejected.

*3.* Does this linear model predict mpg of MechaCar prototypes effectively? Why or why not?

The slope of the linear model predicts prototypes of mpg MechaCar is an effective dataset since the r-squared value is **0.7149**, which indicates that the model is 71% accurate. 

Data shows vehicle length and ground clearance can play a major role in MPG; higher vehicles tend to be less aerodynamic which can cause drag causing engine to consume more fuel. Surprisingly vehicle weight, spoiler angle, and drivetrain system (all-wheel drive) did not play a big role in fuel efficiency. 

## Summary Statistics on Suspension Coils

### Total Summary
![Suspension_totalsummary.png](https://github.com/meliscelikay/MechaCar_Statistical_Analysis/blob/f4ac1144a141932eef84fa5eaba3ec4e97c0cce6/Resources/Suspension_totalsummary.png)

### Lot Summary
![Suspension_lotsummary.png](https://github.com/meliscelikay/MechaCar_Statistical_Analysis/blob/f4ac1144a141932eef84fa5eaba3ec4e97c0cce6/Resources/Suspension_lotsummary.png)

Mechacar suspension coils are not supposed to exceed **100psi** for optimal performance. While **Lot 1** and **Lot 2** are within range, I found that **Lot 3** had **170.29psi** which is unacceptable and signals significant problems with production.

## T-Tests on Suspension Coils
![ttest all.png](https://github.com/meliscelikay/MechaCar_Statistical_Analysis/blob/f4ac1144a141932eef84fa5eaba3ec4e97c0cce6/Resources/ttest%20all.png)
![ttestlot1.png](https://github.com/meliscelikay/MechaCar_Statistical_Analysis/blob/f4ac1144a141932eef84fa5eaba3ec4e97c0cce6/Resources/ttestlot1.png)
![ttestlot2.png](https://github.com/meliscelikay/MechaCar_Statistical_Analysis/blob/f4ac1144a141932eef84fa5eaba3ec4e97c0cce6/Resources/ttestlot2.png)
![ttestlot3.png](https://github.com/meliscelikay/MechaCar_Statistical_Analysis/blob/f4ac1144a141932eef84fa5eaba3ec4e97c0cce6/Resources/ttestlot3.png)

Using R, I performed a T-Test to analyze different lots to ensure average of **1500psi** was consistent. Again, **Lot 1** and **Lot 2** were within range but **Lot 3** had **1496.14**. Mechacar engineers should pay close attention to **Lot 3**, although results were within **0.04** tolerance it is still very close to failing level of **0.05**. Significant failures indicate the production process needs to be reviewed for **Lot 3**. 

## Study Design: MechaCar vs Competition
It would be beneficial to analyze data from other manufacturers to compare against Mechacar results. Most consumers compare fuel efficiency across several brands as one of their top deciding factors before purchasing a new vehicle. Vehicle size, design, weight, drivetrain (All wheel drive/front wheel drive/rear wheel drive), and ground clearance (higher for more utility) can all impact MPG (fuel efficiency). Mechacar’s engineers would have to consider all these variables in order to produce a fuel efficient vehicle but company executives would have to do it in a cost efficient manner which would maximize profitability.
