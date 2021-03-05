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
   
2. :math:`H_{a}: \mu > \mu_{0}` : Reject :math:`H_{0}` for :math:`Z > Z_{a}` 
   
3. :math:`H_{a}: \mu < \mu_{0}` : Reject :math:`H_{0}` for :math:`Z < -Z_{a}`


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
   
2. :math:`H_{a}: \mu > \mu_{0}` : Reject :math:`H_{0}` for :math:`T > t_{a}` 
   
3. :math:`H_{a}: \mu < \mu_{0}` : Reject :math:`H_{0}` for :math:`T < -t_{a}`

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

Two Sample Hypothesis Tests​
===============================

Large Sample Test
-----------------

Two independent random samples are drawn. The first sample is size :math:`n_{1}` from a population with mean :math:`\mu_{1}` and variance :math:`\sigma_{1}^2` . 
The second sample is size :math:`n_{2}` from a population with mean :math:`\sigma_{0}^2` . The hypothesis of interest involves the difference :math:`\mu_{1} - \mu_{2}` .
:math:`H_{0}: \mu_{1} - \mu{2} = d_{0}` . Where :math:`d_{0}` is some hypothesized difference (usually zero).

If :math:`n_{1}` and :math:`n_{2}` are both greater than thirty we can make one of two assumptions:

1. :math:`\sigma_{1}^2` and :math:`\sigma_{2}^2` are known
2. Or :math:`s_{1}^2 \approx \sigma_{1}^2` and :math:`s_{2}^2 \approx \sigma_{2}^2` 

We can now use the standard normal distribution for our test statistic.

If :math:`n_{1}` and :math:`n_{2}` are both greater than thirty, the test statistic used for the hypothesis test given by the null hypothesis:
:math:`H_{0}: \mu_{1} - \mu{2} = d_{0}`

.. math::
    Z = \frac{(\bar{X_{1}} -\bar{X_{2}}) - d_{0}}{\sqrt{\frac{s_{1}^2}{n_{1}} + \frac{s_{2}^2}{n_{2}}}}

The test will follow a standard normal distribution.

Rejection Regions
------------------

The rejection region will vary depending on the alternative hypothesis. 

1. :math:`H_{a}: \mu_{1} - \mu_{2} \ne d_{0}` : reject :math:`H_{0}` for :math:`|Z| > Z_{a/2}`
   
2. :math:`H_{a}: \mu_{1} - \mu_{2} > d_{0}` : Reject :math:`H_{0}` for :math:`Z > Z_{a}` 
   
3. :math:`H_{a}: \mu_{1} - \mu_{2} < d_{0}` : Reject :math:`H_{0}` for :math:`Z < -Z_{a}`


Small sample Test
------------------

Two independent random samples of sizes :math:`n_{1}` and  :math:`n_{2}` are drawn. If  :math:`n_{1}` and  :math:`n_{2}` are both less than thirty we cannot 
make the assumption that :math:`s_{1}^2 \approx \sigma_{1}^2` and :math:`s_{2}^2 \approx \sigma_{2}^2` . If we can assume that the population variances are equal, 
our test statistic will follow a T-distribution instead of standard normal. The null hypothesis is still :math:`H_{0}: \mu_{1} - \mu{2} = d_{0}`

If  :math:`n_{1}` and  :math:`n_{2}` are both less than thirty, the test statistic used for the hypothesis test given by the null hypothesis: :math:`H_{0}: \mu_{1} - \mu{2} = d_{0}`

.. math::
    T = \frac{(\bar{X_{1}}-\bar{X_{2}})-d_{0}}{S_{p}\sqrt{\frac{1}{n_{1}}+\frac{1}{n_{2}}}}


    S_{p}^2 =\frac{(n_{1}-1)s_{1}^2 + (n_{2}-1)s_{2}^2}{n_1+n_2-2} 

The test statistic will follow a T-distribution with :math:`n_{1} + n_{2} - 2` degrees of freedom. Please note that if the population variances cannot be assumed equal the T-distribution is
much more difficult to estimate. Computer software is usually used in those cases.

Rejection Regions
-----------------

For :math:`n_{1}` and :math:`n_{2}` less than thirty and population variances equal we have:

1. :math:`H_{a}: \mu_{1} - \mu_{2} \ne d_{0}` : reject :math:`H_{0}` for :math:`|T| > t_{a/2}`
   
2. :math:`H_{a}: \mu_{1} - \mu_{2} > d_{0}` : Reject :math:`H_{0}` for :math:`T > t_{a}` 
   
3. :math:`H_{a}: \mu_{1} - \mu_{2} < d_{0}` : Reject :math:`H_{0}` for :math:`T < -t_{a}`

Paired Observations
-------------------

As we have previously seen, sample variance can be reduced by creating an experiment with paired observations. EX: weight before vs weight after, Different tire brands on same car.
For paired observations we are interested in the quantity: :math:`\mu_{D} = \mu_{1} - \mu_{2}`

If we have an experiment with paired observations the null hypothesis is: :math:`H_0: \mu_D = d_0`

.. math:: 
    T = \frac{\bar{d} - d_0}{s_d / \sqrt{n}}

This test statistic will follow a T-distribution with v = n - 1 degrees of freedom.

Rejection Regions
-----------------

The rejection region will vary depending on the alternative hypothesis. 

1. :math:`H_{a}: \mu_d \ne d_{0}` : reject :math:`H_{0}` for :math:`|T| > t_{a/2}`
   
