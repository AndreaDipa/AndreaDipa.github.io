---
title: "Homework_7_research"
date: 2022-11-15T09:01:52+01:00
draft: false
author: "Andrea Di Paolo"
math: "true"
---
Assignment:
<ul>
    <li>Try to understand the general idea of the Lebesgue-Stieltjes integral and why it is useful concept and notation in Theory of Probability,</li>
    <li>Explain in your own words the "Law of large numbers" and sketch a simple proof (Markov inequality, Čebyšëv inequality, ... ).</li>
</ul>
<!--more-->

# <mark> Lebesgue–Stieltjes integral </mark>
The Lebesgue–Stieltjes integral:
$$
\int_{a}^{b} f(x)dg(x)
$$
{{< math.inline >}}
is defined when \(f: [a,b] \to \mathbb{R}\) is Borel-measurable (a Borel measure on a topological space is a measure that is defined on all open sets) and bounded and  \(g: [a,b] \to \mathbb{R}\)  is of bounded variation in \([a,b]\) and right-continuous, or when \(f\) is non-negative and \(g\) is monotone and right-continuous. <br>
Where  f  is a continuous real-valued function of a real variable and v is a non-decreasing real function, the Lebesgue–Stieltjes integral is equivalent to the Riemann–Stieltjes integral, in which case we often write:
$$
\int_{a}^{b} f(x)dv(x)
$$
for the Lebesgue–Stieltjes integral, letting the measure \(μ_v\) remain implicit. This is particularly common in probability theory when v is the cumulative distribution function of a real-valued random variable X, in which case:
$$
\int_{-\infty}^{\infty} f(x)dv(x) = E[f(X)]
$$
if the moment E(Xn) exists, then it is equal to:
$$
\int_{-\infty}^{\infty} x^ndv(x) = E[X^n]
$$
{{</ math.inline >}}

# <mark> Markov inequality </mark>
{{< math.inline >}}

Let X be any positive continuous random variable, we can write:
$$
\begin{align*}
E[X] &= \int_{-\infty}^{\infty} xf_X(x)dx \\
     &= \int_{0}^{\infty} xf_X(x)dx \\
    &\geq \int_{a}^{\infty}xf_X(x)dx \\
    &\geq \int_{a}^{\infty}af_X(x)dx \\
    &= a\int_{a}^{\infty}f_X(x)dx \\
    &= aP(X\geq a)
\end{align*}
$$
Thus, we conclude
$$
P(X>a) \leq \frac{E[X]}{a}\ \ for\ any\ a > 0 
$$
That is the Markov inequality.
{{</ math.inline >}}
# <mark> Chebyshev's Inequality </mark>
{{< math.inline >}}

Let \(X\) be any random variable. If you define \(Y=(X−E[X])^2\), then \(Y\) is a nonnegative random variable, so we can apply Markov's inequality to \(Y\). In particular, for any positive real number \(b\), we have:
$$
P(Y\geq b^2) \leq \frac{E[Y]}{b^2}
$$
we have that:
$$
E[Y]=E(X-E[X])^2 = Var(X)\, \\
 P(Y \geq b^2) =P((X - E[X])^2 \geq b^2) = P(|X -E[X]| \geq b)
$$
so we obtain:
$$
P(|X -E[X]| \geq b) \leq \frac{Var(X)}{b^2}
$$
That is the Chebyshev's Inequality.
{{</ math.inline >}}
# <mark>Law of Large Numbers </mark>
The law of large numbers has a very central role in probability and statistics. It states that if you repeat an experiment independently a large number of times and average the result, what you obtain should be close to the expected value. There are two main versions of the law of large numbers. They are called the weak and strong laws of the large numbers.
## Weak laws of large numbers (WLLN)
{{< math.inline >}}
Let \(x_1, X_2, ..., X_n\) be i.i.d. random variables with a finite expected value \(E[X_i] = \mu < \infty\). The, for any \(\epsilon > 0\):
$$
\lim_{n \to \infty}P(|\bar{X} - \mu| \geq \epsilon) = 0
$$
Proof:
we assume that \(Var(X)=\sigma^2\) is finite. Using the Chebyshev's inequality:
$$
P(|\bar{X} - \mu| \geq \epsilon) \leq \frac{Var(\bar(X))}{\epsilon^2} = \frac{Var(X)}{n\epsilon^2}
$$
wich goes to zero as \(n \to \infty\).
{{</ math.inline >}}
# References
[1] en.wikipedia.org, "Lebesgue–Stieltjes integration", [URL](https://en.wikipedia.org/wiki/Lebesgue%E2%80%93Stieltjes_integration), <br>
[2] en.wikipedia.org, "Riemann–Stieltjes integral", [URL](https://en.wikipedia.org/wiki/Riemann%E2%80%93Stieltjes_integral), <br>
[3] probabilitycourse.com, "Markov and Chebyshev Inequalities", [URL](https://www.probabilitycourse.com/chapter6/6_2_2_markov_chebyshev_inequalities.php), <br>
[4] probabilitycourse.com, "Law of Large Numbers", [URL](https://www.probabilitycourse.com/chapter7/7_1_1_law_of_large_numbers.php), <br>
