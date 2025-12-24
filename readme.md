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


4. Compare the acceptance rate between drivers who go to a bar more than once a month and are over the age of 
25 to the all others.  Is there a difference?

Acceptance rate for drivers who go to a bar more than once a month and are over the age of 25: 73.8%

Acceptance rate for all other drivers:

40.5%
5. Use the same process to compare the acceptance rate between drivers who go to bars more than once a month and had 
passengers that were not a kid and had occupations other than farming, fishing, or forestry.

71.1%

6. Compare the acceptance rates between those drivers who:

- go to bars more than once a month, had passengers that were not a kid, and were not widowed 
71.1%
- go to bars more than once a month and are under the age of 30 
50.5%
- go to cheap restaurants more than 4 times a month and income is less than 50K.
66.3%


7. The main conclusion seems to be that drivers over 25 who frequent bars are much more likely to accept bar-related coupons, 
especially when accompanied by non-kid passengers and not widowed (although we have not checked whether being widowed had an influence).
Younger drivers and those with lower income visiting cheap restaurants also show higher acceptance rates, 
indicating that age, social context, and economic factors significantly influence coupon acceptance behavior.

# Further Analysis

First, let's explore wehther there are any subgroups that are much more eager to accept coupons than the general population.
The overall acceptance rate is 56.93% of the surveyed individuals.

For this puorpose, I have analysed the acceptance rates for all the distinct values of the categorical columns, namely:
- gender,
- age,
- maritalStatus,
- education,
- occupation,
- income,
- Bar,
- CarryAway,
- RestaurantLessThan20,
- Restaurant20To50,
- car,
- destination,
- weather,
- time,
- passenger,

In order to assess whether any of these values of those categories correspond to a significantly higher acceptance rate I stored
the acceptance rates along the number of rows  for that group. This allows us to reject very low numbers of people who declared a given value. 
To see whether the number of people is significant, I plotted the average number of participants divided by the number of distinct values of each category. 

This resulted in the table
Total acceptance rate: 56.93%
Showing categories with rate > 62.63%

| column           | category                                 |   n | avg n/val | rate   |
|------------------|-------------------------------------------|-----:|----------:|--------:|
| car              | Car that is too old to install Onstar :D |   21 |      2013 | 80.95% |
| car              | Mazda5                                   |   22 |      2013 | 72.73% |
| occupation       | Healthcare Practitioners & Technical     |  222 |       483 | 71.62% |
| education        | Some High School                         |   88 |      2013 | 71.59% |
| occupation       | Production Occupations                   |   88 |       483 | 70.45% |
| occupation       | Healthcare Support                       |  242 |       483 | 69.83% |
| occupation       | Construction & Extraction                |  154 |       483 | 68.83% |
| passenger        | Friend(s)                                | 3148 |      3020 | 67.63% |
| Restaurant20To50 | gt8                                      |  264 |      2416 | 66.29% |
| time             | 2PM                                      | 1916 |      2416 | 66.08% |
| Restaurant20To50 | 4~8                                      |  684 |      2416 | 65.35% |
| occupation       | Protective Service                       |  175 |       483 | 64.57% |
| Bar              | 4~8                                      | 1054 |      2416 | 63.76% |
| occupation       | Architecture & Engineering               |  175 |       483 | 63.43% |
| destination      | No Urgent Place                          | 5970 |      4026 | 63.40% |
| age              | below21                                  |  504 |      1510 | 63.29% |


I would reject the first two rows as they correspond to very low numbers of people (21 and 22).
Interestingly, it seems that the highest acceptance rates of any coupons are healthcare practitioners and technical staff.
Some High School and Production Occupations are also not very numerous, so I think the results are not so reliable. 
What is more reliable are Healthcare Support and Construction & Extraction workers. 

It also seems that people who have friends as passengers are much more likely to accept coupons. 

Further analysis of pairwise combinations of these categories may yield more insights. I selected a few as shown on the chart below. 
First thing we notice that many of these combinations lyield a small number of people (less than 100), so the results may not be very reliable.
![img.png](img.png)