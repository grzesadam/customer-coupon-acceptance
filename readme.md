# Will the Customer Accept the Coupon?

This project analyzes a survey-based dataset to identify factors that influence whether drivers accept mobile coupons for nearby businesses. Using exploratory data analysis, visualization, and probability-based comparisons, it examines how contextual variables such as destination type, passenger presence, age, income, and prior visitation behavior affect coupon acceptance. The goal is to distinguish patterns between customers who accept coupons and those who do not, with a particular focus on bar-related offers.


Initial exploration of data
Columns with missing values: ['car', 'Bar', 'CoffeeHouse', 'CarryAway', 'RestaurantLessThan20', 'Restaurant20To50']

The column 'car' as it may not be important (we can drop it later), so I replaced Nan with "Not specified"
but the remaining columns concern the essence of the task I  dropped rows with missing values in these columns.

We dropped 12684-12079=605 rows

Proportion of observations that accepted the coupon in the cleaned data: 

56.93%

A summary of findings for bar goers:

2. What proportion of bar coupons were accepted?

41.2 %
3. Compare the acceptance rate between those who went to a bar 3 or fewer times a month to those who went more.

3 or fewer: 30%

more than 3: 69%


4. Compare the acceptance rate between drivers who go to a bar more than once a month and are over the age of 25 to the all others.  Is there a difference?

Acceptance rate for drivers who go to a bar more than once a month and are over the age of 25: 73.8%

Acceptance rate for all other drivers:

40.5%
5. Use the same process to compare the acceptance rate between drivers who go to bars more than once a month and had passengers that were not a kid and had occupations other than farming, fishing, or forestry.

71.1%

6. Compare the acceptance rates between those drivers who:

- go to bars more than once a month, had passengers that were not a kid, and were not widowed 
71.1%
- go to bars more than once a month and are under the age of 30 
50.5%
- go to cheap restaurants more than 4 times a month and income is less than 50K.
66.3%

7.