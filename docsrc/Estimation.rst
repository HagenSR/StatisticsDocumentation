================
Estimating
================

Below are some formulas listed in the cheat sheets from probabilty and stats along with a brief description

Estimating the Mean
===================

Populations are described by their probability distributions and parameters. For quantitative populations, the mean and shape are described by 𝜇 and 𝜎.
For binomial populations, the mean and shape are determined by p. If the values of parameters are unknown, we make inferences about them using sample information.

Two Types of inferences
=======================

Estimation:
-----------

Estimating or predicting the value of the parameter
“What are the most likely values of 𝜇 or p?”

**Example**:

A consumer wants to estimate the average price of similar homes in their city before putting their home on the market.
Estimation: Estimate 𝜇, the average home price

Hypothesis Testing:
-------------------

Deciding about the value of a parameter based on some preconceived idea.
“Did the sample come from a population with 𝜇 = 5?”

**Example**:

A manufacturer wants to know if a new type of steel is more resistant to high temperatures than an old type was.
Hypothesis test: Is the new average resistance, :math:`𝜇_{𝑁}` equal to the old average resistance, :math:`𝜇_{O}`?

An estimator is a rule, usually a formula, that tells you how to calculate the estimate based on the sample.



Interval estimate: two numbers are calculated to create an interval within which the parameter is expected to lie.

Point Estimators
================

Point estimate: a single number is calculated to estimate the parameter.

Ex. :math:`\bar{X}` is a point estimate for 𝜇

Since an estimator is calculated from sample values, it varies from sample to sample according to its sampling distribution.
An estimator is unbiased if the mean of its sampling distribution equals the parameter of interest.

Ex. :math:`E(\bar{X})` = 𝜇

Of all the unbiased estimators, we prefer the estimator whose sampling distribution has the smallest spread or variability.
The unbiased estimator with the smallest variance is called the most efficient estimator of the parameter of interest.

Interval Estimation
===================

Even the most efficient unbiased estimator is unlikely to estimate the population parameter exactly.
There are many situations in which it is preferable to determine an interval where we would expect to find the parameter.

For a generalized population parameter θ an interval estimate is of the form:

.. math::
    \theta_{L} < \theta < \theta_{U}

:math:`\theta_{L}` represents the lower bound 
:math:`\theta_{U}` represents the upper bound

These bounds will depend on the point estimate, 𝜃, and the sampling distribution. The interval estimate is found such that: :math:`P(𝜃_{L}<𝜃<𝜃_{𝑈}) = 1 - 𝛼` .
1 - 𝛼 is called the confidence coefficient or degree of confidence. 𝛼 is called the level of significance :math:`\theta_{L} , \theta_{U}` are called the confidence limits

**Example**:

If 𝛼 = 0.05 we would have a (1 – 0.05) = 95% confidence interval. If 𝛼 = 0.01 we would have a 99% confidence interval.
The wider the interval is, the more confident we can be that the interval contains the unknown parameter.

This confidence interval can be found by:

:math:`P(\bar{X} - Z_{\alpha/2}\frac{\sigma}{\sqrt{n}} < \mu <  \bar{X} + Z_{\alpha/2}\frac{\sigma}{\sqrt{n}}) = 1 – α` 

when sigma is known and N > 30

**Example**:

The average zinc concentration recovered from a sample of zinc measurements in 36 different locations is found to be 2.6 grams per milliliter. Find the 99% confidence interval for 
the zinc concentration in the river. Assume that the population standard deviation is 0.3 gram per milliliter. 

.. math::
    \bar{X} \pm Z_{\alpha/2}\frac{\sigma}{\sqrt{n}}
    2.6 \pm 2.575(\frac{0.3}{\sqrt{36}})
    (2.47, 2.73)

or 2.47 < 𝜇 < 2.73. So In the repeated sampling, we should expect 99% of the time that the average zinc concentration  is between 2.47 and 2.73 gr./mill. 

Confidence Level 
----------------

The more confident we want to be, the larger the margin of error must be. Every confidence interval is a balance between certainty and precision
When choosing confidence level we want to be, in most cases, both sufficiently certain and sufficiently precise to make useful statements

Error
-----

Confidence intervals provide an estimate of the accuracy of our point estimate. Most of the time :math:`\bar{X}` will not exactly equal 𝜇 and the difference between our point estimate and the actual parameter value will be the error.
If :math:`\bar{X}` is used as an estimate of 𝜇, we can be 100(1 -𝛼)% confident that the error will not exceed :math:`Z_{\alpha/2}\frac{\sigma}{\sqrt{n}}`.

