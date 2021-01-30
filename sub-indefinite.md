# Substitution Rule for Indefinite Integrals

## Derivative and Integration Rules
Essentially each derivative rule that we have seen, has a complementary integration counterpart. For example, we have the differentiation and integration rules for **addition:** 

$$
\dfrac{d}{dx}\big[f(x)+g(x)\big] = f'(x)+g'(x)
$$ 

$$
\displaystyle \int \big( f(x)+g(x)\big)dx =\int f(x) dx + \int g(x) dx
$$




Similar matching rules also exist for **subtraction** and  **constant multiplication.** Now you might be wondering, what is the integration rule that corresponds with the **Chain Rule?**

$$
\textbf{Chain Rule: }\dfrac{d}{dx}\bigg[f(g(x))\bigg] = f'(g(x))\cdot g'(x)
$$

```{dropdown} **Question:** What Integration Rule do <em>you</em> think corresponds with the chain rule?
Why, **substitution rule** of course!
```

---

## The Substitution Rule

````{admonition} Substitution Rule
If $u=g(x)$ is a differentiable function and $f$ is continuous, then
```{math}
\int f\big( g(x)\big)g'(x)\,  dx = \int f(u) \, du
```
````




### How It Works
For the most part, we tend to think of the substitution rule, not so much as a formula to memorize, but rather as a process:

1. Choose $u$ and calculate $du$
2. Substitute these values into the original integral.
3. Integrate this new integral in terms of $u$.
4. Convert the antiderivative from $u$ back to the original variable.

```{warning}
One of the key things to remember in Step 2, is that we need to **convert all instances of our original variable.**

- If we start with $x$, then all of the $x$-terms, including $dx$, need to be replaced. And this needs to be done before we move onto step 3.
``` 

### Differentials

Part of this process is that once we choose $u$, it is up to us to actually calculate the new differential $du$. How?

````{admonition} Differentials
If $u=g(x)$ is a differentiable function, then the **differential** $du$ is:
```{math}
du = g'(x) \, dx
```
Remember to put the $dx$ at the end.
````


---

## Example 1
Evaluate the following integral:

$$
\int (3x+4)^{10} \cdot 3\;dx
$$

````{tabbed} Solution
Click through the steps to see what we do.

If you want, give it a try first! (Use the steps listed above as a guide to get you started.)
````

````{tabbed} Step 1
Our first step is choose $u$: 
```{math}
 u=3x+4
```
and then we calculate $du$ to get:
```{math}
 du = [3x+4]' \cdot dx  \longrightarrow du= 3 \, dx
```

````

````{tabbed} Step 2
Next, we plug-in our choice for $u$ and what we calculated for $du$ to get: 
```{math}
\int (3x+4)^{10} \cdot 3\;dx = \int u^{10} \;du
```
````

````{tabbed} Step 3
The resulting integral can now be solved by basic **power rule**. 
```{math}
\int u^{10} \;du = \dfrac{1}{11}u^{11} +C
```
````

````{tabbed} Step 4
Once we are done finding the antiderivative in terms of $u$, the very last step is to convert back to $x$: 
```{math}
\dfrac{1}{11}u^{11} +C = \dfrac{1}{11}(3x+4)^{11} +C 
```
(Don't forget $+C$ for indefinite integrals!)
````

## How To Choose?

At this point, you might be asking: In that last example, how did you know that we needed to pick $u=3x+4$? Well, that's a very good question, with a not too satisfying answer: practice and trial-and-error.

The strategy that tends to work the most often is to break the integral into two pieces. 

````{panels}
:column: col-5
:card: border-2
Complicated Piece
^^^
```{math}
(3x+4)^{10}
```
---
Less-Complicated Piece
^^^
```{math}
3
```
````

And then from there we identify the inner function of the **complicated piece.** 

In our case, the $3x+4$ is the inner function because it is *inside* $(\cdot )^{10}$ the power function "raise to the power 10." In general:

| Complicated Piece | What We Choose | Why? |
|:-----------------:|----------------|------|
|$\big(\cdot\big)^n$ | Terms inside the parentheses | $\displaystyle \int u^n \, du = \dfrac{1}{n+1} u^{n+1}+C$ |
|$\dfrac{1}{\big(\cdot\big)}$ | Terms inside the denominator | $\displaystyle \int \dfrac{1}{u} \, du = \ln\vert u\vert + C$ |
|$e^{\big(\cdot\big)}$ | Terms inside the exponent | $\displaystyle \int e^u \, du = e^u+C$ |


---

## Example 2
Evaluate the following integral:

$$
\int 2x e^{x^2}\;dx
$$

```{dropdown} **Question:** What do <em>you</em> think we should pick for $u$ in this example?
**Answer:** Letting $u=x^2$ should work.
```

---

## Example 3
Evaluate the following integral:

$$
\int \dfrac{3x^2}{x^3+1}\;dx
$$

```{dropdown} **Question:** What do <em>you</em> think we should pick for $u$ in this example?
**Answer:** Letting $u=x^3+1$ should work.
```

