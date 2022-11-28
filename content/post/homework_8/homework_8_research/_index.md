---
title: "Homework 8, research"
date: 2022-11-24T13:14:58+01:00
draft: false
author: "Andrea Di Paolo"
math: "true"
---
Assignment:
<ul>
    <li>Search on the web about possible derivation of the Normal Distribution,</li>
    <li>Search on the web about method to generate normal variate (eg Marsaglia method, etc.).</li>
</ul>
<!--more-->

# <mark> Standard Normal Distribution </mark>
{{< math.inline >}}
We first define the standard normal random variable. We will then see that we can obtain other normal random variables by scaling and shifting a standard normal random variable. <br>
A continuous random variable \(Z\) is said to be a standard normal (standard Gaussian) random variable, shown as \(Z∼N(0,1)\), if its PDF is given by
$$
f_Z(z) = \frac{1}{\sqrt{2\pi}}e^{-(\frac{z^2}{2})}, \ for\ all\ z\in\mathbb{R}
$$
{{</ math.inline >}}

# <mark> Normal Distribution </mark> <br>
{{< math.inline >}}

If \(Z\) is a standard normal random variable and \(X=\sigma Z+\mu\), then \(X\) is a normal random variable with mean \(\mu\) and variance \(\sigma^2\) i.e,
$$
X ∼ N(\mu,\sigma^2)
$$
Conversely, if \(X∼N(\mu,\sigma^2)\), the random variable defined by \(Z=X−\mu\sigma\) is a standard normal random variable, i.e., \(Z∼N(0,1)\).
{{</ math.inline >}}

# <mark> Chi-Square Distribution </mark>
{{< math.inline >}}

The chi-square distribution results when ν independent variables with standard normal distributions are squared and summed. The degrees of freedom of the distribution is equal to the number of standard normal deviates being summed. The formula for the probability density function of the chi-square distribution is

$$
f(x) = \frac{e^{-\frac{x}{2}}x^{\frac{v}{2}-1}}{2^{\frac{v}{2}}\Gamma(\frac{v}{2})},\ for\ x \geq 0
$$
where \(ν\) is the shape parameter and \(\Gamma\) is the gamma function. The formula for the gamma function is
$$
\Gamma(a) = \int_0^{\infty}t^{a-1}e^{-t}dt
$$
{{</ math.inline >}}

# <mark> T Student </mark>
The T distribution (also called Student’s T Distribution) is a family of distributions that look almost identical to the normal distribution curve, only a bit shorter and fatter. The t distribution is used instead of the normal distribution when you have small samples. The larger the sample size, the more the t distribution looks like the normal distribution:
$$
T=\frac{\bar{X} - \mu}{\frac{S}{\sqrt{n}}}
$$

# <mark> F distribution </mark>
{{< math.inline >}}

The F-distribution with \(d1\) and \(d2\) degrees of freedom is the distribution of
$$
X=\frac{S_1/d_1}{S_2/d_2}
$$
where \(S_{1}\) and \(S_{2}\) are independent random variables with chi-square distributions with respective degrees of freedom \(d_{1}\) and \(d_{2}\).
{{</ math.inline >}}

# <mark> Marsaglia polar method </mark>
{{< math.inline >}}

In computer science – in particular, in applications of the Monte Carlo method – the Marsaglia polar method is a method for generating a pair of independent standard normal random variables by choosing random points \((x, y)\) in the square \(−1 < x < 1, −1 < y < 1\)  until
$$
s =x^2 + y^2 < 1,
$$
and then returning the required pair of normal random variables as
$$
x\sqrt{\frac{-2ln(s)}{s}},y\sqrt{\frac{-2ln(s)}{s}}

$$

{{</ math.inline >}}

# References
[1] probabilitycourse.com, "Normal (Gaussian) Distribution", [URL](https://www.probabilitycourse.com/chapter4/4_2_3_normal.php), <br>
[2] itl.nist.gov, "Chi-Square Distribution", [URL](https://www.itl.nist.gov/div898/handbook/eda/section3/eda3666.htm), <br>
[3] onlinestatbook.com, "Chi Square Distribution", [URL](https://onlinestatbook.com/2/chi_square/distribution.html#:~:text=Chi%20Square%20Distribution&text=A%20standard%20normal%20deviate%20is,standard%20normal%20deviates%20being%20summed. ), <br>
[4] statisticshowto.com, "What is the T Distribution?", [URL](https://www.statisticshowto.com/probability-and-statistics/t-distribution/), <br>
[5] en.wikipedia.org, "F-distribution", [URL](https://en.wikipedia.org/wiki/F-distribution)