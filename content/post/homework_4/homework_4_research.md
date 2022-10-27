+++
title = "Homework 4, research"
date = 2022-10-23T18:41:31+02:00
draft = false
author = "Andrea Di Paolo"
math = "true"
+++
Assignment:
<ul>
    <li> Illustrate the parallel between the properties of the relative frequency and the axioms for probability, </li>
    <li> discuss some concrete examples of Measure Space (omega,epsilon,P), </li>
    <li> illustrate how Measure Theory provides the mathematical foundation for Probability. </li>
</ul>
<!--more-->

# <mark> Axioms for probability vs relative frequency </mark>
{{< math.inline >}}
Let \(\Omega\) denote an event set with a probability measure P defined over it, such that probability of any event \(A \subset \Omega\) is given by \(P(A)\). Then, the probability measure obeys the following axioms:
<ol>
    <li> Probability cannot be negative. The smallest value for \(P(A)\) is zero and if \(P(A)=0\), then the event A will never happen: <br>
        <center>\(P(A) \geq 0\)</center>
    </li>
    <li> Probability of the whole sample space is equal to one:
        <center> \(P(\Omega)=1\) </center>
    </li>
    <li> If some events are disjoint (i.e., there is no overlap between them), then the probability of their union must be the summations of their probabilities:
        <center> \(P(\cup^{\infty}_{i=1}E_i) = \sum^{\infty}_{i=1}P(E_i)\)</center>
    </li>
</ol>
Relative frequency, instead has the following basic properties:
<ul>
    
    <li> \(0 \leq f_A \leq 1\),</li>
    <li> \(f(\emptyset)\) = 0,</li>
    <li> \(f(\Omega) = 1\),
    <li> \(f_{A \cup B} = f_A + f_B\) if A and B are disjoint,</li>
    <li>\(f_{A \cup B} = f_A + f_B - f_{A \cap B}\) </li>    
</ul>
as we can see these properties are very similar to probability axioms.
{{</ math.inline >}}

# <mark> Measure space in practice </mark> <br>
{{< math.inline >}}

If the experiment consists of just one flip of a fair coin, then the outcome is either heads or tails: \( \Omega =\{H,T\} \). The \(\sigma-algebra\ F = 2^{\Omega}\) contains \(2^2 = 4\) events. Then \(F=\{\{\},\{H\},\{T\},\{H,T\}\}\). There is a fifty percent chance of tossing heads and fifty percent for tails, so the probability measure in this example is <br>\(P(\{\})=0, P(\{H\})=0.5,P(\{T\})=0.5, P(\{H,T\})=1\).

{{</ math.inline >}}
# <mark> Measure theory and probability </mark>
{{< math.inline >}}
A measure on an algebra \(A\) is a set function \(\mu: A \to [0, \infty]\) that satisfy the following properties: <br>
<ul>
    <li> Non negativity: For all \(A \in A_n\), we have \(\mu(A) \geq 0\)</li>
    <li> Null empty set: \(\mu(\emptyset)=0\).</li>
    <li> Countable additivity: \(\mu(\cup_{n \geq 1}A_n) = \sum_{n \geq 1}\mu(A_n)\). </li>
    
</ul>
A probability measure is a measure with total mass 1, that is, \(\mu(\Omega) = 1\) and as we can see the perobability axioms just comes out from those properties.
{{</ math.inline >}}


# References
[1] probabilitycourse.com, "Probability", [URL](https://www.probabilitycourse.com/chapter1/1_3_2_probability.php), <br>
[2] le.ac.uk, "AXIOMATIC PROBABILITY AND POINT SETS", [URL](https://www.le.ac.uk/users/dsgp1/COURSES/LEISTATS/STATSLIDE2.pdf), <br>
[3] en.wikipedia.org, "Probability space", [URL](https://en.wikipedia.org/wiki/Probability_space#Example_1), <br>
[4] galton.uchicago.edu, "Measure-Theoretic Probability I", 2017, [URL](http://galton.uchicago.edu/~lalley/Courses/381/measure.pdf), <br>
[5] en.wikipedia.org, "Measure (mathematics)", [URL](https://en.wikipedia.org/wiki/Measure_(mathematics)#Definition).
