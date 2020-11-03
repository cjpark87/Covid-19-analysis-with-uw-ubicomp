# Covid-19-analysis-with-uw-ubicomp
This is an ongoing project to analyze how COVID 19 pandemic impacts human behavior in the US. data is downloaded from SafeGraph. I am Hugh and I am working on this with Chunjong Park in UW's Ubiquitous Computing Lab, a lab that aims to brings the best of technology to help society. 
# Findings
2020-09-25: [See the notebook here](https://github.com/wenjunsun/Covid-19-analysis-with-uw-ubicomp/blob/master/2020-09/what_make_people_change_behavior.ipynb)

Within the counties that implemented shelter in place order, why did some counties have more drastic change in people's behavior and some counties don't? I used mutual information and random forest to find out that **Median Household Income** and **Population** are 2 important variables that contribute to people's change of behavior.

2020-10-13:[see the notebook here](https://github.com/wenjunsun/Covid-19-analysis-with-uw-ubicomp/blob/master/2020-10/standardized_linear_regression.ipynb)

Using standardized linear regression and increase of R^2 analysis, found that **Median Household Income** increases the explanatory of the model by **50%** when it is included in the model! 

2020-11-2: [see the notebook here](https://github.com/wenjunsun/Covid-19-analysis-with-uw-ubicomp/blob/master/2020-11/propensity_weighted_method.ipynb)

![](https://github.com/wenjunsun/Covid-19-analysis-with-uw-ubicomp/blob/master/graphs/box-whisker-pscore-logistic.png)
- still used logistic regression to obtain propensity score. (might try to use GBM or random forest in the future)
- used proper weighting method of estimating ATE. We weighed each data point by its inverse of propensity score if it is treated, or 1 - propensity score if it is not treated.
- used bootstrapping method and `survey` package from R to obtain the standard error or our results
- results of weighted effect size of treatment/non-treatment groups:

| SIP. | diff_in_perc_at_home | standard error |
|------|----------------------|----------------|
| 0    | 0.0190328            | 0.0016932478   |
| 1    | 0.0309015            | 0.0009284685   |
 
 - glass dealta = `0.40`. This means we can say that having done shelter in place, counties increased the completely stay at home percentage of people by 0.4 standard deviations
