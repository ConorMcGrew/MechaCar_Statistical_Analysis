# MechaCar_Statistical_Analysis

## Linear Regression to Predict MPG

<img width="819" alt="Screen Shot 2021-06-27 at 7 07 53 PM" src="https://user-images.githubusercontent.com/80495710/123562187-1056b800-d77b-11eb-8f04-038b4985b8e4.png">


<img width="823" alt="Screen Shot 2021-06-27 at 7 07 38 PM" src="https://user-images.githubusercontent.com/80495710/123562184-09c84080-d77b-11eb-9259-ae81260cef3b.png">

- Which variables/coefficients provided a non-random amount of variance to the mpg values in the dataset?
- The vehicle length and ground clearance each impacted the mpg to an extent that is not likely random. Vehicle length had an associated p-value of 2.6 X 10^(-12), and ground clearance had an associated p-value of 5.21 X 10^(-8) (so the probably that these factors affected mpg to this extent is random is less than one in ten million).

- Is the slope of the linear model considered to be zero? Why or why not?
- No, the linear model gives an overall p-value (F-Statistic) of 5.35 X 10^(-11). So, the slope of the linear regression is not negligible. 

- Does this linear model predict mpg of MechaCar prototypes effectively? Why or why not?
- Not exactly. If we look at the Std. Error of each of the coefficients, every one of them is greater than 10% of the coefficient value. So while the mpg is influenced by each of these factors, this linear model is not the best at predicting it. (If you took any one sample MPG and compared it to the MPG calculated from this linear regression, it may seem very close)

## Summary Statistics on Suspension Coils

<img width="375" alt="Screen Shot 2021-06-27 at 9 06 20 PM" src="https://user-images.githubusercontent.com/80495710/123565628-9418a080-d78b-11eb-8c83-9a222ef6991d.png">

<img width="513" alt="Screen Shot 2021-06-27 at 9 06 13 PM" src="https://user-images.githubusercontent.com/80495710/123565636-9844be00-d78b-11eb-94da-cfd00d3fc025.png">

- The design specifications for the MechaCar suspension coils dictate that the variance of the suspension coils must not exceed 100 pounds per square inch. Does the current manufacturing data meet this design specification for all manufacturing lots in total and each lot individually? Why or why not?

- Lot 1 has a variance of 0.97... psi, and lot 2 has a variance of 7.46... psi so each of those are within specifications. Lot 3, however, has a variance of 170.286... psi. Now, the standard deviation associated with lot 3 is 13.049... psi, so the probability of a coil being more than 100 psi different is <0.00001 (a z-score of 13). So it depends on what is meant by variance. If by variance they mean sample variance, then lot 3 is outside specifications. However, if they mean standard deviation, then lot 3 is still highly unlikely to be that far outside of regulation. 

## T-Tests on Suspension Coils

<img width="403" alt="Screen Shot 2021-06-27 at 9 49 28 PM" src="https://user-images.githubusercontent.com/80495710/123568398-405d8580-d792-11eb-97b0-36b4b4b30ee6.png">

<img width="407" alt="Screen Shot 2021-06-27 at 9 49 40 PM" src="https://user-images.githubusercontent.com/80495710/123568410-46ebfd00-d792-11eb-8b3d-44ed7fc89561.png">

<img width="406" alt="Screen Shot 2021-06-27 at 9 49 51 PM" src="https://user-images.githubusercontent.com/80495710/123568422-4f443800-d792-11eb-94d6-449a9916a802.png">

<img width="402" alt="Screen Shot 2021-06-27 at 9 49 59 PM" src="https://user-images.githubusercontent.com/80495710/123568443-5b2ffa00-d792-11eb-86d0-c0d68584e0e7.png">

Lot 1 had a p-value of 1 (so the average psi is exactly the population average). 
Lot 2 had a p-value of 0.6072 (so the difference in the sample average is likely only due to random variation).
Lot 3 had a p-value of 0.04168 (so the difference in this sample average(1496.14 psi) is not due to random chance).

## Study Design: MechaCar vs Competition.

Write a short description of a statistical study that can quantify how the MechaCar performs against the competition. In your study design, think critically about what metrics would be of interest to a consumer: for a few examples, cost, city or highway fuel efficiency, horse power, maintenance cost, or safety rating.
In order to determine how MechaCar Performs versus the competition, consider the following questions:

- What metric or metrics are you going to test?
- The three primary factors when looking to purchase a car (according to consumers) are: Quality, Cost of Ownership, Reliability. So the main metrics would likely be maintenance costs / fuel efficiency, lifetime estimated mileage, and horsepower-to-weight ratio / torque. 
- What is the null hypothesis or alternative hypothesis?
- The null would of course be that each / all of those metrics have no affect on the probability of purchase from either MechaCar or Competition. 
- What statistical test would you use to test the hypothesis? And why?
- I would probably suggest running both t-tests for independent factors and an ANOVA to see if some combination of all those factors leads to a more likely purchase. The other reason to run an ANOVA, is that we are not only trying to determine if those factors affect sales from MechaCar or sales from a competitor individually, but whether that factor makes a person more likely to purchase from one or the other (Not only trying to decide which factor influences the sales at each retailer, but also if that factor makes a diffence as to which retailer they buy from).
- What data is needed to run the statistical test?
- List of common maintenances & mechanics labor guide value for those maintenances, mpg, mileage expected over typical car ownership period, horsepower, vehicle weight, acceleration (0 to 60 time). 
