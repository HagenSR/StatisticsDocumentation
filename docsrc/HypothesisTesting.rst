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

p-value
--------

P Value = P(Z > 2.87) 
        = 1 - P(Z < 2.87)
        = 1 - 0.9979
        = 0.0021

0.0021 < 0.05

Reject :math:`H_0`

Tests involving variance
=========================

When the primary parameter of interest is sample variance, :math:`\sigma^2` , we use the sample standard deviation :math:`s^2` to estimate values 
of the parameter. We choose a sample of size n from a normal distribution. The sampling distribution of :math:`s^2` is given by standardizing with
the formula:

.. math::
    \chi^2 = \frac{(n-1)S^2}{\sigma^2_0}

Which has a chi-square distribution with v = n-1

Rejection Regions
-----------------

The rejection region will vary depending on the alternative hypothesis. 

1. :math:`H_{a}: \sigma^2 \ne \sigma_{0}^2` : reject :math:`H_{0}` for :math:`\chi^2 < \chi^2_{1-\alpha/2}` or :math:`\chi^2 > \chi^2_{a/2}`
   
2. :math:`H_{a}: \sigma^2 > \sigma_{0}^2` : Reject :math:`H_{0}` for :math:`\chi^2 > \chi^2_{\alpha}` 
   
3. :math:`H_{a}: \sigma^2 < \sigma_{0}^2` : Reject :math:`H_{0}` for :math:`\chi^2 < \chi^2_{1-\alpha}`


**Example**

A certain mechanical process claims to have a variance of 10 units :math:`^2` . A sample of 12 is found to have a variance of 13.96. Test whether the variance
is significantly higher than previously claimed. Use 0.05 level of significance.

:math:`H_{0}: \sigma^2 = 10`

:math:`H_{a}: \sigma^2 > 10`

n = 12                  :math:`s^2 = 13.96`

Test Statistic:

.. math:: 
    \chi^2 = \frac{11(13.96)}{10} = 15.356

Critical value: :math:`\chi^2_{\alpha} = \chi^2_{0.05} = 19.675` using v = 11 

Rejection Region: Reject :math:`H_0` if :math:`\chi^2 > 19.675`

Since 15.356 < 19.675, we do not reject :math:`H_0` . There is not sufficient evidence, at 0.05 level, that the population variance is more than 10.

P-Value
---------

P-Value = :math:`P(\chi^2 > 15.356)` . Go to the chi-squared table and find the row with 11 degrees of freedom. Find where 15.356 would lie on that row,
this gives a range for the p-value. 

:math:`0.10 < P(\chi^2 15.356) < 0.20` . So 0.10 < p-value < 0.20. This is greater than 0.05 so we do not reject :math:`H_0` .

Two Sample Test
----------------

For independent random samples of sizes :math:`n_1` and :math:`n_2` from two normal populations with variances :math:`\sigma^2_{1}` and :math:`\sigma^2_{2}`
we are interested in testing if the two population variances are equal. Thus, our null hypothesis is: :math:`H_0: \sigma^2_{1} = \sigma^2_{2}`

We will use the ratio of two variances to find a test statistic.

When testing the hypothesis: :math:`H_0: \sigma^2_{1} = \sigma^2_{2}` our test statistic is given by:

.. math::
    F = \frac{s^2_1}{s^2_2}

This will follow an F-distribution with :math:`V_1 = n_1 - 1` and :math:`V_2 = n_2 - 1` degrees of freedom.

Rejection Regions
-----------------

The rejection region will vary depending on the alternative hypothesis. 

1. :math:`H_{a}: \sigma^2_{1} \ne \sigma_{2}^2` : reject :math:`H_{0}` for :math:`F > f_{\alpha/2}` or :math:`F < f_{1-\alpha/2}`
   
2. :math:`H_{a}: \sigma^2_1 > \sigma_{2}^2` : Reject :math:`H_{0}` for :math:`F > f_{\alpha}` 
   
3. :math:`H_{a}: \sigma^2_1 < \sigma_{2}^2` : Reject :math:`H_{0}` for :math:`F < f_{1-\alpha}`


**Example**

An experiment was performed to compared the abrasive wear of two different laminated materials. It is believed that the two populations have equal variances.​
A sample of 11 is taken with the first material and found to have a variance of 16.​ A sample of 10 is taken with the second material and found to have a 
variance of 25.​

