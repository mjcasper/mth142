# (S-3) Introduction to Series

In this lesson we are going to look at the definitions for series and partial sums, and how we define the convergence of a series using partial sums. We also see a few algebraic rules for combining convergent series.


By the end of this lesson, you will be able to write out the first few terms of the sequence of partial sums for a given series.


---


## Series



```{admonition} (Infinite) Series
Consider the infinite sequence $\displaystyle \left\{ a_n\right\}_{n=1}^{\infty}$. A **series** is an expression of the form:

$$
a_1+a_2+a_3+a_4+ \cdots + a_n+ \cdots
$$

which can also be written as

$$
\sum_{n=1}^{\infty} a_n \quad \text{or} \quad \sum a_n
$$

```

### Intuitive Definition

Essentially, we are trying to **add** all of the terms of an infinite sequence (in a specific order). As we're going to see, this cannot always be done:

- If the **sum exists** we say the series is **convergent.** 
- If the **sum does not exist,** we say the series is **divergent.**

### How do we add infinitely many terms?

Adding infinitely many terms is not like our usual $+$ operation. Sometimes we can do it, sometimes we can't. But as with anything involving infinity, the general strategy involves limits:

1. Add a finite number of terms.
2. Compute the limit as the number of terms we are adding approaches infinity.

---

## Partial Sums

We start by considering what happens when we add a finite number of terms from our sequence $\{a_n\}$. The result is called a partial sum.

```{admonition} Partial Sums
Given a series $\displaystyle \sum_{n=1}^{\infty} a_n$, we let $s_n$ denote the $n^{\text{th}}$ **partial sum:** 

$$
s_n = \sum_{i=1}^{n} a_i = a_1+a_2+a_3+a_4+ \cdots + a_n
$$

```

### Sequence of Partial Sums

So given a sequence $\{a_1, a_2, a_3, \dots, a_n, \dots  \}$ we can form a brand new sequence$ \{s_1, s_2, s_3, \dots, s_n, \dots  \}$, called the **sequence of partial sums,** where:

$$
s_1 & = a_1 \\[5pt]
s_2 & = a_1+a_2 \\[5pt]
s_3 & = a_1+a_2 +a_3 \\[5pt]
s_4 & = a_1+a_2 +a_3 +a_4\\[5pt]
$$


## Example 1

Write out the first 4 terms of the sequence of partial sums, for the series:

$$
\dfrac{1}{3}+\dfrac{1}{9}+\dfrac{1}{27}+\dfrac{1}{81}+\cdots + \dfrac{1}{3^n}+\cdots
$$

````{dropdown} Solution (Click to see the steps.)
We start by writing out the original sequence $\{a_n\}$.

$$
\{a_n\}_{n=1}^{\infty} = \left\{ \dfrac{1}{3},\dfrac{1}{9},\dfrac{1}{27},\dfrac{1}{81},\dots , \dfrac{1}{3^n},\dots \right\}
$$

From here we add progressively more and more of the terms together to get our partial sums:

$$
s_1 & = a_1 & = \dfrac{1}{3}  & = \dfrac{1}{3}\\[5pt]
s_2 & = a_1 +a_2 & = \dfrac{1}{3} +\dfrac{1}{9} & = \dfrac{4}{9} \\[5pt]
s_3 & = a_1 +a_2 +a_3 & = \dfrac{1}{3} +\dfrac{1}{9}+\dfrac{1}{27} & = \dfrac{13}{27}\\[5pt]
s_4 & = a_1 +a_2 +a_3 +a_4 \quad & = \dfrac{1}{3} +\dfrac{1}{9}+\dfrac{1}{27}+\dfrac{1}{81} \quad & = \dfrac{40}{81}\\[5pt]
$$

The sequence of partial sums is therefore:

$$
\{s_n\}_{n=1}^{\infty} = \left\{ \dfrac{1}{3}, \dfrac{4}{9},  \dfrac{13}{27}, \dfrac{40}{81}, \dots \right\}
$$


````


## Example 2

Write out the first 5 terms of the sequence of partial sums, for the series:

$$
\sum_{n=1}^{\infty} \dfrac{1}{n}
$$


````{dropdown} Solution (Click to see the steps.)
We start by writing out the original sequence $\{a_n\}$.

$$
\{a_n\}_{n=1}^{\infty} = \left\{ 1, \dfrac{1}{2},\dfrac{1}{3},\dfrac{1}{4},\dfrac{1}{5},\dots , \dfrac{1}{n},\dots \right\}
$$

From here we add progressively more and more of the terms together to get our partial sums:

