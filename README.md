# Missing-Data-Analysis

# Objective and Methods

-Aimed to explore advanced methods for handling missing data in a dataset focused on forecasting.

-Investigated methods under Completely Missing at Random (CMAR) and Missing Not at Random (MNAR) mechanisms, including Maximum Likelihood Estimation (MLE), Bayesian Inference, and Selection Models.

-Emphasized the role of auxiliary variables in improving bias and precision.

-Documented the missing data rates for each variable, noting that PHEV had no missing values while other variables varied.
# Regression Analysis Without Missing Data
-Found a significant positive relationship between presidential approval ratings (Approval) and autonomous vehicle collisions (Vehicle), with a p-value < 0.001.

-The relationship between PHEV and Vehicle was positive but not statistically significant.

-The model explained a low percentage (8.63%) of the variance in Vehicle, suggesting other unaccounted factors.

# Auxiliary Variable Analysis
-Categorized auxiliary variables based on their Cohen’s D and residual correlations.

-Variables like BoxOffice, cognitive abilities (dn, crt, cfs), and vocabulary (vs) were identified as significant for both Vehicle and Approval forecasts.

-Age was categorized as not useful for mitigating bias or improving statistical power (Category C).
# CMAR Analysis
-Employed several CMAR methods including Bayesian models (brms), MLE (semTools), and rblimp, all showing consistent significant effects of Approval on Vehicle.

-PHEV effects were smaller and varied in significance across methods.

-The CMAR models provided better fit and lower residual variance compared to simple regression, with significantly better fit indicated by lower DIC2 and WAIC values.

-MCMC methods showed good convergence with trace plots indicating stable and consistent sampling, with chains exhibiting good mixing and stable fluctuations around a mean value.

# MNAR Analysis
-Estimated both focused and diffuse selection models for the missingness on the "Vehicle" variable.

-In the focused model, I included a limited set of predictors for missingness, typically one or a few key variables that I hypothesized may directly influence whether Vehicle data was missing.

-The diffuse model incorporated a broader range of variables to account for missingness, perhaps reflecting a more complex interaction between observed and unobserved factors.

# Comparison of CMAR and MNAR Models
-CMAR models consistently showed a strong positive effect of Approval on Vehicle and a more significant effect of PHEV than simple linear regression.

-The MNAR selection models were less favorable based on information criteria statistics, suggesting that CMAR was a superior modeling approach for your data.
