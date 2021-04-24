================
ANOVA
================


Analysis of Variance (ANOVA) is a procedure whereby the total variation in the dependent variable, Y, is subdivided into meaningful components that are then observed and treated in a systematic fashion.

Total variation in Y = SST = Syy 

Explanation of variation
--------------------------

We wish to divide the total variation in Y into meaningful subdivisions.

SSE = SST – b1Sxy 
SST = b1Sxy + SSE

SSE measures the error variation, or the variation in Y that is not explained by the model.
The quantity b1Sxy measures the variation in Y that is explained by the model.

Regression Identity
--------------------

The regression identity is:

SST = SSR + SSE

Where

SST = total variation in Y

SSR = b1Sxy = variation explained by using X in the model

SSE = leftover variation not explained by X

Now we have another formula for calculating the coefficient of determination.

R2 = 𝑆𝑆𝑅/𝑆𝑆𝑇

Previously we had:

R2 = 1−𝑆𝑆𝐸/𝑆𝑆𝑇

Anova Table
-------------

The division of variation is usually displayed in an Analysis of Variation table.

=================== =================== =================== =================== ===================
Source                  DF                      SS                  MS                  F 
=================== =================== =================== =================== ===================
Regression           1(number of vars)    SSR                       MSR                 MSR/MSE 
ERROR                 n-2                   SSE                     MSE                 
TOTAL                   n-1                 SST 
=================== =================== =================== =================== ===================

We have divided the total variation into two sources: Regression and Error.

Each source has its own degrees of freedom.
Error has (n – 2) degrees of freedom because two parameters, 𝛽_0 and 𝛽_1, are estimated when we created a fitted regression line.
Regression has (1) degree of freedom because we are only using one independent variable, X, in our creation of the fitted regression line.

The regression identity states:
SST = SSR + SSE
The total variation can be found as a sum of the two divisions of variation. The degrees of freedom for the total variation can be found similarly.
1 + (n – 2) = (n – 1)
Thus the total degrees of freedom for the analysis is (n – 1).

Mean Squares 
------------

If we divide each source of variation by its associated degrees of freedom we get an estimate of the variation in the experiment.
These estimates are called mean squares (MS).
MSR = 𝑆𝑆𝑅/1
MSE = 𝑆𝑆𝐸/(𝑛−2) = s^2

F value
--------

The F-value given in the last column of the ANOVA table is found by taking MSR divided by MSE.
This value is a statistic that will follow an       F-distribution with v1 = 1, and v2 = (n – 2) degrees of freedom.

The F Test
============

H0: The model is not useful in predicting Y
Ha: The model is useful in predicting Y
(OR H0: 𝛽_1= 0   vs. Ha: 𝛽_1 ≠ 0 )

Test statistic: 𝐹=𝑀𝑆𝑅/𝑀𝑆𝐸
Critical value: fα(1, n - 2)
Reject H0 if F > fα 

(For simple linear regression, this test is equivalent to the T-test for H0: 𝛽_1= 0)

**Example**

Fill out an ANOVA table for the appliance store example data. Perform an F-test to determine if the model is useful at the 0.05 level.

========= =========
    X          Y
========= =========
1             1
2             1
3             2
4             2
5             4
========= =========

SSE = 1.1
SST = 6

Then 

=================== =================== =================== =================== ===================
Source                  DF                      SS                  MS                  F 
=================== =================== =================== =================== ===================
Regression                  1                  4.9                  4.9                 13.36
ERROR                       3                  1.1                  0.3667                 
TOTAL                       4                  6 
=================== =================== =================== =================== ===================

H0: The model is not useful in predicting Y

Ha: The model is useful in predicting Y

Test statistic: F = 13.36

Critical value: f0.05(1, 3) = 10.1

Reject H0 if F > 10.1

13.36 > 10.1

Reject H0. At the 0.05 level we conclude that X is useful in predicting Y. (advertising expenditure is useful in predicting sales revenue)