$$
s_1 & = a_1 & = 1  & = 1\\[5pt]
s_2 & = a_1 +a_2 & = 1 +\dfrac{1}{2} & = \dfrac{3}{2} \\[5pt]
s_3 & = a_1 +a_2 +a_3 & = 1 +\dfrac{1}{2} +\dfrac{1}{3} & = \dfrac{11}{6}\\[5pt]
s_4 & = a_1 +a_2 +a_3 +a_4 \quad & = 1 +\dfrac{1}{2} +\dfrac{1}{3}+\dfrac{1}{4} \quad & = \dfrac{25}{12}\\[5pt]
s_5 & = a_1 +a_2 +a_3 +a_4 +a_5 \quad & = 1 +\dfrac{1}{2} +\dfrac{1}{3}+\dfrac{1}{4} +\dfrac{1}{5}\quad & = \dfrac{137}{60}\\[5pt]
$$

The sequence of partial sums is therefore:

$$
\{s_n\}_{n=1}^{\infty} = \left\{ 1, \dfrac{3}{2}, \dfrac{11}{6},  \dfrac{25}{12}, \dfrac{137}{60}, \dots \right\}
$$


````


<!--

---

## Series Convergence

```{admonition} Convegence of a Series
A series $\sum a_n$ is said to be **convergent** if the sequence $\{s_n\}$ of partial sums converges to some number $s$. This number $s$ is called the **sum** of the series. And we write:

$$
\sum_{n=1}^{\infty} a_n = \lim_{n\to \infty} \sum_{i=1}^n a_i= \lim_{n\to \infty} s_n = s
$$


---

On the other hand, a series $\sum a_n$ is said to be **divergent** if the sequence $\{s_n\}$ of partial sums diverges.

```

A few comments:

1. It is usually difficult to determine a nice, simple formula for the general term $s_n$ of the sequence of partial sums.
1. Even if we know a series converges, the exact sum is usually difficult to determine. 



---


## Example 3


Show that the following series is convergent and find its sum.

```{math}
\sum_{n=1}^{\infty} \dfrac{1}{n(n+1)}
```


````{dropdown} Solution (Click to see the steps.)

```{tabbed} Step 1
We notice that the $n$-values start with $n=3$. To find the first four terms of the sequence, we will plug $n=3$, $n=4$, $n=5$, and $n=6$ into the formula of the general term:

$$
a_n=(-1)^n (n+1)
$$

```

```{tabbed} Step 2

Let's calculate these:

$$
n=3 & \quad \longrightarrow \quad & (-1)^3 (3+1) = -4\\[10pt]
n=4 & \quad \longrightarrow \quad & (-1)^4 (4+1) = 5\\[10pt]
n=5 & \quad \longrightarrow \quad & (-1)^5 (5+1) = -6 \\[10pt]
n=6 & \quad \longrightarrow \quad & (-1)^6 (6+1) = 7\\[10pt]
$$

```

```{tabbed} Step 3

Finally we write out the first four terms of our sequence:

$$
\bigg\{ -4, 5, -6, 7 , \dots \bigg\}
$$

```


````

---


## Algebraic Properties

Convergent series behave very nicely with addition, subtraction, and constant multiplication.

```{panels}
:column: col-lg-12 p-2


Algebraic Properties of Convergent Series
^^^

If $\sum a_n$ and $\sum b_n$ are convergent series, then so are the series:

$$
\sum_{n=1}^{\infty} c a_n & = c \cdot \sum_{n=1}^{\infty} a_n  \\[10pt]
\sum_{n=1}^{\infty} \big(a_n+b_n \big) & = \sum_{n=1}^{\infty} a_n +\sum_{n=1}^{\infty} b_n \\[10pt]
\sum_{n=1}^{\infty} \big(a_n-b_n \big) & = \sum_{n=1}^{\infty} a_n -\sum_{n=1}^{\infty} b_n  \\[10pt]

$$


```







## Example 4


Determine the sum of the series:


```{math}
\sum_{n=1}^{\infty} \left(\dfrac{5}{3^n}-\dfrac{1}{2^n}\right)
```

Given that we know:

$$
\sum_{n=1}^{\infty} \dfrac{1}{3^n} = \tfrac{1}{2} \qquad \text{and} \qquad \sum_{n=1}^{\infty} \dfrac{1}{2^n} = 1
$$

````{dropdown} Solution (Click to see the steps.)

```{tabbed} Step 1
We notice that the $n$-values start with $n=0$. To find the first four terms of the sequence, we will plug $n=0$, $n=1$, $n=2$, and $n=3$ into the formula of the general term:

$$
a_n=\dfrac{2^n}{n!}
$$

```

```{tabbed} Step 2

Let's calculate these:

$$
n=0 & \quad \longrightarrow \quad & \dfrac{2^0}{0!} = 1\\[10pt]
n=1 & \quad \longrightarrow \quad & \dfrac{2^1}{1!} = 2\\[10pt]
n=2 & \quad \longrightarrow \quad & \dfrac{2^2}{2!} = 2\\[10pt]
n=3 & \quad \longrightarrow \quad & \dfrac{2^3}{3!} = \tfrac{4}{3}\\[10pt]
$$

```

```{tabbed} Step 3

Finally we write out the first four terms of our sequence:

$$
\bigg\{ 1, 2, 3, \tfrac{4}{3} , \dots \bigg\}
$$

```


````

-->