Often we are concerned with how large a sample is necessary to ensure that the error in estimating 𝜇 will be less than a specified amount, e.
If 𝑋 ̅ is used as an estimate of 𝜇, we can be 100(1 -𝛼)% confident that the error will not exceed e when the sample size is:
:math:`n = (\frac{Z_{\alpha/2}*\sigma}{e})^2` . N must be a whole number, so round up.

**Example**:

How large a sample is required if we want to be 95% confident that our estimate of 𝜇 in example 1 is off by less than 0.05?

:math:`n = (\frac{Z_{\alpha/2}*\sigma}{e})^2 = (\frac{1.96 * 0.3}{0.05})^2` 

= 138.3 = 139

One sided confidence bounds
---------------------------

Confidence intervals are by their nature two-sided since they produce upper and lower bounds for the parameter. One-sided bounds can be constructed simply by using a value of z that puts a rather than a/2 in the tail of the z distribution. 

.. math::
    P(\mu > \bar{X} - Z_{\alpha}\frac{\sigma}{\sqrt{n}} = 1 -\alpha)

    P(\mu < \bar{X} + Z_{\alpha}\frac{\sigma}{\sqrt{n}} = 1 -\alpha)

**Example**:

In a psychological testing experiment, 25 subjects are selected randomly and their reaction time, in seconds to a particular stimulus is measured. Assume population variance is 4 seconds2 and that the distribution is approximately normal. 
In our sample the average reaction time was 6.2 seconds. Give a 95% upper bound for the mean reaction time.

    :math:`\bar{X} + z_{\alpha}\frac{\sigma}{\sqrt{n}}`

    :math:`6.2 + 1.645\frac{2}{\sqrt{25}}` 

    6.2 + 0.658 = 6.858

We are 95% confident that the mean reaction time is less than 6.858 seconds


Paired Comparison
-----------------

Comparing observations from two groups. This Requires
-Conditions of the two populations are not assigned randomly to experimental units​
-Each homogeneous experimental unit receives both population conditions​
-Our observations of interest are the differences between the homogeneous units

The ith difference is: :math:`D_{i} = X_{1i} - X_{2i}`

If we are sampling from normal populations, these differences will be normally distributed with a mean of :math:`\mu_{D} = \mu_{1} - \mu_{2}`

If :math:`\bar{d} and s_{d}` are the mean and standard deviation of the normally distributed differences of n random pairs of the normally
distributed of n random pairs of measurements, a 100(1-:math:`\alpha` )% confidence interval for :math:`\mu_{D} = \mu{1} - \mu_{2}` is

.. math::
    \bar{d} \pm t_{\alpha/2}\frac{S_{d}}{\sqrt{n}}
    
Where V = n-1 degrees of freedom

Paired observations
-------------------

Once you have designed the experiment by pairing, you MUST analyze it as a paired experiment. If the experiment is not designed as a paired 
experiment in advance, do not use this procedure.

**Example**:

Two types of tires, A and B, are randomly assigned to each of the rear wheels of five cars. Compare the average wear for types A and B using a 95% confidence interval.

===== ======= =======
cars  Type A  Type B
===== ======= =======
 1      10.6    10.2
 2      9.8     9.4
 3      12.3    11.8
 4      9.7     9.1
 5      8.8     8.3
===== ======= =======

This experiment includes paired observations because the measurements are taken on the same car.​
We must calculate the differences:

===== ======= ======= ========
cars  Type A  Type B   Diff
===== ======= ======= ========
 1      10.6    10.2    0.4
 2      9.8     9.4     0.4
 3      12.3    11.8    0.5
 4      9.7     9.1     0.6
 5      8.8     8.3     0.5
===== ======= ======= ========

    :math:`\bar{d}` = mean of the differences so (0.4 + 0.4 +0.5 + 0.6 + 0.5)/5

    :math:`S_{d}` = standard deviation of the differences

    = :math:`\sqrt{\frac{1}{n-1}*\sum_{i=1}^{n}(D_{i}-\bar{d})^2}`

    = :math:`\sqrt{\frac{1}{4}*((0.4 - 0.48)^2 + (0.4 - 0.48)^2) + (0.5 - 0.48)^2 + (0.6 - 0.48)^2 + (0.5 - 0.48)^2}`

    = 0.08367


**Example**:

    n = 5

    95% confidence Interval gives :math:`\alpha` = 0.05

    :math:`t_{\alpha/2} = t_{0.025}` = 2.776 (V = 4)

    :math:`\bar{d} \pm t_{\alpha/2} * \frac{S_{d}}{\sqrt{n}}`

    :math:`0.48 \pm 2.776 * \frac{0.08367}{\sqrt{5}}`

    :math:`0.48 \pm 0.1039`

    (0.3761, 0.5839)

    0.3761 < :math:`\mu_{D}` < 0.5839

