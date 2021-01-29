================
Formulas
================

Below are some formulas listed in the cheat sheets from probabilty and stats along with a brief description

Sample Statistics
=================

pretty much everything we take is a sample. Finding probabilities for samples requires normalizing the sample

Transforming X to Z
-------------------

If you have a population, A normal random variable X can be transformed into Z by 

:math:`Z=\frac{\bar{X}-\mu}{\sigma^2}`

The standard normal distribution has a mean of 0 and variance of 1. These values can then be looked up in the standard normal table.
Note that if you don't have N, It is probably a normal population variable that can be standardized by :math:`Z=\frac{\bar{X}-\mu}{\sigma}`

Sample Mean
-----------
The most common statistics used to measure the center of a sample is the mean. Let :math:`X_{1}, X_{2}...X_{n}` represent n random variables from a sample.
The Sample Mean is defined by :math:`\bar{Z}=\frac{1}{\eta}\sum_{i=1}^n{X_{i}}`
Example: Suppose we take a sample of 7 students and record the number of classes they took last year. The sample is: 2, 4, 9, 8, 6, 5, 3. Then the sample mean
would be :math:`\bar{x}=\frac{1}{7}` (2+3+9+8+6+5+3) = 5.29

Median
-------------------

The median is the middle measurement when the measurements are ranked from smallest to largest. If n is odd the median will be in the :math:`\frac{n + 1}{2}` position
when the measurements are ranked. If n is even the median will be the average of the :math:`\frac{n}{2}` and :math:`\frac{n}{2}+1` measurements

:math:`Z=\frac{\bar{X}-\mu}{\sigma^2}`

Mode
-------------------

The mode is the value of the sample that occurs most often.​ In our example, where the sample consists of the values 2, 3, 4, 5, 6, 8, 9, there is no mode. Each value is unique.
Sample data: 2, 4, 9, 8, 8, 5, 3​
The mode is 8, which occurs twice.​

​Sample data: 2, 2, 9, 8, 8, 5, 3​
There are two modes – 8 and 2.

Measures of Variability
-----------------------

A measure of central tendency in a sample does not by itself give a clear indication of the nature of the sample. Thus, a measure of variability in the sample must also be considered.​
We measure variability with variance, standard deviation, and range.

Sample Variance
-------------------

:math:`\sigma^2` shows how far the spread of the data is from the mean

:math:`S^2=\frac{1}{n-1}\sum_{i=1}^n({X_{i}-\bar{X}})^2`

Example:
Sample Data: 2, 4, 9, 8, 6, 5, 3
:math:`\bar{x}` = 5.29.
So the sample variance is 
:math:`S^2=\frac{1}{7-1} * (2-5.29)^2 +(4-5.29)^2 + (9-5.29)^2 +(8-5.29)^2 +(6-5.29)^2 + (5-5.29)^2 +(3-5.29)^2 = 6.57`

Standard deviation
-------------------

The standard deviation is simply :math:`\sqrt{S^2}`

Range
-------------------

The Range is simply :math:`X_{max} - X_{min}`



Distributions
=================

Normal Distribution
-------------------


