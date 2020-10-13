# Covid-19-analysis-with-uw-ubicomp
This is an ongoing project to analyze how COVID 19 pandemic impacts human behavior in the US. data is downloaded from SafeGraph. I am Hugh and I am working on this with Chunjong Park in UW's Ubiquitous Computing Lab, a lab that aims to brings the best of technology to help society. 
# Findings
2020-09-25:

Within the counties that implemented shelter in place order, why did some counties have more drastic change in people's behavior and some counties don't? I used mutual information and random forest to find out that **Median Household Income** and **Population** are 2 important variables that contribute to people's change of behavior. [See the notebook that I used for this finding here](https://github.com/wenjunsun/Covid-19-analysis-with-uw-ubicomp/blob/master/2020-09/what_make_people_change_behavior.ipynb)

2020-10-13:

Using standardized linear regression and increase of R^2 analysis, found that **Median Household Income** increases the explanatory of the model by **50%** when it is included in the model! ![see the notebook here](https://github.com/wenjunsun/Covid-19-analysis-with-uw-ubicomp/blob/master/2020-10/standardized_linear_regression.ipynb)