We are 95% confident that Type A tires have a higher average wear (?)
or the mean difference between type A tires and Type B tires is between 0.3761 < :math:`\mu_{D}` < 0.5839

Estimating Proportions
======================

A random sample of size n is selected from a binomial distribution. We are interested in the number of "Successes"
The population has parameter p which equals probability equals probability of success. We estimate p by taking the
number of Successes, x, divided by the total number in the sample, n.

:math:`\hat{p} = \frac{x}{n}`

:math:`\hat{p}` is an unbiassed estimator for p:

so if we are sampling from a binomial population, E(X) = np then the mean is

    :math:`E(\hat{p}) = p`

The variance of :math:`\hat{p}` is 

    :math:`\frac{pq}{n}`

Then if n is large and p is not too close to zero or one, the sampling distribution of :math:`\hat{p}` will be 
approximately normal and we have the property that

.. math::
    Z = \frac{\hat{p} - p}{\sqrt{\frac{pq}{n}}}

which has a standard normal distribution.

Confidence interval for a Proportions
-------------------------------------

The confidence interval for the probability of success, p is 

.. math::
    P(\hat{p}-Z_{\alpha/2}\sqrt{(\hat{p}\hat{q})/{n}} < p < \hat{p}+Z_{\alpha/2}\sqrt{(\hat{p}\hat{q})/{n}}) = 1 - \alpha

If :math:`\hat{p}` is the proportion of successes in a random sample of size n and :math:`\hat{q}` = 1- :math:`\hat{p}` ,
an approximate 100(1-\alpha)% confidence interval for the binomial paramter p is:

.. math::
    \hat{p} \pm z_{\alpha/2}\sqrt{\frac{\hat{p}\hat{q}}{n}}

**Example**:
In a random sample of n = 500 families owning TV’s in the city of Hamilton, Canada, it is found that x = 340 subscribe to HBO. 
Find a 95% confidence interval for the actual proportion of families with TVs in this city that subscribe to HBO.

.. math::
    n = 500, x = 340

    \hat{p} = \frac{x}{n} = \frac{340}{500} = 0.68

    \hat{q} = 1 - \hat{p} = 0.32

    \hat{p} \pm z_{\alpha/2}\sqrt{\frac{\hat{p}\hat{q}}{n}}

    0.68  \pm 1.96\sqrt{\frac{0.68(0.32)}{500}}

    0.68 \pm 0.041

    0.639 < p < 0.721


We are 95% confident that the real proportion of families that subscribe to HBO is between 0.639 < p < 0.721

Difference between two binomial Proportions
-------------------------------------------

Consider a situations where we wish to estimate the difference between two proportions, p1 and p2.​

**Example**: p1 is the proportion of smokers who have lung cancer and p2 is the proportion of non-smokers with lung cancer, 
and we wish to estimate the difference between these two.

Using the samping distribution of a single proportion, we can determine the sampling distribution of the difference of 
propotions.

    :math:`E(\hat{p_{1}} - \hat{p_{2}}) = p_{1} - p_{2}`

    :math:`Var(\hat{p}_{1} - \hat{p}_{2}) = \frac{p_{1}q_{1}}{n_{1}} + \frac{p_{2}q_{2}}{n_{2}}`

Since :math:`\hat{p}_1` and :math:`\hat{p}_2` both have approximately normal distributions, their difference will 
also be approximately normal. We can find a confidence interval for the difference of the proportions using the 
standard normal distribution

.. math::
    Z = \frac{(\hat{p_{1}} - \hat{p_{2}}) - (p_{1} - p_{2})}{\sqrt{\frac{p_{1}q_{1}}{n_{1}}+\frac{p_{2}q_{2}}{n_{2}}}}

Confidence Interval for the difference between propotions
---------------------------------------------------------

If :math:`\hat{p}_1` and :math:`\hat{p}_2` are proportions of successes in random samples of sizes :math:`n_1` and :math:`n_2` 
an approximate :math:`100(1-\alpha)%` confidence interval for the difference of two binomial parameters ( :math:`\hat{p}_1` - :math:`\hat{p}_2` ) is

.. math::
    (\hat{p}_1 - \hat{p}_2) \pm Z_{\alpha/2} \sqrt{\frac{p_{1}q_{1}}{n_{1}}+\frac{p_{2}q_{2}}{n_{2}}}

**Example**:

We are interested in the proportion of males and females in the population who have a minor blood disorder. In a random sample of 1000 males, 250 are found to be afflicted. ​

In a sample of 1000 females, 275 are afflicted.​

Compute a 95% confidence interval for the difference between the proportions of males and females who have this blood disorder.

