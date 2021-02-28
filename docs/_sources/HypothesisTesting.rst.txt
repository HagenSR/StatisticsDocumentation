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


Single Sample Hypothesis Tests​
===============================

Large Sample Test
-----------------

Take a random sample of size :math:`n \geq 30` from a population with mean :math:`\mu` and standard deviation :math:`\sigma`. We assume that either:
- :math:`\sigma` is known or
- :math:`S \approx \sigma` since n is Large

The hypothesis to be tested is :math:`H_{0}: \mu = \mu_{0}`

To begin with, we assume :math:`H_{0}` is true. The sample mean, :math:`\bar{X}` , is our best estimate of :math:`\mu` . We will use :math:`\bar{X}`
in its standardized form.

Test Statistic
--------------

.. math::
    Z = \frac{\bar{X} - \mu_{0}}{s/\sqrt{n}}

Z follows a standard normal distribution.

If :math:`H_{0}` is true the value of :math:`\bar{X}` should be close to :math:`\mu_{0}` and the test statistic will be close to zero. If :math:`H_{0}`
is false :math:`\bar{X}` will be much larger or smaller than :math:`\mu_{0}` and the test statistic will be large or small compared to zero, and then we 
should reject :math:`H_{0}` .

Rejection Regions
-----------------

The rejection region will vary depending on the alternative hypothesis. 

1. :math:`H_{a}: \mu \ne \mu_{0}` : reject :math:`H_{0}` for :math:`|Z| > Z_{a/2}`
   
2. :math:`H_{a}: \mu > \mu_{0}` : Reject :math:`H_{0}` for :math:`|Z| > Z_{a}` 
   
3. :math:`H_{a}: \mu < \mu_{0}` : Reject :math:`H_{0}` for :math:`|Z| < -Z_{a}`


Example:
--------

Rejection Region approach
-------------------------

The daily yield for a chemical plant has averaged 880 tons for several years. The quality control manager wants to know if this average has changed. 
She randomly selects 50 days and records an average yield of 871 tons with a standard deviation of 21 tons.​ Use 0.05 level of significance.

:math:`H_{0}: \mu = 880` , 

:math:`H_{a}: \mu \ne 880` , 

n = 50 :math:`\bar{X} = 871` s = 21

Test  Statistic: :math:`Z = \frac{\bar{X} - \mu_{0}}{s/\sqrt{n}} = \frac{871 - 880}{21/\sqrt{50}} = -3.03`

Critical  Value = :math:`Z_{a/2} = Z_{0.025} = 1.96`

Because :math:`|-3.03| > 1.96` We reject :math:`H_{0}` and conclude that there is sufficient evidence that the mean daily yield has changed and is 
no longer 880.

P value approach
----------------

Or we could use the p-value approach instead of finding a rejection region.

.. math::
    P-value = P(|Z| > |-3.03|) with \mu = 880
    = P(Z > 3.03) + P(Z < -3.03)
    = 2(0.0012)
    = 0.0024

P-value is 0.0024 < 0.05 = alpha Therefore we reject :math:`H_{0}` . 

Example
-------

Rejection region 
----------------

A random sample of 100 recorded deaths in the United States during the past year showed an average life span of 71.8 years. Assuming a population standard deviation of 8.9 years, 
does the data seem to indicate that the mean life span today is greater than 70 years?​ Use 0.10 level of significance.​

.. math::
    H_{0}: \mu = 70

    H_{a}: \mu > 70
    
    n = 100    \bar{X} = 71.8 \sigma = 8.9

    Test statistic: Z = \frac{\bar{X} - \mu_{0}}{s/\sqrt{n}} = \frac{71.8 - 70}{8.9/\sqrt{100}} = 1.28

Rejection Region: Reject :math:`H_{0}` if Z > 1.28​. Because 2.02 > 1.28 we reject :math:`H_{0}` and conclude that there is sufficient evidence that the average life span is greater than 70 years.

P value approach
----------------

Or we could use the p-value approach instead of finding a rejection region.

P-value = P(Z > 2.02) with :math:`\mu` = 70

= 0.0217

0.0217 < 0.1 = alpha. Therefore we reject :math:`H_{0}` .

Small Sample Test
==================

If the sample size is small (n < 30) we cannot make the assumption that S :math:`\approx \sigma` .
When :math:`\sigma` is unknown the test statistic we calculate will not follow a normal distribution,
but instead will follow a T-distribution. We are still performing a test on the population mean so the 
null hypothesis is still :math:`H_{0}: \mu = \mu_{0}` . 

Test Statistic:

.. math::
    T = \frac{\bar{X} - \mu_{0}}{s/\sqrt{n}}

This will follow a T-distribution with v = n-1 degrees of freedom.

Rejection Regions
-----------------

The rejection region will vary depending on the alternative hypothesis. 

1. :math:`H_{a}: \mu \ne \mu_{0}` : reject :math:`H_{0}` for :math:`|T| > t_{a/2}`
   
2. :math:`H_{a}: \mu > \mu_{0}` : Reject :math:`H_{0}` for :math:`|T| > t_{a}` 
   
3. :math:`H_{a}: \mu < \mu_{0}` : Reject :math:`H_{0}` for :math:`|T| < -t_{a}`

Example
-------

Rejection Region
----------------

It is claimed that a certain vacuum cleaner uses an average of 46 kilowatt hours per year. A random sample of 12 vacuums produced an average of 42 kilowatt hours per year with a standard deviation of 11.9 kilowatt hours.​
Does this sample suggest that this vacuum cleaner uses less than 46 kilowatt hours per year?​ Use 0.05 level of significance.​

.. math::
    H_{0}: \mu = 46

    H_{a}: \mu < 46
    
    n = 12    \bar{X} = 42 \sigma = 11.9

    Test statistic: T = \frac{\bar{X} - \mu_{0}}{s/\sqrt{n}} = \frac{42 - 46}{11.9/\sqrt{12}} = -1.16

    Critical Value: t_{a} = t_{0.05} = 1.796 (v = 11) 

Rejection Region: Reject :math:`H_{0}` if T < :math:`-t_{a}`

-1.16 > -1.796

Therefore we do not reject :math:`H_{0}` and conclude that the average kilowatt hours used annually by these vacuums is not significantly less than 46.

P Value
--------

When using the T-distribution it is difficult to find an exact p-value if we are not using computer software. We are only able to get a range for the p-value.​

P-value = P(T < -1.16) = P(T > 1.16) because t is symmetric.

0.10 < p-value < 0.15 (using the T table with v = 11)