Test if the two population variances are equal or not at 0.10 level.

:math:`H_{0}: \sigma^2_{1} = \sigma_{2}^2`

:math:`H_{a}: \sigma^2_{1} \ne \sigma_{2}^2`

:math:`n_1 = 11`      :math:`s_1^2 = 16`
:math:`n_12 = 10`     :math:`s_2^2 = 25`

Test Statistic = :math:`F = \frac{16}{25}` = 0.64

Critical values = :math:`f_{\alpha/2} = f_{0.1/2} = f_{0.05}(10,9) = 3.14`

:math:`f_{1 - \alpha/2} = f_{1 - 0.05} = f_{0.95}(10,9) = \frac{1}{f_{0.05}(9,10)} = \frac{1}{3.02} = 0.33`

Rejection Region: Reject :math:`H_0` if, F > 3.14 or F < 0.33

Our test statistic was F = 0.64. This value does not fall in the rejection region. 

We do not reject :math:`H_0` and conclude that there is not sufficient evidence, at the 0.10 level, that the population variances are different.

Independence Testing, Or Analysis of Categorical data
======================================================

Many experiments result in measurements that are qualitative or categorical rather than quantitative.​ 
- Cars classified by color​
- M&Ms classified by type (plain or peanut)​

These data sets have the characteristics of a multinomial experiment.  ​

Multinomial experiment
----------------------

1. The experiment consists of n identical trials.​\
2. Each trial results in one of k categories.​
3. The probability that the outcome falls into a particular category i on a single trial is :math:`p_i` and remains constant from trial to trial. The sum of all k probabilities, :math:`p_1+p_2 +…+ p_k = 1`. ​
4. The trials are independent
5. We are interested in the number of outcomes in each category, :math:`O_1, O_2, ..., O_k` with :math:`O_1, O_2, ..., O_k = n`

The Binomial experiment
-----------------------

- A special case of the multinomial experiment with k = 2.
- Categories 1 and 2: success and failure​
- p1 and p2:	p and q​
- O1 and O2: x and n-x​
- We made inferences about p ​(and q = 1 - p)​


Pearson's Chi-Square Statistic
-------------------------------

- We have some preconceived idea about the values of the pi and want to use sample information to see if we are correct.
- The expected number of times that outcome i will occur is :math:`E_i = np_i` . If the observed cell counts, :math:`O_i`, are too far from what we hypothesize under :math:`H_0`, the more likely it is that :math:`H_0` should be rejected. ​

We use the pearson chi-square statistic:

.. math::
    \chi^2 = \sum{\frac{(O_i-E_i)^2}{E_i}}

When :math:`H_0` is true, the differences O-E will be  small, but large when :math:`H_0` is false. 

Look for large values of :math:`\chi_0` based on the chi-square distribution with a particular number of degrees of freedom.​

Goodness of Fit test
---------------------

- A single categorical variable is measured, and exact numerical values are specified for each of the :math:`p_i`.​
- Expected cell counts are :math:`E_i = np_i`
- Degrees of freedom: :math:`df = k-1`

**Example**

Toss a die 300 times with the following results. Is the die fair or biased? ​

=========== ========== ========== ========== ========== ========== ==========  
Upper Face      1           2          3          4         5           6              
=========== ========== ========== ========== ========== ========== ========== 
# of times      50          39         45        62        61          43  
=========== ========== ========== ========== ========== ========== ==========

- A multinomial experiment with k = 6 and O1 to O6 given in the table. 
- We test at alpha = 0.05:

:math:`H_0: p_n = 1/6` (die is fair)
:math:`H_a:` at least one :math:`p_i` is different from 1/6 (die is biased)

The first step is to calculate the expected cell counts: :math:`E_i = np_i = 300(1/6) = 50`

======================= ========== ========== ========== ========== ========== ==========  
Upper Face                  1           2          3          4         5           6              
======================= ========== ========== ========== ========== ========== ========== 
# of times :math:`O_i`      50          39         45        62        61          43  
:math:`E_i:`                50          50         50        50        50          50
======================= ========== ========== ========== ========== ========== ==========

Test statistic and rejection Region:

..math::
    \chi^2 = \sum{\frac{(O_i-E_i)^2}{E_i}} = \frac{(50 - 50)^2}{50} + \frac{(39 - 50)^2}{50} + ... + \frac{(43 - 50)^2}{50} = 9.2