2. :math:`H_{a}: \mu_d > d_{0}` : Reject :math:`H_{0}` for :math:`T > t_{a}` 
   
3. :math:`H_{a}: \mu_d < d_{0}` : Reject :math:`H_{0}` for :math:`T < -t_{a}`



Tests Involving proportions
===========================

Test on proportions are important in many areas.​ Politicians are concerned with the percentage of voters who favor them.​ Manufacturers need to know the proportion of defective items 
being produced.​ We will consider the problem of testing that the proportion is equal to some specified value, :math:`H_0: p = p_0` 

A random sample of size n from a binomial population to test  :math:`H_0: p = p_0` the test statistic is calculated as:

.. math::
    Z = \frac{\hat{p} - p_0}{\sqrt{\frac{p_0 q_0}{n}}}

Where  :math:`\hat{p}` is the number of successes divided by n. This test statistic will follow a standard normal distribution. 

Rejection Regions
-----------------

The rejection region will vary depending on the alternative hypothesis. 

1. :math:`H_{a}: p \ne p_{0}` : reject :math:`H_{0}` for :math:`|Z| > Z_{a/2}`
   
2. :math:`H_{a}: p > p_{0}` : Reject :math:`H_{0}` for :math:`Z > Z_{a}` 
   
3. :math:`H_{a}: p < p_{0}` : Reject :math:`H_{0}` for :math:`Z < -Z_{a}`


**Example**

A commonly prescribed drug is believed to be only 60% effective. A random sample of 100 adults taking this drug show a 70% effective rate.
 Is this sufficient evidence to conclude that the drug is preforming better than originally thought?​

Use 0.05 level of significance.

.. math::
    n = 100     \hat{p} = 0.70

    H_0: p = 0.60

    H_a: p > 0.60 

    Test statistic: Z = \frac{\hat{p}-p_0}{\sqrt{\frac{p_0 q_0}{n}}} = \frac{0.70 - 0.60}{\sqrt{\frac{0.60(0.40)}{100}}}

Rejection Region: Reject :math:`H_{0}` if Z > :math:`Z_{a}`

2.04 > 1.645

Reject :math:`H_{0}` . There is sufficient evidence (at level 0.05) that the drug is performing better than it was originally believed.

P-value = P(Z > 2.04) = 1 - P(Z < 2.04)

= 1 - 0.9793

0.0207 < 0.05

Reject :math:`H_{0}`

Test on the Difference of Two Proportions:
===========================================

If we take two independent samples from two different binomial populations generally we are interested in whether the two population proportions are
equal. :math:`H_{0}: p_1 = p_2` Which would be equivalent to testing:  :math:`H_{0}: p_1 - p_2`

Thus we will use the sampling distribution for  :math:`\hat{p}_1 - \hat{p}_2` to determine the appropriate test.

A sample size of :math:`n_1` results in :math:`x_1` successes. 

A sample size of :math:`n_2` results in :math:`x_2` successes. 

:math:`\hat{p_1} = \frac{x_1}{n_1}` and :math:`\hat{p_2} = \frac{x_2}{n_2}`

:math:`H_0: p_1 = p_2`

When :math:`H_0` is true, :math:`p_1 = p_2 = p` we have a pooled estimate of the proportion p.

.. math::
    \hat{p} = \frac{x_1 + x_2}{n_1 + n_2}

    H_0: p_1 = p_2

The test statistic is calculated as:

.. math::

    Z = \frac{\hat{p_1} - \hat{p_2}}{\sqrt{\hat{p}\hat{q}(\frac{1}{n_1}+\frac{1}{n_2})}}

This will follow the standard normal distribution.


Rejection Regions
-----------------

The rejection region will vary depending on the alternative hypothesis. 

1. :math:`H_{a}: p_1 \ne p_{2}` : reject :math:`H_{0}` for :math:`|Z| > Z_{a/2}`
   
2. :math:`H_{a}: p_1 > p_{2}` : Reject :math:`H_{0}` for :math:`Z > Z_{a}` 
   
3. :math:`H_{a}: p_1 < p_{2}` : Reject :math:`H_{0}` for :math:`Z < -Z_{a}`


**Example**

Use the information in the table below to test whether the first population has a higher probability of success than the second population at a level of 0.05.

==================== ====================
    Sample 1            Sample 2
==================== ====================
:math:`n_1` = 200     :math:`n_2` = 500 
:math:`x_1` = 120     :math:`x_2` = 240     
==================== ====================

:math:`\hat{p}_1 = \frac{120}{200}` = 0.6 and :math:`\hat{p}_2 = \frac{240}{500}` = 0.48

:math:`\hat{p} = \frac{120 + 240}{200 + 500} = \frac{360}{700}` = 0.51

:math:`H_0: p_1= p_2`

:math:`H_a: p_1 > p_2`

Test Statistic:

.. math::
    Z = \frac{0.6 - 0.48}{\sqrt{0.51(0.49)(\frac{1}{200} + \frac{1}{500})}} = 2.87

**Example**

Critical Value :math:`Z_\alpha = Z_0.005 = 1.645`

Rejection Region: Reject :math:`H_0` if :math:`Z > Z_a`

2.87 > 1.645

Reject :math:`H_0`. There is sufficient evidence (at 0.05) that the first population proportion is greater than the second population proportion.

P Value = P(Z > 2.87) 
        = 1 - P(Z < 2.87)
        = 1 - 0.9979
        = 0.0021

0.0021 < 0.05

Reject :math:`H_0`