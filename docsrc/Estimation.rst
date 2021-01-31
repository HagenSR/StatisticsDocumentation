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
Example:
A consumer wants to estimate the average price of similar homes in their city before putting their home on the market.
Estimation: Estimate 𝜇, the average home price

Hypothesis Testing:
-------------------

Deciding about the value of a parameter based on some preconceived idea.
“Did the sample come from a population with 𝜇 = 5?”
Example:
A manufacturer wants to know if a new type of steel is more resistant to high temperatures than an old type was.
Hypothesis test: Is the new average resistance, 𝜇_𝑁 equal to the old average resistance, 𝜇_𝑂?

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

Even the most efficient unbiased estimator is unlikely to estimate the pppulation parameter exactly.
There are many situations in which it is preferable to determine an interval where we would expect to find the parameter.

For a generalized population parameter θ an interval estimate is of the form:

.. math::
    \theta_{L} < \theta < \theta_{U}

:math:`\theta_{L}` represents the lower bound 
:math:`\theta_{U}` represents the upper bound

These bounds will depend on the point estimate, 𝜃, and the sampling distribution. The interval estimate is found such that: :math:`P(𝜃_{L}<𝜃<𝜃_{𝑈}) = 1 - 𝛼`
1 - 𝛼 is called the confidence coefficient or degree of confidence. 𝛼 is called the level of significance :math:`\theta_{L} , \theta_{U}` are called the confidence limits

Example:
If 𝛼 = 0.05 we would have a (1 – 0.05) = 95% confidence interval.
If 𝛼 = 0.01 we would have a 99% confidence interval.
The wider the interval is, the more confident we can be that the interval contains the unknown parameter.

This confidence interval can be found by:
:math:`P(\bar{X} - Z_{\alpha/2}\frac{\sigma}{\sqrt{n}} < \mu <  \bar{X} + Z_{\alpha/2}\frac{\sigma}{\sqrt{n}}) = 1 – α` when sigma is known and N > 30

Example:
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

Example:
How large a sample is required if we want to be 95% confident that our estimate of 𝜇 in Example 1 is off by less than 0.05?
:math:`n = (\frac{Z_{\alpha/2}*\sigma}{e})^2 = (\frac{1.96 * 0.3}{0.05})^2` = 138.3 = 139

One sided confidence bounds
---------------------------

Confidence intervals are by their nature two-sided since they produce upper and lower bounds for the parameter. One-sided bounds can be constructed simply by using a value of z that puts a rather than a/2 in the tail of the z distribution. 

.. math::
    P(\mu > \bar{X} - Z_{\alpha}\frac{\sigma}{\sqrt{n}} = 1 -\alpha)

    P(\mu < \bar{X} + Z_{\alpha}\frac{\sigma}{\sqrt{n}} = 1 -\alpha)

Example:

In a psychological testing experiment, 25 subjects are selected randomly and their reaction time, in seconds to a particular stimulus is measured. Assume population variance is 4 seconds2 and that the distribution is approximately normal. 
In our sample the average reaction time was 6.2 seconds. Give a 95% upper bound for the mean reaction time.

:math:`\bar{X} + z_{\alpha}\frac{\sigma}{\sqrt{n}}`

:math:`6.2 + 1.645\frac{2}{\sqrt{25}}` 

6.2 + 0.658 = 6.858

We are 95% confident that the mean reaction time is less than 6.858 seconds


