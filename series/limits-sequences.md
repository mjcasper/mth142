# (S-2) Limits of Sequences

In this lesson we are going to see how to calculate the limit of a sequence and ultimately determine whether the sequence is convergent or divergent.


---


## Definition of Limit



```{admonition} Limit of a Sequence 
The **limit of a sequence** is the number $L$ such that when we make $n$ sufficiently large positive, the terms of our sequence $a_n$ become very close to this number $L$. We write:

$$
\lim_{n\to \infty} a_n = L
$$

- **Converges:** the sequence is convergent if this limit exists.
- **Diverges:** the sequence is divergent if this limit does not exist.

```

### Graphical Representation


![sequence1](../images/sequence3.png)



## Limit Laws

If $\{a_n\}$ and $\{b_n\}$ are convergent sequences, then:

```{panels}
Constants
^^^
$$
\lim_{n\to\infty} c & = c \\[10pt]
\lim_{n\to\infty} c\cdot a_n & = c\cdot \lim_{n\to\infty} a_n \\[10pt]
(*)\quad \lim_{n\to\infty} \big( a_n \big)^p & = \bigg(\lim_{n\to\infty} a_n \bigg)^p 
$$

---

Arithmetic
^^^
$$
\lim_{n\to\infty} \big(a_n+b_n \big) & = \lim_{n\to\infty} a_n + \lim_{n\to\infty} b_n \\[10pt]
\lim_{n\to\infty} \big(a_n-b_n \big) & = \lim_{n\to\infty} a_n - \lim_{n\to\infty} b_n \\[10pt]
\lim_{n\to\infty} \big(a_n\cdot b_n \big) & = \lim_{n\to\infty} a_n \cdot \lim_{n\to\infty} b_n \\[10pt]
(*)\quad  \lim_{n\to\infty} \dfrac{a_n}{b_n} & = \dfrac{\displaystyle \lim_{n\to\infty} a_n}{\displaystyle \lim_{n\to\infty} b_n} \\[10pt]
$$


```

**Disclaimer:** Two of the above limits laws have some extra conditions.
- For the power function property, we additionally require $p>0$ and $a_n>0$
- For the quotient property, we additionally require $\displaystyle \lim_{n\to\infty}b_n \neq 0$.






---


## Example 1


Calculate the following limit:

```{math}
\lim_{n\to\infty}\dfrac{3n}{2n-1}
```

````{dropdown} Solution (Click to see the steps.)


For limits at infinity like this, we start with our $\tfrac{1}{n}$-method: 
- Identify the largest power of $n$ in the denominator.
- Divide each term in the numerator and the denominator by this largest power.

$$
\lim_{n\to\infty}\dfrac{3n}{2n-1} &= \lim_{n\to\infty}\dfrac{3n}{2n-1}\cdot \dfrac{\tfrac{1}{n}}{\tfrac{1}{n}}\\[10pt]
&= \lim_{n\to\infty}\dfrac{\tfrac{3n}{n}}{\tfrac{2n}{n}-\tfrac{1}{n}}\\[10pt]
&= \lim_{n\to\infty}\dfrac{3}{2-\tfrac{1}{n}}\\[10pt]
$$

Use the limit laws:

$$
= \dfrac{\displaystyle \lim_{n\to\infty}3}{\displaystyle \lim_{n\to\infty}2-\lim_{n\to\infty}\tfrac{1}{n}}= \dfrac{3}{2-0}= \dfrac{3}{2}\
$$

And there we have it!

One thing to notice is that the limit of $\tfrac{1}{n}$ is one of our $\tfrac{1}{\infty}$-forms and so goes to $0$.

````

---

## Real Variable Functions

There is a result that allows us to use all of the techniques for calculating limits at infinity that we developed back when we were talking about real variable functions:


```{admonition} Theorem
Given sequence $\{a_n\}$, suppose $a_n=f(n)$ for some real variable function&nbsp;$f$.

$$
\text{If} \quad \lim_{x\to\infty} f(x) = L \quad \text{then} \quad \lim_{n\to\infty} a_n = L
$$

```


![sequence1](../images/sequence1.png)


### Special Case

```{admonition} Important Limit
For $r>0$ we have: $\displaystyle \lim_{n\to\infty} \dfrac{1}{n^r} = 0 $
```

To prove this, we need to relate this sequence to a real variable function: 

$$
a_n = \dfrac{1}{n^r} \qquad \longrightarrow \qquad f(x)=\dfrac{1}{x^r}
$$

And then we consider the limit of this real variable function instead:

$$
\lim_{n\to\infty} \dfrac{1}{n^r} = \lim_{x\to\infty} \dfrac{1}{x^r} =0
$$



### L'Hospital's Rule

```{note}
If we can relate our sequence back to a real variable function, then we can use L'Hospital's Rule to help calculate limits, where applicable.
```



## Example 2


Calculate the following limit:

```{math}
\lim_{n\to\infty}\dfrac{2n}{e^n}
```

````{dropdown} Solution (Click to see the steps.)


We notice that this is one of our $\tfrac{\infty}{\infty}$ indeterminate forms, so we want to use L'Hospital's Rule. 

First we need to relate this sequence to a real variable function: 

$$
a_n = \dfrac{2n}{e^n} \qquad \longrightarrow \qquad f(x)=\dfrac{2x}{e^x}
$$

We consider the limit of this function instead:

$$
\lim_{n\to\infty}\dfrac{2n}{e^n} = \lim_{x\to\infty}\dfrac{2x}{e^x} \stackrel{H}{=} \lim_{x\to\infty}\dfrac{\big[2x\big]'}{\big[e^x\big]'} = \lim_{x\to\infty}\dfrac{2}{e^x} =0
$$



And there we go! We see that the limit of our sequence is 0 (that final limit is a $\tfrac{c}{\infty}$-form and so goes to $0$).



````

