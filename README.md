# UCI Coupon Analysis

This repository contains an analysis of the coupon surveys performed on Amazon Mechanical Turk, which describes different driving scenarios and asks whether someone would accept a coupon based on these scenarios. An analysis of the scenarios involving restaurants with dishes that cost between $20-$50 per person is included. You can review the workbook [here](./prompt.ipynb).

## Conclusion

Based on the data provided, we can draw the following conclusions for coupon acceptance rates for restaurants that cost on average $20-$50 per person. We performed analyses to look for correlations in age, income, occupation and education to see if certain demographics tend to accept or decline these coupons.

### Age

- Expensive Restaurant coupon acceptance rate for drivers over **under** age 35 with more than 1 expensive restaurant visit per month: 0.5551839464882943
- Expensive Restaurant coupon acceptance rate for drivers over **over** age 35 with more than 1 expensive restaurant visit per month:  0.5585106382978723

There doesn't seem to be a lot of correlation when grouped together like this, but the graphs of each individual age category do show a trend where older drivers tended to decline at a higher rate. We used this conclusion to further explore related demographics, such as income, occupation and education.

### Income

- Definitions:
    - Lower: Less than $25000
    - Middle: $25000-$62499
    - Upper: More than $62500
- Middle class salaries acceptance rate:  0.48756218905472637
- Lower and upper class salaries acceptance rate:  0.4152334152334152
- Middle class salaries acceptance rate with at least 1 visit per month:  0.5639810426540285
- Lower and upper class salaries acceptance rate with at least 1 visit per month:  0.5507246376811594

As stated above, there seems to be a trend where lower and upper class drivers had lower acceptance rates than drivers in the middle class ranges. This may be explained by the social characteristics of individuals in these different income ranges (i.e. lower class tend not to go to expensive restaurants, upper class tend not to use/need coupons). There is a clear trend past the $62500 mark, but interestingly, a larger proportion of drivers making more than $100000 did have a higher acceptance rate of coupons.

There seems to be a wave-like trend in the income vs acceptance rate curves, which is very interesting, and may warrant further study.

### Occupation

- Unemployed, retired or student acceptance rate:  0.3747178329571106
- Industry occupation acceptance rate:  0.4784394250513347
- Unemployed, retired or student acceptance rate with at least 1 visit per month:  0.4740740740740741
- Industry occupation acceptance rate with at least 1 visit per month:  0.4784394250513347
- Unemployed, retired or student total coupons:  443
- Unemployed, retired or student with at least 1 visit per month total coupons :  135

Drivers who do not have occupations (in this case, unemployed, retired or students) overall tended not to accept expensive restaurant coupons at a greater rate than those with industry occupations listed. However, this discrepancy is made clearer when an additional variable for the number of visits to the expensive restaurants per month is added.

This can probably be explained by those without occupations being required to be more frugal, and so expensive restaurants are out of their budgets. This is further evidenced by the number of occupation-less drivers with at least 1 visit per month to expensive restaurants being far less than the total.

### Education

- High school education acceptance rate:  0.5309734513274337
- College education acceptance rate:  0.4152334152334152
- High school education with at least 1 visit per month acceptance rate:  0.6521739130434783
- College education with at least 1 visit per month acceptance rate:  0.5507246376811594

Similar to the Occupation section, drivers with high school as their highest education tended to accept expensive restaurant coupons more readily than those with some level of college education. This trend holds even when further enhanced with the additional variable of number of visits per month. This is the clearest trend we have seen when it comes to acceptance rate.