=========================
Hypothesis Testing
=========================

Introduction
============

A statistical hypothesis is an assertion or conjecture concerning one or more populations.​ The truth or falsity of a statistical hypothesis is never known with absolute 
certainty unless we examine the entire population.​ We take a random sample and determine if there is evidence to support the hypothesis or not.​

Consider a courtroom trial. The jury needs to decide between two possibilities:​

- The person is guilty​
- The person is not guilty​

To begin with, the person is assumed innocent. The prosecutor presents evidence trying to convince the jury to reject the original assumption.​

Null Hypothosis
---------------

Assumed to be true until we can prove otherwise.​

:math:`H_{0}` : The person is innocent.

Alternative Hypothesis
-----------------------

What we believe to be true if we can disprove :math:`H_{0}`

:math:`H_{a}` : The person is guilty

Parts of a statistical Test
===========================

Test Statistic
--------------
A single statistic calculated from the sample which will allow us to make a decision about :math:`H_{0}`

Rejection region (Critical Region)
-----------------------------------

A rule that tells us for which values of the test statistic the null hypothesis should be rejected

Critical value
--------------

The last number that we observe in passing into the critical region.​

Conclusion
----------

If we have data that the null hypothesis is not true our conclusion is “Reject :math:`H_{0}` ”. (in favor of :math:`H_{a}` because of sufficient evidence in the data)​
Otherwise, the conclusion is “Do not reject :math:`H_{0}` ”. (insufficient evidence in the data)​ The conclusion should also contain a statement about the reliability 
of your conclusion.​

Note: You do not “accept” :math:`H_{0}` . EX In the courtroom if there is insufficient evidence, the conclusion is “not guilty”.​ The conclusion is not that the person 
is “innocent”.​

Types of Error
==============

Type 1 Error
-------------

Rejection of the null hypothesis when it is actually true.

Type 2 Error
------------

Fail to reject the null hypothesis when it is actually false.​

==================== ======================= =======================
         X             Null Hypothesis True   Null Hypothesis False
==================== ======================= =======================
   Do not reject        Correct decision       Type II Error
   Reject               Type I Error           Correct decision
==================== ======================= =======================

P(Type I Error) = :math:`a` = level of significance. :math:`a` is controlled by the experimentor and is set before the test is conducted.

P(Type II Error) = :math:`B` . :math:`B` Is difficult to calculate. We need a specific value for our alternative, :math:`H_{a}` . 
- Ideally, we would like to use a test procedure for which :math:`a` and :math:`B` are small. However the two types of error are related and a decrease in one generally results in an increase of the other.
- But we do have control of :math:`a` (the critical region), So we can reduce the probability of committing type I error by adjusting the critical value.​
- An Increase in the sample size, n, will reduce :math:`a` and :math:`B` simultaneously
- If the null hypothesis is falce, :math:`B` is a maximum when the true value of the parameter approaches the hypothesized value. The greater the distance between the true value and the hypothesized value, the smaller :math:`B` will be.

Power
------

The power of a test is the probability of rejecting :math:`H_{0}` when a specific :math:`H_{a}` is true.

.. math::
    Power = 1 - B

Ex Power = 0.1339

Our test properly rejects :math:`H_{0}` 13.39% of the time. (not a good test)

Writing Hypotheses
------------------

The null hypothesis contains a statement of equality.    “=”​

The alternative hypothesis is somewhat a complement to the null hypothesis. It is a statement that must be true if H0 is false. It contains a statement of inequality.    “<, >, ≠”​

Ex 1:

A university claims that the proportion of students who graduate in 4 years is 80%. Test if the university is correct.

.. math::
    H_{0}: p = 0.80

    H_{a}: p != 0.80

Ex 2: 

A tire manufactureer claims that the mean life of a certain tire is less than 50,000 miles.

.. math:: 
    H_{0}: \mu = 50,000

    H_{a}: \mu < 50,000

One and Two tailed tests
========================

One tailed test
----------------

A test of any statistical hypothesis where the alternative is one-sided is caleed a one-tailed test.

Ex:

.. math::
    H_{0}: \mu = 50,000

    H_{a}: \mu < 50,000

has a left tail.

Ex:

.. math::
    H_{0}: p = 0.25

    H_{a}: p > 0.25

has a right tail.

The critical region will lie within one tail of the distribution. 

Two tailed tests
----------------

A test of any statistical hypothesis where the alternative is two-sided is called a two-tailed test.

Ex:

.. math::
    H_{0}: \mu = 40

    H_{a}: \mu != 40

The critical region will be split into two parts because we would reject for :math:`\mu` < 40 or :math:`\mu` > 40

Making a decision
-----------------

We will make a decision on the null hypothesis in one of two ways

1. Using the Test Statistic

We will reject :math:`H_{0}` if the test statistic falls within the rejection region. Formulas for test statistics and how to find the rejection region will be defined for different types of tests

2. Using the P-Value
   
The probability of obtaining our calculated test statistic value, given that the null hypothesis is true, is the P-value. In other words, the p-value gices a measure of how likely it is to obtain 
the sample data if :math:`H_{0}` is true. We will reject :math:`H_{0}` if the p-value is less than :math:`a` ie p-value < :math:`a` reject.



