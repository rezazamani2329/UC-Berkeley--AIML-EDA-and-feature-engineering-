# feature engineering and exploratory Data Analysis (EDA) to driver's decision to accept coupons delivered to their cell phones while driving
- This repo contains the files for the project PCMLAI Module 5 assignment 
#### Description of files in the repo
- 'coupons.csv': this files contains dataset used for this project 
- 'prompt-final(2).ipynb': this file contains the codes for this project 
### Purpose: Analyze and identify the factors that influence a driver's decision to accept coupons delivered to their cell phones while driving.

## Data Description
Keep in mind that these values mentioned below are average values.
The attributes of this data set include:
    User attributes
        Gender: male, female
        Age: below 21, 21 to 25, 26 to 30, etc.
        Marital Status: single, married partner, unmarried partner, or widowed
        Number of children: 0, 1, or more than 1
        Education: high school, bachelors degree, associates degree, or graduate degree
        Occupation: architecture & engineering, business & financial, etc.
        Annual income: less than $12500, $12500 - $24999, $25000 - $37499, etc.
        Number of times that he/she goes to a bar: 0, less than 1, 1 to 3, 4 to 8 or greater than 8
        Number of times that he/she buys takeaway food: 0, less than 1, 1 to 3, 4 to 8 or greater than 8
        Number of times that he/she goes to a coffee house: 0, less than 1, 1 to 3, 4 to 8 or greater than 8
        Number of times that he/she eats at a restaurant with average expense less than $20 per person: 0, less than 1, 1 to 3, 4 to 8 or greater than 8
        Number of times that he/she goes to a bar: 0, less than 1, 1 to 3, 4 to 8 or greater than 8

    Contextual attributes
        Driving destination: home, work, or no urgent destination
        Location of user, coupon and destination: we provide a map to show the geographical location of the user, destination, and the venue, and we mark the distance between each two places with time of driving. The user can see whether the venue is in the same direction as the destination.
        Weather: sunny, rainy, or snowy
        Temperature: 30F, 55F, or 80F
        Time: 10AM, 2PM, or 6PM
        Passenger: alone, partner, kid(s), or friend(s)

    Coupon attributes
        time before it expires: 2 hours or one day


## Key Findings
See Jupyter notebook for detailed analysis: prompt-final.ipynb

### Data Visualization 
- we check data, find one column is not revelant.
- we check null data, and then decide to fill them with mode 

### What proportion of the total observations chose to accept the coupon
- Proportion of the total observations that chose to accept the coupon: 56.84%

## Investigating the Bar Coupons
#### What proportion of bar coupons were accepted? 
- Proportion of the total observations that chose to accept the coupon: 41.00%
- Percent of visitors (between 1 to 3 times per month) accepted coupons: 64.7%
- Coupons Accepted for those who went to a bar more than once a month and are also more than 25 is about 69.52 percent
- Coupons Accepted by all others is about 39.33 percent
- There is remarkable differece of acceptance between two groups (diffrence between them is about 30.19 percent)
- Coupons Accepted by drivers who go to bars more than once a month and had passengers that were not a kid and had occupations other than farming, fishing, or forestry is about:
        68.79 percent

### more groupby 
- Group 1 : go to bars more than once a month, had passengers that were not a kid, and were not widowed
- group 2 : go to bars more than once a month and are under the age of 30
- group 3 : go to cheap restaurants more than 4 times a month and income is less than 50K

---------------------
- Coupons Accepted by group one is 68.8 percent
---------------------
- Coupons Accepted by group two is 72.2 percent
---------------------
- Coupons Accepted by group three is 73.3 percent

### Based on these observations: 
- Based on these observations, the porbability of accepting the bar coupons for drivers, whose age is 21, 26 or 31 is high.
- Based on these observations, the porbability of accepting the bar coupons for the Student and Unemployed drivers are more than others.
- Based on these observations, the porbability of accepting the bar coupons for the drivers who are Alone is higher than the others.

### Independent Investigation
-Using the bar coupon example as motivation, you are to explore one of the other coupon groups and try to determine the characteristics of passengers who accept the coupons. 
-we chose Coffe House as it has the highest acceptance
- Ressults for accepting the coupon of coffe house by drivers:
- diver with lower than 25000 have the highe probability to accept
- Unempployed and Students dirvers are more likely to accpet
- No ergent place for expiration is more likely to be accepted
- No ergent place for destination is more likely to be accepted
- Alone passenger is more likely to be accepted
- driver with the age of 21 and 26 are more likely to accept
- there is no significant difference between men and women to accpet
- it is more likely to accept the coupon in sunny weather
