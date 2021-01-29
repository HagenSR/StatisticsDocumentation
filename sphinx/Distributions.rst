================
Distributions
================

Below are some distributions mentioned throughout the class

Normal Distribution
===================

The density of the normal random variable X, with mean µ and variance σ2 Is
N(X; µ, σ) = {latex}f(x) = \frac{1}{\sqrt{2\pi\sigma^{2}}}e^{-\frac{(x - \mu)^{2}}{2\sigma^{2}}}{/latex} 

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


