---
title: "Homework 8, research on application"
date: 2022-11-24T13:20:01+01:00
draft: false
author: "Andrea Di Paolo"
math: true
---
Assignment:
<ul>
    <li>Find in the web what are the distributions that you just simulated.</li>
</ul>
<!--more-->

# <mark> X </mark>
X has normal distribution generated with the Marsaglia method.

# <mark> X^2 </mark>
X^2 has Chi-squared distribution, which is defined as
$$
Q = \sum_{i=1}^k Z^2_i
$$
# <mark> X/Y^2 </mark>
X/Y^2 has Student-T distribution:
$$
T_n = \frac{Z}{\sqrt{K/n}}
$$
# <mark> X^2/Y^2 </mark>
X^2/Y^2 has Fisher-Snedecor distribution:
$$
F = \frac{X/m}{Y/n},
$$
where X and Y both have Chi-squared distribution; m and n are the degrees of freedom
# <mark> X/Y </mark>
X/Y has Cauchy distribution, its density function is
$$
f_{(x_0,y_0)}(x) = \frac{y_0}{(x - x_0)^2 + y_0^2}
$$