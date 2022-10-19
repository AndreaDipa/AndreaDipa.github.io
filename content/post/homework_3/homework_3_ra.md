+++
title = "Homework 3, research on application"
date = 2022-10-13T15:54:56+02:00
draft = false
author = "Andrea Di Paolo"
math = "true"
+++

Assignment:
<ul>
    <li> A survey on online algorithms (Welford), </li>
    <li> in particular, Knuth recursion for the computation of the arithmetic mean (average). </li>
</ul>
<!--more-->
An online algorithm is one that can process its input piece-by-piece in a serial fashion, i.e., in the order that the input is fed to the algorithm, without having the entire input available from the beginning.
In contrast, an offline algorithm is given the whole problem data from the beginning and is required to output an answer which solves the problem at hand.
# <mark> Welford's online algorithm </mark>
The standard deviation is a measure of how much a dataset differs from its mean; it tells us how dispersed the data are. A dataset that’s pretty much clumped around a single point would have a small standard deviation, while a dataset that’s all over the map would have a large standard deviation.<br>
{{< math.inline >}}
Given a sample \(x_1,…,x_N\), the standard deviation is defined as the square root of the variance:
{{</ math.inline >}}
$$
    s^2 = \frac{\sum_{i=1}^{N}(x_i - \bar{x})^2}{N-1}, s = \sqrt{s^2}
$$
{{< math.inline >}}
where \(\bar{x} = \frac{1}{N}\sum_{i=1}^{N}x_i \).
Welford method is derivable by looking at the differences between the sums of squared differences for \(N\) and \(N-1\):
{{</ math.inline >}}

$$
    (N-1)s^2_N - (N-2)s^2_{N-1} 
$$
{{< math.inline >}}

and with simple computation: 
    \((x_N-\bar{x}_N)(x_N-\bar{x}_{N-1})\).
{{</ math.inline >}}
So we can obtain the algorithm:
```
variance(samples):
  M := 0
  S := 0
  for k from 1 to N:
    x := samples[k]
    oldM := M
    M := M + (x-M)/k
    S := S + (x-M)*(x-oldM)
  return S/(N-1)
```
# <mark> Knuth's algorithm </mark>
Classical averaging with the aid of software can lead to several types of error, first and foremost Catastrophic Cancellation, i.e. the deletion of significant figures. In addition, for large amounts of data, there can be anomalies and disadvantages due to high calculation and memory times. <br>
In order to overcome this type of problem, the computer scientist Donald Knuth proposed a different algorithmic formulation for calculating the mean:   
<br>
{{< math.inline >}}
    \(\bar{x}_n = \bar{x}_{n-1} + \frac{1}{n}(x_n - \bar{x}_{n-1})\)
{{</ math.inline >}}

# References
[1] geeksforgeeks.org, "Online Algorithm", 2017, [URL](geeksforgeeks.org/online-algorithm/), <br>
[2] jonisalonen.com, "Welford’s method for computing variance", 2013 [URL](https://jonisalonen.com/2013/deriving-welfords-method-for-computing-variance/), <br>
[3] statisticaapplicata800375216.wordpress.com, "Algoritmo di Knuth per il calcolo della “running mean”,  2020 [URL](https://statisticaapplicata800375216.wordpress.com/2020/03/25/algoritmo-di-knuth-per-il-calcolo-della-running-mean/).