---
title: "Homework 6, research"
date: 2022-11-07T17:00:14+01:00
draft: false
author: "Andrea Di Paolo"
math: "true"
---
Assignment:
<ul>
    <li>Try to explain in your own words, the concept of population and sampling distribution, </li>
    <li>show the expected value and variance of the sampling mean and take a look at the same sampling variance.</li>
</ul>
<!--more-->

# <mark> Population distribution </mark>
{{< math.inline >}}
The population is the whole set of values, or individuals, you are interested in. For example, if you want to know the average height of the residents of India, that is your population, ie, the population of India.
Population characteristic are mean (\(\mu\)), Standard deviation (\(\sigma\)) , proportion (P) , median,  percentiles etc. The value of a population characteristic is fixed. This characteristics are called population distribution. They are symbolized by Greek characters as they are population parameters.
{{</ math.inline >}}

# <mark> Sampling distribution </mark>
{{< math.inline >}}

The sample is a subset of the population, and is the set of values you actually use in your estimation. Let’s think 1000 individual you have selected for your study to know about average height of the residents of India. This sample has some quantity computed from values e.g.  mean (x ), Standard deviation (s) , sample proportion etc. This is called sample distribution. The mean and standard deviation are symbolized by Roman characters as they are sample statistics.<br> 

Formally, given a population, we can represent it as a random variable \(X\). A random sample of a population of size n can be represented as a set of n random variables:
$$
    X_1, X_2, ..., X_n
$$
where they are all identically distributed with each other since they have the same distribution of X.
 
{{</ math.inline >}}
# <mark> Expected value and variance of the sampling mean </mark>
{{< math.inline >}}

The sample mean is basically the mean of the random sample that we define previously:
$$
    \bar{X} = \frac{X_1 + X_2 + ... + X_n}{n}
$$

The expected value (also called expectation, expectancy, mathematical expectation, mean, average, or first moment) is a generalization of the weighted average. Informally, the expected value is the arithmetic mean of a large number of independently selected outcomes of a random variable.
Now we want to compute the expected value of the sampling mean:
$$
    E(\bar{X}) = E\left (\frac{X_1 + X_2 + ... + X_n}{n}\right)
$$
Then, for the linearity property of the expected value \(E(aX) = aE(X)\):
$$
    E(\bar{X}) = \frac{1}{n}E({X_1 + X_2 + ... + X_n})
$$
Always for the linearity property we have that \(E(X + Y) = E(X) + E(Y)\):
$$
    E(\bar{X}) = \frac{1}{n}[E(X_1) + E(X_2) + ... + E(X_n)]
$$
Since \(X_1, X_2, ..., X_n\) are independent and identically distributed we have thate they have all the same expected value \(\mu\):
$$
    E(\bar{X}) = \frac{1}{n}[n\mu] = \mu
$$
We have shown that the mean (or expected value, if you prefer) of the sample mean \(\bar{X}\)is . That is, we have shown that the mean of \(\bar{X}\) is the same as the mean of the individual \(X_i\).

The variance is the expectation of the squared deviation of a random variable from its population mean or sample mean. Variance is a measure of dispersion, meaning it is a measure of how far a set of numbers is spread out from their average value.
Now we want to compute the variance of the sampling mean:
$$
    Var(\bar{X}) = Var\left(\frac{X_1 + X_2 + ... + X_n}{n}\right)
$$
we have that \(Var(X + Y) = Var(X) + Var(Y) + 2Cov(X,Y)\), but when \(X\) and \(Y\) are independent \(Cov(X,Y) = 0\). Using that property and that \(Var(aX) = a^2Var(X)\) we obtain:
$$
    Var(\bar{X}) = \frac{1}{n^2}Var(X_1) + \frac{1}{n^2}Var(X_2) + ... + \frac{1}{n^2}Var(X_n)  
$$
The \(X_i\) are identically distributed, which means they have the same variance \(\sigma^2\), then:
$$
    Var(\bar{X}) = \frac{1}{n^2}[n\sigma^2] = \frac{\sigma^2}{n}
$$

{{</ math.inline >}}
# <mark> Expected value and variance of the sampling variance </mark>
The sample variance is defined as: 
$$
    S^2 = \frac{1}{n}\sum_{i=1}^{n}(X_i - \bar{X})^2
$$
The expected value of the sampling variance is:
$$
    E(S^2) = E\left(\frac{1}{n}\sum_{i=1}^{n}(X_i - \bar{X})^2\right) = \frac{n-1}{n}\sigma^2
$$
The variance of the sampling variance, instead, is:
$$
    Var(S^2) = \frac{\mu_4}{n} - \frac{\sigma^4(n-3)}{n(n-1)}
$$
where \(\mu_4\) is the fourth central moment of \(X\), defined as:
$$
    \mu_4 = E[(X-\mu)^4]
$$
# References
[1] makemeanalyst.com, "population distribution, sample distribution and sampling distribution", [URL](https://makemeanalyst.com/observational-studies-and-experiments/population-distribution-sample-distribution-and-sampling-distribution/), <br>
[2] en.wikipedia.org, "Sampling distribution", [URL](https://en.wikipedia.org/wiki/Sampling_distribution), <br>
[3] online.stat.psu.edu, "Mean and Variance of Sample Mean", [URL](https://online.stat.psu.edu/stat414/lesson/24/24.4), <br>
[4] en.wikipedia.org, "Variance", [URL](https://en.wikipedia.org/wiki/Variance).