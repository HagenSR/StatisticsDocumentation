=======================================
Models with Qualitative variables
=======================================

Qualitative variables are variables that cannot be measured numerically.
These variables are often called categorical because they have different categories.
i.e. gender, eye color, marital status

Multiple regression requires that the response Y be a quantitative variable (measured numerically).
Independent variables can be either quantitative or qualitative. 
Qualitative variables are entered into a regression model through the use of dummy variables (or indicator variables).

Using Indicator variables
--------------------------

If a qualitative variable involves r categories, or levels, then (r – 1) indicator variables should be added to the regression model.

**Example**

Data was collected on 12 assistant professors (6 male and 6 female). Their salaries, years of experience, and gender were recorded. We wish to create a 
model to predict salary based on experience and gender.

Y = Salary

X_1 = Years of Experience

Need to create dummy variables for gender.

Gender has two categories, thus we need (2 – 1) = 1 dummy variable.

Z1 = {(1, 𝑚𝑎𝑙𝑒 | 0, 𝑓𝑒𝑚𝑎𝑙𝑒)}

Our model can now be written as:

.. math::
    𝑌=𝛽_0+𝛽_1 𝑋_1+𝛽_2 𝑍_1+𝜀

Expected Value of Y:

For males: 

.. math::
    E(Y) = 𝛽_0+𝛽_1 𝑋_1+𝛽_2 (1)

    = (𝛽_0+𝛽_2)+𝛽_1 𝑋_1

For females: 

.. math::
    E(Y) = 𝛽_0+𝛽_1 𝑋_1+𝛽_2 (0)

    = 𝛽_0+𝛽_1 𝑋_1

**Example - Two Categories**

A model with categorical variables essentially involves a change in the intercept as we change from one category to another.

.. image:: _static/images/twoCat.png
   :width: 400
   :height: 300

**Example – Three Categories**

An employer plans to use a multiple regression model to predict annual sales (in $1000) for members of her sales staff. She wants to include a categorical variable to indicate an individual’s highest level of education. 
The possible categories are: high school degree, some college, college degree.

Indicator Variables:
Since we have 3 categories we need 2 indicator variables.

Z1 = {(1, 𝑠𝑜𝑚𝑒 𝑐𝑜𝑙𝑙𝑒𝑔𝑒 | 0, 𝑜𝑡ℎ𝑒𝑟𝑤𝑖𝑠𝑒)}

Z2 = {(1, 𝑐𝑜𝑙𝑙𝑒𝑔𝑒 𝑑𝑒𝑔𝑟𝑒𝑒 | 0, 𝑜𝑡ℎ𝑒𝑟𝑤𝑖𝑠𝑒)}

Another way to visualise this relationship is with a table

==================== =========== ===========
         Cat             Z_1          Z_2
==================== =========== ===========
Highschool Degree          0        0
Some college               1        0
College Degree             0        1
==================== =========== ===========

If there are no other variables, our model would be:

.. math::
    𝑌=𝛽_0+𝛽_1 𝑍_1+𝛽_2 𝑍_2+𝜀

The change in the intercept is seen below

.. image:: _static/images/threeCat.png
   :width: 400
   :height: 300

Suppose regression results show a coefficient of 8.2 for Z1 and 12.7 for Z2.
How can we interpret these estimated coefficient values?

The category “high school degree” has both of the indicator variables take on a value of zero.
This means that high school degree serves as a base to which the other categories can be compared.

.. math::
    \hat{𝑦} = 𝑏_0+𝑏_1 𝑧_1+𝑏_2 𝑧_2

For high school degree:

.. math::
    \hat{𝑦} = 𝑏_0+𝑏_1 (0)+𝑏_2 (0) = b0

For some college:

.. math::
    \hat{𝑦} = 𝑏_0+𝑏_1 (1)+𝑏_2 (0) = b0 + b1 

The difference between having “some college” and having “high school degree” is (b0 + b1) – b0 = b1

In our example b1 = 8.2

We can associate having “some college” with an added $8,200 in annual sales when compared to having only a “high school degree”

(This is only based on sample data and our results are only estimates)

For college degree:

.. math::
    \hat{𝑦} = 𝑏_0+𝑏_1 (0)+𝑏_2 (1) = b0 + b2 

The difference between having “college degree” and having “high school degree” is (b0 + b2) – b0 = b2 = 12.7
We can associate having a “college degree” with an added $12,700 in annual sales when compared to having only a “high school degree”

The difference between having “college degree” and having “some college” is   

(b0 + b2) – (b0 + b1) = (b2 – b1) 

= 12.7 – 8.2

= 4.5

We can associate having a “college degree” with an added $4,500 in annual sales when compared to having only “some college”

Varying Slope with Indicator Categories
========================================

The way we created our model with categorical variables is by simply adding them in as another factor. This suggests that the slopes are constant across categories.
This is not always going to be the case.
We can account for the possibility of varying slopes by including the product (or interaction) terms between indicator terms and continuous variables.