.. math::
    n_{1} = 1000, x_{1} = 250, \hat{p}_{1} = 0.25

    n_{2} = 1000, x_{2} = 275, \hat{p}_{2} = 0.275

    (\hat{p}_1 - \hat{p}_2) \pm Z_{\alpha/2} \sqrt{\frac{p_{1}q_{1}}{n_{1}}+\frac{p_{2}q_{2}}{n_{2}}}

    (.25 - .275) \pm 1.96 \sqrt{\frac{.25(.75)}{1000}+\frac{.275(.725)}{1000}}

    -0.025 \pm 0.0386

    -0.0636 < (p_{1} - p_{2}) < 0.0136

Because the interval crosses 0, there appears to be no significant difference in the proportion of males who have the disorder and the proportion of
females who have the disorder.

Estimating variance, One and two sample
---------------------------------------

Sometimes the primary parameter of interest is not the population mean :math:`\mu` but rather the population variance :math:`\sigma^2` . We choose a 
random sample of size n from a normal distribution. We use the following to describe the sampling distribution of :math:`s^2`

.. math::
    \chi^2 = \frac{(n - 1)S^2}{\sigma^2}

which has a chi-squared distribution with n-1 degrees of freedom. So the confidence interval for variance would be

.. math::
    P(\frac{(n - 1)S^2}{\chi^2_{\alpha/2}} < \sigma^2 < \frac{(n - 1)S^2}{\chi^2_{1 - \alpha/2}})

Where v = n-1

**Example**
The weights of 10 packages of grass seed were measured and found to have a sample variance of 0.286 decagrams2.​Find a 95% confidence 
interval for the variance of the weights of all such packages, assuming they are coming from a normal distribution.

95% confidence gives :math:`\alpha` = 0.05, n = 10, v = 9 degrees of freedom. So

.. math::
    \chi^2_{\alpha/2} = \chi^2_{0.025} = 19.023

    \chi^2_{1 - \alpha/2} = \chi^2_{0.975} = 2.7

    \frac{(n - 1)S^2}{\chi^2_{\alpha/2}} < \sigma^2 < \frac{(n - 1)S^2}{\chi^2_{1 - \alpha/2}}

    P(\frac{(9)(0.286)}{19.023} < \sigma^2 < \frac{(9)(0.286)}{2.7})

    0.135 < \sigma^2 < 0.953 

Estimating the Ratio of Two Variances
-------------------------------------

A point estimate of the ratio of two population variances :math:`\frac{\sigma^2_{1}}{\sigma^2_{2}}` is given by the ratio 
:math:`\frac{S^2_{1}}{S^2_{2}}` of the sample variances. We can establish an interval estimate for the ratio of the population
variances by using the statistic:

.. math::
    F = \frac{\sigma^2_{2}S^2_{1}}{\sigma^2_{1}S^2_{2}}

The F statistic, when calculated, will have :math:`v_{1} = n_{1} - 1` degrees of freedom in the numerator and :math:`v_{2} = n_{2} - 1` 
degrees of freedom in the denominator. By using the F distribution we can create an interval estimate of the ration of the two population 
variances.

.. math::
    P(\frac{S^2_{1}}{S^2_{2}}\frac{1}{f_{\alpha/2}(v_{1}, v_{2})} < \frac{\sigma^2_{1}}{\sigma^2_{2}} <  \frac{S^2_{1}}{S^2_{2}}f_{\alpha/2}(v_{1}, v_{2})) = 1 - \alpha 

**Example**:

We wish to compare the variance of levels of the chemical orthophosphorus at two different stations along a river. Sixteen samples were collected at the first 
station and found to have a standard deviation of 3.07. Eleven samples were collected at the second station and found to have a standard deviation of 0.80.​
Find a 90% confidence interval for the ratio of the variances at the two stations.

.. math::
    n_{1} = 16, s_{1} = 3.07

    n_{2} = 11, s_{2} = 0.80

    90% confidence gives \alpha = 0.10
    f_{\alpha/2}(v_{1}, v_{2}) = f_{0.05}(15,10) = 2.85
    
    f_{\alpha/2}(v_{2}, v_{1}) = f_{0.05}(10,15) = 2.54

     P(\frac{S^2_{1}}{S^2_{2}}\frac{1}{f_{\alpha/2}(v_{1}, v_{2})} < \frac{\sigma^2_{1}}{\sigma^2_{2}} <  \frac{S^2_{1}}{S^2_{2}}f_{\alpha/2}(v_{1}, v_{2}))

     P(\frac{3.07^2}{0.8^2}\frac{1}{2.85} < \frac{\sigma^2_{1}}{\sigma^2_{2}} <  \frac{3.07^2}{0.8^2}(2.54)) 

     5.167 < \frac{\sigma^2_{1}}{\sigma^2_{2}} < 37.405

we are 90% confident that the real standard deviation is between 5.167 and 37.405