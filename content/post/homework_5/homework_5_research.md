+++
title = "Homework 5, research"
date = 2022-10-29T17:45:00+02:00
draft = false
author = "Andrea Di Paolo"
math = true
+++
Assignment:
<ul>
    <li>Explain all possible derivation of the arithmetic mean and in general of the other common types of averages,</li>
    <li>illustrate the difference between "mathematical convergence" and "convergence" in probability,</li>
    <li>illustrate the differences between Descriptive Statistics and Inferential Statistics and the role of probability and probability distributions.</li>
</ul>
<!--more-->

# <mark>Means</mark>
Mean in statistics refers to the average of a collection of values. The collection of values can be two or more. It is a measure of central tendency and output typical value in a collection or set of data. The mean is one of the simple methods employed in descriptive statistics used to interpret or summarize the given data set and derive relevant information or conclusion about the population or sample of a population represented by the data set. Most of the time, it is imperative to derive an average to understand the overall performance and simplify the statistical calculations. Fundamentally, it is the value obtained by dividing the sum of all observations by the number of observations: <br>
$$
\bar{x} = \frac{\sum{x_i}}{n}
$$
## Arithmetic Mean 
Arithmetic Mean is also referred to as the arithmetic average. It is calculated by summing all the observations and then dividing it by the total number of observations.
## Geometric Mean 
{{< math.inline >}}
Geometric Mean is a central tendency method that determines the power average of a growth series data. It is computed as the \(n^{th}\) root of the multiplicative result of all the data figures up to n. The method is suitable for determining the average value appreciation of a particular investment or the overall portfolio—for a given time frame. It accurately evaluates average values pertaining to a continuous series of interdependent values. The geometric mean calculation helps investors ascertain the compounding average for a given data series. It is evaluated using the following formulas:
{{</ math.inline >}}
$$
GM = \sqrt[n]{\prod^n_{i=1}x_i}
$$
## Harmonic Mean
{{< math.inline >}}
The harmonic mean helps to find multiplicative or divisor relationships between fractions without worrying about common denominators. Harmonic means are often used in averaging things like rates (e.g., the average travel speed given a duration of several trips).
The harmonic mean is the reciprocal of the arithmetic mean of reciprocals, i.e., the average calculated by dividing the number of observations in the given dataset by the sum of its reciprocals \(\frac{1}{Xi}\) of every observation in the given dataset.
{{</ math.inline >}}
$$
HM = \frac{n}{\sum(\frac{1}{x_i})}
$$
## Root Mean Square
{{< math.inline >}}
The root mean square of a set of numbers \(x_{i}\) is defined as the square root of the mean square of the set.
{{</ math.inline >}}
$$
RMS = \sqrt{\frac{\sum_{i=1}^{n}x_i^2}{n}}
$$
It is useful when trying to measure the average “size” of numbers, where their sign is unimportant, as the squaring makes all of the numbers non-negative.
## Contraharmonic Mean
The contraharmonic mean of a set of positive numbers is defined as the arithmetic mean of the squares of the numbers divided by the arithmetic mean of the numbers:
$$
CM(x_i) = \frac{\frac{1}{n}(\sum_{i=1}^{n}x^2_i)}{\frac{1}{n}(\sum_{i=1}^{n}x_i)}
$$

# <mark> Mathenmatical convergence vs Convergence in probability </mark> 
{{< math.inline >}}

Convergence, in mathematics, property (exhibited by certain infinite series and functions) of approaching a limit more and more closely as an argument (variable) of the function increases or decreases or as the number of terms of the series increases. For example, the function \(y = \frac{1}{x}\) converges to zero as x increases. Although no finite value of x will cause the value of y to actually become zero, the limiting value of y is zero because y can be made as small as desired by choosing x large enough. The line \(y = 0\) (the x-axis) is called an asymptote of the function. <br>

Convergence in probability is stronger than convergence in distribution. In particular, for a sequence \(X_1, X_2, X_3, ..., X_n\) to converge to a random variable \(X\), we must have that \(P(\lvert X_n−X \rvert \geq \epsilon)\) goes to 0 as \(n \to \infty\), for any \(\epsilon > 0\). To say that \(X_n\) converges in probability to \(X\), we write
{{</ math.inline >}}
$$
X_n \xrightarrow p X
$$

# <mark> Descriptive Statistics vs Inferential Statistics </mark>

***Descriptive statistics*** are used to describe the characteristics or features of a dataset. The term "descriptive statistics" can be used to describe both individual quantitative observations (also known as "summary statistics") as well as the overall process of obtaining insights from these data. Suppose we want to describe the test scores in a specific class of 30 students. We record all of the test scores and calculate the summary statistics and produce graphs. <br>
***Inferential statistics*** focus on making generalizations about a larger population based on a representative sample of that population. Because inferential statistics focuses on making predictions (rather than stating facts) its results are usually in the form of a probability. In descriptive statistics, we picked the specific class that we wanted to describe and recorded all of the test scores for that class. Nice and simple. For inferential statistics, we need to define the population and then draw a random sample from that population.
# References
[1] wallstreetmojo.com, "Mean", [URL](https://www.wallstreetmojo.com/mean/#h-mean-explained), <br>
[2] investopedia.com, "Harmonic Mean Definition: Formula and Examples", 2020, [URL](https://www.investopedia.com/terms/h/harmonicaverage.asp#:~:text=The%20harmonic%20mean%20helps%20to,a%20duration%20of%20several%20trips).), <br>
[3] undergroundmathematics.org, "Root mean square", [URL](https://undergroundmathematics.org/glossary/root-mean-square#:~:text=The%20root%20mean%20square%20is%20a%20type%20of%20mean.&text=It%20is%20useful%20when%20trying,1%2C%20%E2%80%A6%2C%20xn.), <br>
[4] en.wikipedia.org, "Contraharmonic mean", [URL](https://en.wikipedia.org/wiki/Contraharmonic_mean), <br>
[5] britannica.com, "convergence", [URL](https://www.britannica.com/science/convergence-mathematics). <br>
[6] probabilitycourse.com, "Convergence in Probability", [URL](https://www.probabilitycourse.com/chapter7/7_2_5_convergence_in_probability.php). <br>
[7] careerfoundry.com, "What’s the Difference Between Descriptive and Inferential Statistics?", 2021, [URL](https://careerfoundry.com/en/blog/data-analytics/inferential-vs-descriptive-statistics/), <br>
[8] statisticsbyjim.com, "Difference between Descriptive and Inferential Statistics", [URL](https://statisticsbyjim.com/basics/descriptive-inferential-statistics/).