Let’s look at the example dealing with professor’s salary.

Previously our model was:

.. math::
    𝑌=𝛽_0+𝛽_1 𝑋_1+𝛽_2 𝑍_1+𝜀

Where:

Y = Salary

X1 = Years of Experience

Z1 = 1 for males; 0 for females

If we think the slope could be different for males and females we would add the interaction term: X1*Z1 

Our model then becomes:

.. math::
    𝑌=𝛽_0+𝛽_1 𝑋_1+𝛽_2 𝑍_1+𝛽_3 𝑋_1 𝑍_1+𝜀

This interaction term allows the two independent variables to interact.

This allows the relationship between Salary and Years of Experience to behave differently for men and women.

When the faculty member is a woman:

.. math::
    E(Y) = 𝛽_0+𝛽_1 𝑋_1+𝛽_2 (0)+𝛽_3 𝑋_1 (0)

    =𝛽_0+𝛽_1 𝑋_1

This is a straight line with slope = 𝛽_1 and intercept = 𝛽_0

When the faculty member is a man:

.. math::
    E(Y) = 𝛽_0+𝛽_1 𝑋_1+𝛽_2 (1)+𝛽_3 𝑋_1 (1)

    =(𝛽_0+𝛽_2)+(𝛽_1+𝛽_3)𝑋_1

This is a straight line with slope = (𝛽_1+𝛽_3)  and intercept = (𝛽_0+𝛽_2)

.. image:: _static/images/changingSlope.png
   :width: 400
   :height: 300
   
Test For Parallelism
---------------------

We can test for the condition of parallelism by testing if the interaction term is significant in the model.
If the interaction term is not significant, the slopes would be the same for all of the categories (the lines would be parallel).

In the previous example the coefficient of the interaction term was 𝛽_3, so our test for parallelism would be:

H0: :math:`𝛽_3` = 0    (slopes are the same)

Ha: :math:`𝛽_3` ≠ 0    (slopes are different)

Test statistic: :math:`T = \frac{𝑏_3}{(𝑆𝐸(𝑏_3))}`

Critical value: 𝑡_(𝛼/2)  (with v = n – k – 1) 

If we reject H0, we conclude that there is evidence that the interaction term is significant in the model. (There is evidence that the slopes are different).

The Partial F Test
===================

Given a model with 3 or more independent variables, we can test if portions of the model are significant (when taken together).

For example, given the model:

.. math::
    Y = β_0 + β_1X_1 + β_2X_2 + β_3X_3 + β_4X_4 + ε

We can test if X_3 and X_4 are significant to the model when taken together.

Testing if X_3 and X_4 are significant to the model when taken together is not the same as testing each variable individually with a T-test.

What we are trying to test is:

:math:`H0 : β_3 = β_4 = 0` 

:math:`H_a` : at least one :math:`β_i ≠ 0`

This test will be  similar to the F-test because we are trying to test more than one variable at a time. 
We will call this the Partial F-test since we are only testing some of the parameters.
            
When testing a subset of variables we are essentially comparing two different models:
Full model contains all of the independent variables.
Reduced model does not have the variables that you are trying to test.

**Example**

We have created a model to predict Y using four independent variables ( :math:`X_1, X_2, X_3, X_4` ). We want to test if X3 and X4 are significant to the model when taken together.

Full model:

.. math::
    Y = β_0 + β_1X_1 + β_2X_2 + β_3X_3 + β_4X_4 + ε

Reduced Model:

.. math::
    Y = β_0 + β_1X_1 + β_2X_2 + ε

We then run regressions on both models (full and reduced) to get the necessary information for the Partial F-test

To perform a partial F-test we calculate:

.. math::
    𝐹^∗=\frac{\frac{(𝑆𝑆𝐸_𝑅−𝑆𝑆𝐸_𝐹)}{(𝑘_𝐹−𝑘_𝑅)}}{(𝑀𝑆𝐸_𝐹)}

R signifies that the values are coming from the Reduced model.

F signifies Full model.

:math:`𝑘_𝐹−𝑘_𝑅` = the number of betas being tested

We can reject :math:`H_0` if :math:`F* > f_𝛼` 

With :math:`v_1 = (k_F – k_R) and v_2 = [n – (k_F + 1)]` .

The numerator degrees of freedom is the number of betas being tested.

The denominator degrees of freedom is the degrees of freedom for error from the full model.

Conclusions
------------

If we reject :math:`H_0` then the variables are significant when taken together, and should not be removed from the model. (the full model should be used)

If we do not reject :math:`H_0` then the variables are not significant when taken together and the variables tested can be removed from the model. (the reduced model should be used)

**Example**

A multiple linear regression was performed to fit a model with 8 independent variables.

