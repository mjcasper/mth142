# (AI-5) Improper Integrals

In this lesson we are going to see how we can generalize our definition of the definite integral to include improper integrals:
- integrals over infinite intervals 
- integrals of functions with an infinite discontinuity

By the end of this lesson, you will be able to determine whether an improper integral is convergent or divergent, and if convergent, be able to evaluate the integral. 



## Fundamental Theorem of Calculus Part&nbsp;2

We begin by recalling the big one. The theorem that motivates most of what we do with integral calculus: 

```{admonition} Fundamental Theorem of Calculus Part 2
If $f$ is continuous on $[a,b]$ then:

$$
\int_a^b f(x)\, dx = F(b)-F(a)
$$

where $F$ is any antiderivative of $f$.
```

Notice that there are really two conditions for this theorem to hold:

1. The interval $[a,b]$ is finite.
2. Function $f$ is continuous on the interval.

If we relax either of these conditions we can get what are called **improper integrals.**




## (Right) Infinite Intervals


```{admonition} (Right Hand) Improper Integrals
If $f(x)$ is continuous for $x\geq a$ then,

$$
\int_a^{\infty} f(x)\, dx = \lim_{b\to\infty} \int_a^{b} f(x)\, dx
$$

```

We say that this improper integral is **convergent** if the limit exists. If the limit does not exist, then we say the improper integral is **divergent.** 

### Area Interpretation

For non-negative functions we interpret this improper integral as representing the **area under the curve** $y=f(x)$ for $x\geq a$.

![improper1](../images/improper1.png)

## Example 1
Determine if the following improper integral is convergent or divergent. If convergent, find its value:

$$
\int_0^{\infty} e^{-2x}\, dx
$$




``````{dropdown} Solution (Click to see the steps.)



`````{tabbed} Step 1
We notice that we are attempting to integrate over infinite interval $[0,\infty)$, so we have an improper integral. 

This means we first need to use the definition and rewrite this integral as a limit:


$$
\int_0^{\infty} e^{-2x}\, dx = \lim_{b\to\infty} \int_0^{b} e^{-2x}\, dx 
$$

This is a crucial step. 

What we've done here is effectively separate the $\infty$ from our integration. The only way we can deal with $\infty$ is with limits, we need to approach it. We cannot just plug $\infty$ into a function because it is **not a number that we can evaluate.**


`````

`````{tabbed} Step 2
Next we work on calculating the resulting definite integral:

$$
\lim_{b\to\infty} \int_0^{b} e^{-2x}\, dx & = \lim_{b\to\infty} -\tfrac{1}{2} e^{-2x}\biggr|_{x=0}^{x=b}\\[10pt]
& = \lim_{b\to\infty} \bigg(\left(-\tfrac{1}{2} e^{-2b}\right)-\left(-\tfrac{1}{2} e^{0}\right)\bigg)\\[10pt]
& = \lim_{b\to\infty} \bigg(\tfrac{1}{2}-\tfrac{1}{2} e^{-2b}\bigg)\\[10pt]
$$


`````

`````{tabbed} Step 3
Finally, we calculate the limit at infinity (using all of our techniques we learned back in Calculus 1.) And to help with this we rewrite any negative exponents as fractions. This just helps us conceptually see what is happening with the limit.

$$
& = \lim_{b\to\infty} \bigg(\tfrac{1}{2}-\tfrac{1}{2} e^{-2b}\bigg)\\[10pt]
& = \lim_{b\to\infty} \bigg(\tfrac{1}{2}-\tfrac{1}{2} \cdot \dfrac{1}{e^{2b}}\bigg)\\[10pt]
& = \tfrac{1}{2}-\tfrac{1}{2} \cdot 0\\[10pt]
& = \tfrac{1}{2}
$$

```{admonition} Limit at Infinity
Note that  $\dfrac{1}{e^{2b}}$ is one of our $\dfrac{1}{\infty}$-forms and so:

$$
\lim_{b\to\infty} \dfrac{1}{e^{2b}}=0
$$
```


`````


`````{tabbed} Conclusion
We have shown that the improper integral

$$
\int_0^{\infty} e^{-2x}\, dx = \dfrac{1}{2}
$$

and is therefore **convergent.**

`````





`````{tabbed} Area
Since $f(x)=e^{-2x}$ is a non-negative function, what we have just shown is that the area of the region under this curve starting at $x=0$ and extending infinitely far to the right is finite and:

$$
\text{Area } =\tfrac{1}{2}
$$


![improper2](../images/improper2.png)


`````




``````



## Example 2
Determine if the following improper integral is convergent or divergent. If convergent, find its value:

$$
\int_2^{\infty} \dfrac{1}{\sqrt{3x+5}}\, dx 
$$





``````{dropdown} Solution (Click to see the steps.)



`````{tabbed} Step 1
We notice that we are attempting to integrate over infinite interval $[2,\infty)$, so we have an improper integral. 

This means we first need to use the definition and rewrite this integral as a limit:


$$
\int_2^{\infty} \dfrac{1}{\sqrt{3x+5}}\, dx  = \lim_{b\to\infty} \int_2^{b} \dfrac{1}{\sqrt{3x+5}}\, dx 
$$

This is a crucial step. 

What we've done here is effectively separate the $\infty$ from our integration. The only way we can deal with $\infty$ is with limits, we need to approach it. We cannot just plug $\infty$ into a function because it is **not a number that we can evaluate.**


`````

`````{tabbed} Step 2
Next we work on calculating the resulting definite integral. Note that this is a $k$-form integral, so we can just do a mental $u$-substition.

$$
\lim_{b\to\infty} \int_2^{b} \dfrac{1}{\sqrt{3x+5}}\, dx & = \lim_{b\to\infty} \int_2^{b} (3x+5)^{-1/2}\, dx \\[10pt]
& = \lim_{b\to\infty} \tfrac{2}{3} (3x+5)^{1/2} \biggr|_{x=2}^{x=b}\\[10pt]
& = \lim_{b\to\infty} \bigg( \tfrac{2}{3} (3b+5)^{1/2}- \tfrac{2}{3} (11)^{1/2}\bigg)\\[10pt]
$$


`````

`````{tabbed} Step 3
Finally, we calculate the limit at infinity:

$$
\lim_{b\to\infty} \bigg( \tfrac{2}{3} (3b+5)^{1/2}- \tfrac{2}{3} (5)^{1/2}\bigg)= \infty
$$



```{admonition} Limit at Infinity
Note that  $(3b+5)^{1/2}$ is one of our $b^n$-forms and so:

$$
\lim_{b\to\infty} (3b+5)^{1/2}=\infty
$$
```


`````


`````{tabbed} Conclusion
We have shown that the improper integral

$$
\int_2^{\infty} \dfrac{1}{\sqrt{3x+5}}\, dx = \infty
$$

and is therefore **divergent.**

`````




`````{tabbed} Area
Since $f(x)= \tfrac{1}{\sqrt{3x+5}}$ is a non-negative function, what we have just shown is the area of the region under this curve starting at $x=2$ and extending infinitely far to the right is **infinite.**


![improper3](../images/improper3.png)


`````




``````




## Procedure

In general the steps for computing an improper integral are:

1. Rewrite the improper integral as a limit.
2. Integrate $\displaystyle \int_a^b f(x)\, dx$ like usual.
3. Calculate the limit.















