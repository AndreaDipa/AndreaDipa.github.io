+++
title = "Homework 3, research"
date = 2022-10-13T15:54:43+02:00
draft = false
author = "Andrea Di Paolo"
math = "true"
+++

Assignment:
<ul>
    <li> Illustrate the concept of conditional, joint, marginal (relative) frequency using a simple bivariate distribution, </li>
    <li> illustrate the concept of statistical independence and the resulting mathematical relationships between the above frequencies.</li>
</ul>
<!--more-->
In this post we will talk about what are marginal, joint and conditional frequency. We will also explain the concept of statistical independence and why, in case of independence, the relative joint frequencies are equal to the products of the corresponding marginal frequencies.

# <mark> Joint (relative) frequency </mark>
A **joint frequency** is how many times a combination of two conditions happens together.
Bivariate joint frequencies are displayed in the center of a frequency distribution table.


<table>
    <thead>
        <tr>
            <th></th>
            <th> Cats </th>
            <th> Fish </th>
            <th> Dogs </th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td> Man </td>
            <td> 2 </td>
            <td> 4 </td>
            <td> 6 </td>
            <td> 12 </td>
        </tr>
        <tr>
            <td>Woman</td>
            <td> 5 </td>
            <td> 3 </td>
            <td> 2 </td>
            <td> 10 </td>
        </tr>
        <tr>
            <td></td>
            <td> 7 </td>
            <td> 7 </td>
            <td> 8 </td>
            <td> 22 </td>
        </tr>
    </tbody>
</table>

 For example, the table above shows how many people (women and men) own which pets. The value at the “joint” of women cats is 5. Therefore, the joint frequency of women who own cats is 5. The edges, or totals of the table are called marginal distributions. </br>
 **Joint relative frequency** is the ratio of the frequency in a certain category and the total number of data points in that category. In the above table, 7 people own cats, and two of those are men. So the joint relative frequency of male cat owners is 2/7.
# <mark> Marginal (relative) frequency </mark>
Marginal relative frequency is the ratio between the frequency of a row total or column total to the total frequency of the data. It is commonly used to analyze general trends in one specific category of data.
$$
    Freq(fish) = \frac{Freq(fish)}{Freq(total)}= \frac{7} {22}
$$
# <mark> Conditional (relative) frequency </mark>
Conditional relative frequency is a fraction that tells you how many members of a group have a particular characteristic. More technically, it is the ratio of a frequency in the center of the table to the frequency’s row total or column total.
For example with our table we have that the conditional relative frequency that the person is a man, given that he own a fish is:
$$
    Freq(man | fish) = \frac{Freq(man \cap fish)}{Freq(fish)}= \frac{4} {7}
$$
# <mark> Statistical Independence </mark>
We ha ve statistical independence if:
$$
    Pr(A|B)=Pr(A)
$$
we say that A is statistically independent of B: whether B happens makes no difference to how often A happens. <br>
{{< math.inline >}}
Since \(Pr(A \cap B)=Pr(A|B)Pr(B)\), if A is independent of B, then
{{</ math.inline >}}

$$
    Pr(A \cap B) = Pr(A)Pr(B)
$$

If this holds, though, then B is also independent of A:

$$
    Pr(B|A)=\frac{Pr(A \cap B)} {Pr(A)} = \frac{Pr(A)Pr(B)} {Pr(A)} = Pr(B)
$$

# References
[1] statisticshowto.com, "Joint Frequency", 2022, [URL](https://www.statisticshowto.com/joint-frequency/), <br>
[2] statisticshowto.com, "Conditional Relative Frequency: How to Find Them", 2022, [URL](https://www.statisticshowto.com/conditional-relative-frequency/), <br>
[3] study.com, "All about Joint, Marginal, and Conditional Frequencies", [URL](https://study.com/learn/lesson/conditional-joint-marginal-relative-frequency-overview-comparison-examples.html#:~:text=%2C%20or%202%25.-,What%20is%20Marginal%20Relative%20Frequency%3F,one%20specific%20category%20of%20data.)., <br>
[4] stat.cmu.edu, "Lecture 5: Statistical Independence, Discrete Random Variables", 2005, [URL](https://www.stat.cmu.edu/~cshalizi/36-220/lecture-5.pdf).