.. math::
    Y = β_0 + β_1X_1 + β_2X_2 + β_3X_3 + β_4X_4 + β_5X_5 

    + β_6X_6+ β_7X_7+ β_8X_8+ ε
  
The sample size is n = 25.

We believe variables X_2, X_3, X_6, and X_7 are not significant in the model when taken together.

Perform a partial F-test.

Full Model
	Y = β_0 + β_1X_1 + β_2X_2 + β_3X_3 + β_4X_4 + β_5X_5 
			+ β_6X_6+ β_7X_7+ β_8X_8+ ε
  
ANOVA

=================== =================== =================== =================== ===================
Source                  DF                      SS                  MS                  F 
=================== =================== =================== =================== ===================
Regression                  8                  528                  66                 4.14
ERROR                       16                 255                  15.9375                 
TOTAL                       24                 783 
=================== =================== =================== =================== ===================

Reduced model:

.. math::
    Y = β_0 + β_1X_1 + β_4X_4 + β_5X_5 + β_8X_8+ ε

ANOVA

=================== =================== =================== =================== ===================
Source                  DF                      SS                  MS                  F 
=================== =================== =================== =================== ===================
Regression                  4                  456                  144                 6.97
ERROR                       20                 327                  16.35                 
TOTAL                       24                 783 
=================== =================== =================== =================== ===================

:math:`H_0: 𝛽_2=𝛽_3=𝛽_6=𝛽_7=0`

:math:`H_a:` at least one :math:`𝛽_𝑖≠0`

.. math::

    𝐹^∗=\frac{\frac{(𝑆𝑆𝐸_𝑅−𝑆𝑆𝐸_𝐹)}{(𝑘_𝐹−𝑘_𝑅)}}{(𝑀𝑆𝐸_𝐹)}

    =\frac{\frac{(327−255)}{(8−4)}}{(15.9375)}

    =1.13

Critical value: :math:`f_{0.05} = 3.01 (v_1 = 4, v_2 = 16)`

Reject H0 if F > 3.01

1.13 < 3.01

Do not reject :math:`H_0` . There is not evidence that the selected variables are significant to the model when taken together. (The reduced model should be used)


Selection Procedures
======================

Building a model
-------------------

Usually, we have a good idea which independent variables to use in a model.
We have several variables or terms that could be used in a model, some of which are significant and some are not.
We would like to find a subset of these variables that does the “best” possible job of predicting y (without including insignificant variables)

We want to reduce the number of variables so that the resulting regression equation is easy to understand, interpret and work with.
Thus we only include the most significant variables. 
Overall, we want as few variables as possible in the final regression equation while at the same time retaining the ability to effectively predict Y.

Finding a subset of variables to predict Y is often referred to as the variable selection problem.

Selection Methods:

- Forward Selection
- Backward Elimination
- Stepwise Regression

Each method has a series of steps which will lead you to the optimal model.

Forward Selection 
------------------

At first the model only contains the intercept, β0. At each step, at most one variable can be added to the model. 

Step 1:

Fit a simple linear regression model with each of the potential independent variables. Choose the variable that is most significant (has the largest R2, or has the largest T-statistic, or has the lowest p-value)

Step 2:

Find the variable that, when inserted in the model found in the previous step, gives the largest increase in R2 (the most significant variable possible)
If this variable is insignificant based on some predetermined α, the procedure stops.

Step 3:

The procedure continues until no variable considered for addition to the model provides a significant increase in R2.
(until the next variable to be added is insignificant compared to α) 

Backward Elimination
---------------------

Backward elimination starts with all independent variables in the model. At each step at most one variable is eliminated from the model.

Step 1:

Fit a regression equation with all independent variables included. Choose the variable that is the most insignificant (has the smallest T-statistic, or has the largest p-value). If this variable is insignificant compared to some predetermined α, it is eliminated from the model.

Step 2:

Fit a regression equation using all variables except the one that was eliminated in the previous step.
Choose the variable that is the most insignificant (has the smallest T-statistic). If this variable is insignificant compared to some predetermined α, it is eliminated from the model. If this variable is significant, the procedure stops.

Step 3:

The procedure continues until a variable selected for elimination is found to be significant.

Stepwise Regression
----------------------

Stepwise regression combines forward selection and backward elimination in the following way:

Step 1:

Start with only the intercept, β0, in the model. At each step the forward selection method is used in an attempt to add a variable into the model. 
If no variables are added, the process stops.

Step 2:

After a variable is added to a model already containing at least one variable, then employ one step of the backward elimination method on the model containing all of the 
entered variables. If a variable is removed it is returned to the collection of un-entered variables.
Continue until no variables are added or eliminated.

Level Of Significance
----------------------

It is common to use a level of significance of α = 0.15.
So for forward selection a variable is only added if its p-value is less than 0.15.
For backward elimination a variable is only eliminated if its p-value is greater than 0.15.

Note that These selection procedures fit first order models and are not helpful in detecting curvature or interaction in the data.