Reject :math:`H_0` if :math:`X^2` > :math:`\chi^2_0.05` = 11.07 with k-1 = 6-1 = 5 df

We do not reject :math:`H_0` . There is insufficient evidence to indicate that the die is biased.

Things to note
--------------

- The test statistic, :math:`X^2` has only an approximate chi-square distribution. 
- For the approximation to be accurate, statisticians recommend :math:`E_i \ge 5` for all cells
- Goodness of fit tests are different from previous tests since the experimenter uses :math:`H_0` for the model he thinks is true. ​
- Be careful not to accept :math:`H_0` (say the model is correct)

Test of Independence
=====================

Contigency Tables: A Two-Way classification
--------------------------------------------

​The experimenter measures two qualitative variables to generate bivariate data.
- Gender and colorblindness
- Age and opinion
- Professiorial rank and type of university

Summarize the data by counting the observed number of outcomes in each of the intersections of category levels in a contingency table.​

R x c Contigency Table
-----------------------

The contingency table has r rows and c columns - rc total cells.

========== ============== ============== ============== ==============
                1                2            ,,,,             c
========== ============== ============== ============== ==============
    1       :math:`O_11`   :math:`O_12`        ,,,,       :math:`O_1c`
    2       :math:`O_21`   :math:`O_22`        ,,,,       :math:`O_2c`
   ,,,,          ,,,,          ,,,, 
    r       :math:`O_r1`   :math:`O_r2`        ,,,,       :math:`O_rc`
========== ============== ============== ============== ==============

We study the relationship between the two variables. Is one method of classification contingent or dependent on the other? 

Does the distribution of measurements in the various categories for variable 1 depend on which category of variable 2 is being observed?​
If not, the variables are independent.

Chi Square test of Independence
--------------------------------

:math:`H_0:` classifications are independent

:math:`H_a:` classifications are dependent

Observed cell counts are :math:`O_ij:` for row i and column j.​

Expected cell counts are :math:`E_ij = np_ij`

:math:`p_{ij} = p_ip_j` = P(falling in row i)P(falling in row j)​

Chi-Square test of Independence
--------------------------------

Estimate :math:`p_i` and :math:`p_j` with :math:`\frac{r_i}{n}` and ​:math:`\frac{c_j}{n}`

.. math::
    \hat{E_{ij}} = n(\frac{r_i}{n})(\frac{c_j}{n}) = \frac{r_ic_j}{n}

Test statistic

.. math::
    X^2 = \sum{\frac{(O_{ij} - \hat{E_{ij}})^2}{\hat{E_{ij}}}}

The test statistic has an approcimate chi-square distribution with df = (r-1)(c-1)

**Example**

Furniture defects are classified according to type of defect and shift on which it was made.​

========= ======== ======== ======== =============
    x                     Shift
--------- ----------------------------------------
   Type     1         2         3        Total   
========= ======== ======== ======== =============
    A       15         26     33        74
    B       21         31     17        69
    C       45         34     49        128
    D       13         5      20        38
  Total     94         96     119       309
========= ======== ======== ======== =============

Does the data present sufficient evidence to indicate that the type of furniture defect varies with the shift during which the piece of furniture is produced? Test at the 1% level of significance.​

:math:`H_0:` type of defect is independent of shift​

:math:`H_a:` type of defect depends on the shift 

Then calculate the expected cell counts. For Example

chi-sqr = 19.178 for df = 6 and p-value = 0.004

.. math:: 

    \hat{E_{12}} = \frac{r_1c_2}{n} = \frac{74(96)}{309} = 22.99

Reject :math:`H_0:`. There is sufficient evidence to indicate that the proportion of defect types vary from shift to shift.​

Test for Homogeneity
---------------------

Sometimes researchers design an experiment so that the number of experimental units falling in one set of  categories is fixed in advance.

Example: An experimenter selects 900 patients who have been treated for flu prevention. She selects 300 from each of three types—no vaccine, one shot, and two shots. 

Each of the c columns (or r rows) whose totals have been fixed in advance is actually a single multinomial experiment.

The chi-square test of independence with (r-1)(c-1) df is equivalent to a test of the equality of c (or r)  multinomial populations.

**Honestly I couldn't finish these slides they were a mess, Maybe I'll come back to it later.**