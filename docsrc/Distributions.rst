================
Distributions
================

Below are some distributions mentioned throughout the class

Normal Distribution
===================

The density of the normal random variable X, with mean µ and variance σ2 Is

.. math::
    N(X; µ, σ) = f(x) = \frac{1}{\sqrt{2\pi\sigma^{2}}}e^{-\frac{(x - \mu)^{2}}{2\sigma^{2}}}

Sampling Distribution
=====================

The distribution of a statistic is called a sampling distribution.​ A statistic is a random variable that depends only on the observed sample.​
The sampling distribution of a statistic depends on the distribution of the population, the size of the sample, and the method of choosing samples.​

The sampling distribution of :math:`\bar{X}` with sample size n is the distribution that results when the experiment is conducted over and over 
(always with sample size n) and the many values of :math:`\bar{X}` result. This sampling distribution then describes the variability of the sample
averages around the population mean :math:`\mu`

The :math:`\bar{X}` :math:`\mu_{\bar{x}} = \mu` And has a variance of :math:`\sigma_{\bar{x}} = \frac{\sigma^2}{n}`

Thus, if the random sample of n observations is taken from a population with a normal distribution with mean :math:`\mu` and variance :math:`\sigma^2` the sample mean, 
:math:`\bar{X}`, will have a normal distribution with :math:`\bar{X} = N(\mu, \frac{\sigma^2}{n})`

Central Limit Theorem
=====================

If :math:`\bar{X}` is the mean of a random sample of size n taken from a population with mean :math:`\mu` and finite variance :math:`\sigma^2` , then the limiting form of the 
distribution of :math:`Z=\frac{\bar{X}-\mu}{\sigma}` , As :math:`N \to \infty` is the standard normal distribution, N(0,1). As long as N > 30, The clt applies.

Example:
Suppose the amount of TV a college student watches in a week follows a normal distribution with a mean of 8 hours and a standard deviation of 3 hours.​
Find the probability that, for a sample of 10 students, they have a mean time of less than 6 hours per week?
So N(8, 3) then the sampling distribution of :math:`\bar{X} = Normal(\mu_{\bar{x}} = 8, \sigma_{\bar{x}}^2 = 9/10 )`
Then :math:`P(\bar{X} < 6)` needs to be converted to Z so :math:`Z=\frac{6-8}{\frac{3}{\sqrt{10}}}` = -2.11
This value can be looked up in the Z table, Which is P(Z < -2.11) = 0.0174


T Distribution
===================

For CLT to work the population standard deviation σ must be known. When we do not know :math:`sigma` or it is unreasonable to assume :math:`sigma` then it must be estimated using sample information 
much in the same way :math:`\mu = \bar{X}` . In this situation we use the T distribution. The T Table should also be used when n < 30, and the Z table otherwise.

T(X; µ, s) = :math:`T = \frac{\bar{X} - \mu}{\frac{S}{\sqrt{N}}}` where s is the estimate of :math:`sigma` .

T can also be a function of the Chi square and the Z table?  

.. math:: 
    T = \\frac{Z}{\\sqrt{\\frac{V}{(n-1)}}}

Let Z be a standard normal random variable and V a chi-squared random variable with v degrees of freedom. If Z and V are independent, then the distribution of the random variable T, where

:math:`T = \frac{Z}{\sqrt{\frac{V}{(v)}}}` is known as the t-distribution with v degrees of freedom

The T-distribution is similar to standard normal. It is bell-shaped and symmetric about the mean of zero. However, the T-distribution is more variable and its variance depends on degrees of freedom (n-1).
Only when n goes to infinity are T and Z the same. :math:`\tau_{\alpha}` represents the t-value where the area to the right is :math:`\alpha` so :math:`P(T > \tau_{\alpha}) = \alpha` . 
Since T is symmetric about zero: :math:`\tau_{1 - \alpha} = -\tau_{\alpha}` :math:`P(T > -\tau_{\alpha}) = 1 - \alpha`. The T table is used for fingin t-values.

A t-value that falls below :math:`-\tau_{0.025}` or above :math:`\tau_{0.025}` would make us believe that a very rare event has occurred or that our assumption about population mean µ is incorrect.
The probability we fall in that region given that µ is correct is only 5%.


Example:
The t-value with v = 14 degrees of freedom that has an area to the right of 0.025 is: :math:`\tau_{0.025, 14} = 2.145`

Example: 
:math:`P(\tau_{0.025} < T < \tau_{0.05})`
:math:`= P(T < \tau_{0.05}) - P(T < -\tau_{0.025})`
=(1-0.05) - 0.025
= 0.95 - 0.025
= 0.925

Example: 
A chemical engineer claims that the population mean yield of a certain batch process is 500 grams per milliliter of raw material. To check this claim he samples 25 batches.
What conclusion should he draw from a sample that has mean :math:`\bar{X}` = 518 grams per milliliter and sample standard deviation of s = 40 grams?

.. math::
    \tau = \frac{\bar{X} - \mu}{\frac{s}{\sqrt{n}}} = \frac{518 - 500}{\frac{40}{5}}
    V = 24 degrees of freedom
    \tau_{2.064}

Since 2.25 > 2.064, we do fall above :math:`\tau_{0.025}` and the claim about :math:`\mu` is most likely incorrect.


F distribution
==============
The F statistic is defined to be the ratio of 2 independent chi-square random variables, each divided by its degrees of freedom.

.. math::
    F = \frac{\frac{\upailon}{\nu_{1}}}{\frac{\upailon}{\nu_{2}

Where U and V are independent chi-square random variables with :math:`\nu_{1}` and :math:`\nu_{2}` degrees of freedom, respectively. The order the degrees of freedom are listed is important. 
:math:`\nu_{1}` is the numerator degrees of freedom and :math:`\nu_{2}` is the denominator degrees of freedom.

:math:`f_{a}` denotes the f-value with a probability to the right of :math:`\alpha` so
:math:`P(F > f_{\alpha})` 
The F-distribution is not symmetric but we do have the property: :math:`f_{1-\alpha}(\nu_{1}, \nu_{2}) = \frac{1}{f_{\alpha}(\nu_{1}, \nu_{1})}`

Example:
We wish to test if two population variances are equal. We take a sample of 10 from the first population and come up with a sample variance of :math:`s_{1}^2` = 10.441.
We take a sample of 8 from the second population and come up with a sample variance of :math:`s_{2}^2` = 1.846.

:math:`f = \frac{\sigma_{2}^2 S_{1}^2}{\sigma_{1}^2 S_{2}^2} = \frac{10.411}{1.846} = 5.656`

So the f distribution value is :math:`f_{0.05}(9,7)` = 3.68
Since 5.565 > 3.68 our f-value has less than 5% chance of occurring if the population variances are actually equal.
