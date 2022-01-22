### Scope and Aim
This project aims at creating routines that fit an input of random variables to a set of continuous / discrete distributions to determine the best fitting distribution for the sample data. Input sample is tested against discrete distributions like Bernoulli, Poisson, Geometric and continuous distributions like Normal, Gamma and Weibull. We generate maximum likelihood estimates of the distributions that are very close to the actual parameters of the sample data set, and perform Chi-Squared goodness of fit tests on the sample data against every distribution to validate the goodness of fit of the routine. Additionally, we validate negative scenarios, for e.g., an input geometric data should fail the goodness of fit test for a normal distribution.  

### Method & Findings
Distributions under consideration:
* **Discrete**: Poisson, Geometric, Bernoulli
* **Continuous:** Normal, Gamma, Weibull
The above discrete distributions and continuous distributions were tried to fit a Maximum Likelihood Estimate for. Once the MLE estimate gives the parameters of the best distribution, we evaluate the fit using the Goodness of fit (Chi-squared) test.


_Maximum Likelihood estimate:_ MLE is a technique used to estimate the parameters of a distribution. In this technique, we find the parameter values that maximize the likelihood of making the observations given the parameters. Specifically, we differentiate the distribution wrt to the parameters and equate it to zero to find the best parameters that satisfy the optimal fit.


_Goodness of fit test:_ We use the chi square test to assess the goodness of fit for the assumed distribution. For the example of a normal distribution hypothesis testing, the null hypothesis is that the distribution is normal and the alternate hypothesis is that we have sufficient evidence to prove that the distribution is non-normal. Therefore, a p value of less than 0.05 or a Test statistic greater than Critical statistic (as shown in the table below) indicates rejection of the null hypothesis for the distribution. The logic for the test is coded by equally sampling input data into bins and calculating the expected (Ei)/ observed frequencies(Oi) of data in each range. The Chi-squared statistic is calculated using the below logic:

![GOF](https://github.com/svellaichamy3/Simulation/blob/main/Distribution%20Fitting/chisq.PNG)

### Sample Result
Generated Poisson distribution data. 

![dist](https://github.com/svellaichamy3/Simulation/blob/main/Distribution%20Fitting/images/p1.PNG)

The output from the routine is as follows:

![op](https://github.com/svellaichamy3/Simulation/blob/main/Distribution%20Fitting/images/p2.PNG)

The MLE estimator is very close to the actual parameters (rate=2) used to generate the input
data.
From the p value as well as the Test statistic in relation to the Critical statistic, we see here that
the randomly generated Poisson data fails to reject the null hypothesis that the distribution is
Poisson. All other distributions reject the hypothesis that it belongs to other distributions.

### Conclusion
We have successfully implemented MLE for estimating hyperparameters and assessed the resultant goodness of fit using chi square test. We also saw the effect of having a lesser number of datapoints on the conclusion of the hypothesis testing. Lower number of datapoints cause the decision to be ambiguous.We infer that maximum likelihood estimators give the best estimates for input data distributions. Also, Chi-squared goodness of fit tests work well when data has large number of samples. In future, we should explore other goodness of fit tests on more distributions. This will help us utilize specific tests based on the nature of data samples to achieve best outcomes.


Code:  
Input_Distribution_Routines.ipynb  

Results:  
Fitting_Input_Distributions_Report.pdf
