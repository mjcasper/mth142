# (I-1) Substitution Rule for Indefinite Integrals

## Derivative and Integration Rules
Essentially each derivative rule that we have seen, has a complementary integration counterpart. For example, we have the differentiation and integration rules for **addition:** 

$$
\dfrac{d}{dx}\big[f(x)+g(x)\big] = f'(x)+g'(x)
$$ 

$$
\displaystyle \int \big( f(x)+g(x)\big)\; dx =\int f(x) \; dx + \int g(x) \; dx
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
:column: col-sm
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

````{tabbed} Solution
Click through the steps to see what we do.

If you want, give it a try first! 
````

````{tabbed} Step 0
It sometimes is helpful to rewrite the integral by putting the complicated term first, and then any less-complicated terms next to the $dx$ (but still within the integral).
```{math}
\int 2x e^{x^2}\;dx=\int  e^{x^2}\cdot 2x\;dx
```
This step is not really necessary, but it can be helpful - especially if you are unsure of how to pick $u$.

````

````{tabbed} Step 1
Since the more complicated piece of our function is $e^{x^2}$, we choose $u$ to be the inner function: 
```{math}
 u=x^2
```
We also calculate $du$ to get:
```{math}
 du = \left[x^2\right]' \cdot dx  \longrightarrow du= 2x \, dx
```

````



````{tabbed} Step 2
Next, we plug-in our choice for $u$ and what we calculated for $du$ to get: 
```{math}
\int  e^{x^2}\cdot 2x\;dx = \int e^u \;du
```
````

````{tabbed} Step 3
The resulting integral can now be solved since it is one of our basic forms. 
```{math}
\int e^u \;du = e^u +C
```
````

````{tabbed} Step 4
Once we are done finding the antiderivative in terms of $u$, the very last step is to convert back to $x$: 
```{math}
e^u +C = e^{x^2} +C 
```
(Don't forget $+C$ for indefinite integrals!)
````



## Example 3
Evaluate the following integral:

$$
\int \dfrac{3x^2}{x^3+1}\;dx
$$

```{dropdown} **Question:** What do <em>you</em> think we should pick for $u$ in this example?
**Answer:** Letting $u=x^3+1$ should work.
```

````{tabbed} Solution
Click through the steps to see what we do.

If you want, give it a try first! 
````

````{tabbed} Step 0
Let's split up our function again and rewrite it with the complicated piece first:
```{math}
\int \dfrac{3x^2}{x^3+1}\;dx = \int \dfrac{1}{x^3+1}\cdot 3x^2\;dx
```
Again, this step is not really necessary, but it can be helpful for picking $u$.

````

````{tabbed} Step 1
Since the more complicated piece of our function is $\dfrac{1}{x^3+1}$, we choose $u$ to be the inner function: 
```{math}
 u=x^3+1
```
We also calculate $du$ to get:
```{math}
 du = \left[x^3+1\right]' \cdot dx  \longrightarrow du= 3x^2 \, dx
```

````



````{tabbed} Step 2
Next, we plug-in our choice for $u$ and what we calculated for $du$ to get: 
```{math}
\int \dfrac{1}{x^3+1}\cdot 3x^2\;dx = \int \dfrac{1}{u}\;du
```
````

````{tabbed} Step 3
The resulting integral can now be solved since it is one of our basic forms. 
```{math}
\int \dfrac{1}{u}\;du = \ln\vert u\vert + C
```
````

````{tabbed} Step 4
Once we are done finding the antiderivative in terms of $u$, the very last step is to convert back to $x$: 
```{math}
\ln\vert u\vert + C = \ln\lvert x^3+1\rvert + C
```
(Don't forget the absolute value signs!)
````


## Example 4
Evaluate the following integral:

$$
\int \dfrac{\ln x}{x}\;dx
$$

```{dropdown} **Question:** What do <em>you</em> think we should pick for $u$ in this example?
**Answer:** Hmmm... let's try to figure this one out.
```

````{tabbed} Solution
Click through the steps to see what we do.

If you want, give it a try first! 
````

`````{tabbed} Step 0
When we're trying to decide what to pick for $u$ it helps to split up the function a bit:
````{math}
\int \dfrac{\ln x}{x}\;dx = \int  \ln x\cdot \dfrac{1}{x}\;dx
````
Again, this step is not really necessary, but it can be helpful. So what are some possible choices for $u$? Well, let's look at all of the pieces we have there on the right. We could do:

````{panels}
:column: col-sm
:card: border-2
Option 1
^^^
```{math}
u=x
```
We **never** do this substitution, since it does not simplify our problem at all.
---
Option 2  
^^^
```{math}
u=\tfrac{1}{x}
```
If we calculate $du$ we get:
```{math}
du=-\tfrac{1}{x^2}\, dx
```
But this doesn't match up too nicely with the remaining $\ln x$ term.
---
Option 3
^^^
```{math}
u=\ln x
```
If we calculate $du$ we get:
```{math}
du=\tfrac{1}{x}\, dx
```
And this matches up perfectly with the remaining $\tfrac{1}{x}$ term. We have a winner!
````


`````

````{tabbed} Step 1
So, we're going to choose:
```{math}
 u=\ln x
```
And calculate:
```{math}
 du = \left[\ln x\right]' \cdot dx  \longrightarrow du= \dfrac{1}{x} \, dx
```

````



````{tabbed} Step 2
Next, we plug-in our choice for $u$ and what we calculated for $du$ to get: 
```{math}
\int \ln x\cdot \dfrac{1}{x}\;dx = \int u\;du
```
````

````{tabbed} Step 3
The resulting integral is now a nice power rule problem. 
```{math}
\int u\;du = \tfrac{1}{2}u^2 + C
```
````

````{tabbed} Step 4
And then finally we get back to $x$.
```{math}
\tfrac{1}{2}u^2 + C = \tfrac{1}{2}\left(\ln x\right)^2 + C
```

````

## Matching Differentials

Up until this point, all of the substitutions we have seen have had a perfect match between what we calculate for $du$ and the extra, leftover terms in our integral.

In example 3 we had:

````{panels}
:column: col-sm
:card: border-2
Our calculated $du$
^^^
```{math}
du= 3x^2 \cdot dx
```
---
Leftovers in the Integral
^^^
```{math}
3x^2\cdot dx
```
````

A perfect match! Usually, this does not have happen. Usually, we have to do a little bit of work with the differentials to make our calculated $du$ fit better with what is actually there in the integral. And that's what we're going to see in the next example.

## Example 5

Evaluate the integral.

$$
\int \sqrt{4x+5} \; dx
$$

```{dropdown} **Question:** What do <em>you</em> think we should pick for $u$ in this example?
**Answer:** Could we try $u=4x+5$?
```


````{tabbed} Solution
Click through the steps to see what we do.

If you want, give it a try first! 
````


````{tabbed} Step 0
The first thing we should do whenever we see a **root function** is to rewrite it as a power function
```{math}
\int \sqrt{4x+5} \; dx = \int (4x+5)^{1/2} \; dx
```

(This just helps us later on, if we have to use the power rule.)

````

````{tabbed} Step 1a
Choose $u$ by looking for the inner function:

```{math}
u=4x+5
```

And then calculate $du$:
```{math}
du=\big[4x+5\big]' dx \longrightarrow du = 4\cdot dx
```

````

`````{tabbed} Step 1b
Next, we need to compare:
````{panels}
:column: col-sm
:card: border-2
Our calculated $du$
^^^
```{math}
du= 4 \cdot dx
```
---
Leftovers in the Integral
^^^
```{math}
dx
```
````

And we see that they do not exactly match, there is an **extra constant** (that $4$) in what we calculated for $du$ that does not appear in the original integral.

How do we handle this? Well, we need to solve our differential equation for what does appear in the integral, we need to solve for the $dx$. 

```{math}
du = 4\cdot dx \longrightarrow \tfrac{1}{4}\cdot du = dx
```

`````

````{tabbed} Step 2
Now we're ready to substitute our $u$ and $\frac{1}{4}du$ into the original integral:

```{math}
\int (4x+5)^{1/2} \; dx = \int u^{1/2} \cdot \frac{1}{4}\; du
```

````

````{tabbed} Step 3
And this gives us one of our basic integrals, where we can just apply the power rule:

```{math}
\frac{1}{4} \cdot \int u^{1/2} \; du = \dfrac{1}{4}\cdot \left(\dfrac{2}{3}\cdot u^{3/2}\right) +C
```

````

````{tabbed} Step 4
And then finally we can simplify and convert all instances of $u$ back to our original variable $x$.


```{math} 
\dfrac{1}{6} u^{3/2} +C = \dfrac{1}{6} (4x+5)^{3/2} +C
```
````


## Example 6

Evaluate the integral.

$$
\int x^2\sin\left(x^3+5\right) \; dx
$$

```{dropdown} **Question:** What do <em>you</em> think we should pick for $u$ in this example?
**Answer:** How about $u=x^3+5$?
```


````{tabbed} Solution
Click through the steps to see what we do.

If you want, give it a try first! 
````



````{tabbed} Step 1a
Since the more complicated piece of our function is $\sin\left(x^3+5\right)$, we choose $u$ to be the inner function:

```{math}
u=x^3+5
```

And then calculate $du$
```{math}
du=\big[x^3+5\big]' dx \longrightarrow du = 3x^2\cdot dx
```

````

`````{tabbed} Step 1b
Next, we need to compare:
````{panels}
:column: col-sm
:card: border-2
Our calculated $du$
^^^
```{math}
du= 3x^2 \cdot dx
```
---
Leftovers in the Integral
^^^
```{math}
x^2 \cdot dx
```
````

And we see that they do not exactly match, there is an **extra constant** (that $3$) in what we calculated for $du$ that does not appear in the original integral.

Again, we need to solve for what does appear in the integral, we need to solve for the $x^2\cdot dx$. 

```{math}
du = 3x^2 \cdot dx \longrightarrow \tfrac{1}{3}\cdot du = x^2 dx
```

`````



````{tabbed} Step 2
Now we're ready to substitute our $u$ and $\frac{1}{3}du$ into the original integral:

```{math}
\int x^2\sin\left(x^3+5\right) \; dx = \int \sin u \cdot \frac{1}{3}\; du
```

````

````{tabbed} Step 3
This gives us one of our basic integrals, which we can just do:

```{math}
\frac{1}{3} \cdot \int \sin u \; du  = \dfrac{1}{3} \cdot \left(-\cos u\right) +C
```

````

````{tabbed} Step 4
And then finally we convert back to $x$.


```{math} 
-\dfrac{1}{3}\cos u +C = -\dfrac{1}{3}\cos \left(x^3+5\right) +C 
```
````


## Example 7

Evaluate the integral.

$$
\int \dfrac{2-x}{\sqrt{2x^2-8x+1}} \; dx
$$

```{dropdown} **Question:** What do <em>you</em> think we should pick for $u$ in this example?
**Answer:** Maybe $u=2x^2-8x+1$?
```


````{tabbed} Solution
Click through the steps to see what we do.

If you want, give it a try first! 
````


````{tabbed} Step 0
We start by rewriting this **root function** as a power function
```{math}
\int \dfrac{2-x}{\sqrt{2x^2-8x+1}} \; dx = \int (2x^2-8x+1)^{-1/2} (2-x)\; dx
```


(This just helps us later on, if we have to use the power rule.)

````

````{tabbed} Step 1a
Since the more complicated piece of our function is $(2x^2-8x+1)^{-1/2}$, we choose $u$ to be the inner function:

```{math}
u=2x^2-8x+1
```

And then calculate $du$
```{math}
du=\big[2x^2-8x+1\big]' dx \longrightarrow du = (4x-8)\cdot dx
```

````

`````{tabbed} Step 1b
Next, we need to compare:
````{panels}
:column: col-sm
:card: border-2
Our calculated $du$
^^^
```{math}
du = (4x-8)\cdot dx
```
---
Leftovers in the Integral
^^^
```{math}
(2-x) \cdot dx
```
````

And we see that they do not exactly match, but if we do some **factoring** we can get them to almost match, except for a constant.


````{panels}
:column: col-sm
:card: border-2
Our calculated $du$
^^^
```{math}
du = -4\cdot (2-x)\cdot dx
```
---
Leftovers in the Integral
^^^
```{math}
(2-x) \cdot dx
```
````

And since the $(2-x)\cdot dx$ shows up in both of these, this is what we solve for:

```{math}
du = -4\cdot (2-x)\cdot dx \longrightarrow \tfrac{-1}{4}\cdot du = (2-x) \cdot dx
```

`````


````{tabbed} Step 2
Now we're ready to substitute our $u$ and $\frac{-1}{4}du$ into the original integral:

```{math}
\int (2x^2-8x+1)^{-1/2} (2-x)\; dx = \int u^{-1/2} \cdot \frac{-1}{4}\; du
```

````

````{tabbed} Step 3
This gives us one of our basic integrals, which can be solved by using power rule:

```{math}
\frac{-1}{4} \cdot \int u^{-1/2}  \; du = \dfrac{-1}{4} \cdot  \left(2u^{1/2}\right)  +C
```

````

````{tabbed} Step 4
And then we get back to $x$.


```{math} 
\dfrac{-1}{2}u^{1/2} +C = \dfrac{-1}{2}(2x^2-8x+1)^{1/2} +C 
```
````

## Solving for x

Sometimes after making as many subsitutions with $u$ and $du$ as possible, there are still some pesky $x$ terms that stick around. How can we get of rid of them? 

````{admonition} Strategy
One strategy to try is to solve our $u=g(x)$ equation for $x$.
````


As a quick example, let's suppose we were working on an integral and after choosing $u=5+x$ were able to get to this point in our substitution:

$$
\int u^{1/2}\cdot x \; du
$$

Now, we can't go any further yet because of that remaining $x$-term. **Remember we need to convert everything from $x$ to $u$, before going on with the  integration.**

But if we solve for $x$ ...

$$
u=5+x \longrightarrow x =u-5
$$

We see that we can replace that leftover $x$ with $5-u$ instead:


$$
\int u^{1/2}\cdot(u-5) \; du
$$

And now we're ready to keep going!




## Example 8


Evaluate the integral.

$$
\int x^3\sqrt{1+x^2} \; dx
$$

```{dropdown} **Question:** What do <em>you</em> think we should pick for $u$ in this example?
**Answer:** Maybe give $u=1+x^2$ a try?
```


````{tabbed} Solution
Click through the steps to see what we do.

If you want, give it a try first! 
````


````{tabbed} Step 0
We start by rewriting this **root function** as a power function
```{math}
\int x^3\sqrt{1+x^2} \; dx= \int (1+x^2)^{1/2}\cdot x^3 \; dx
```


(This just helps us later on, if we have to use the power rule.)

````

````{tabbed} Step 1a
Since the more complicated piece of our function is $(1+x^2)^{1/2}$, we choose $u$ to be the inner function:

```{math}
u=1+x^2
```

And then calculate $du$
```{math}
du=\big[1+x^2\big]' dx \longrightarrow du = 2x\cdot dx
```

````

`````{tabbed} Step 1b
Next, we need to compare:
````{panels}
:column: col-sm
:card: border-2
Our calculated $du$
^^^
```{math}
du = 2x\cdot dx
```
---
Leftovers in the Integral
^^^
```{math}
x^3 \cdot dx
```
````

We're sort of looking for the greatest common factor between the two of these. Both have an $x$ on the right and both have a $dx$, so this is what we try to produce:



````{panels}
:column: col-sm
:card: border-2
Our calculated $du$
^^^
```{math}
\tfrac{1}{2}\cdot du = x\cdot dx
```
---
Leftovers in the Integral
^^^
```{math}
x^2 \cdot x \cdot dx
```
````

`````


````{tabbed} Step 2
Now we're ready to substitute our $u$ and $\frac{1}{2}du$ into the original integral:

```{math}
\int (1+x^2)^{1/2}\cdot x^2 \cdot x \; dx= \int u^{1/2} \cdot x^2\cdot \frac{1}{2}\; du
```

But... we can't go any further yet since we still have some $x$-terms that we haven't gotten rid of yet. So we turn to our "solve for $x$ strategy."



$$
u=1+x^2 \longrightarrow x^2 =u-1
$$

And this is actually as far as we need to solve, since an $x^2$ is what we have remaining.

```{math}
\int u^{1/2} \cdot x^2\cdot \frac{1}{2}\; du = \int u^{1/2} \cdot (u-1)\cdot \frac{1}{2}\; du
```

````

````{tabbed} Step 3
This gives us a basic integral, which can be solved by multiplying out the integrand and then using power rule:

```{math}
\begin{split}
\dfrac{1}{2} \cdot \int u^{1/2} \cdot (u-1)\; du &= \dfrac{1}{2} \cdot \int u^{3/2}-u^{1/2} \; du \\
& = \dfrac{1}{2}\cdot \left( \dfrac{2}{5}u^{5/2}-\dfrac{2}{3}u^{3/2}\right) +C
\end{split}
```

````

````{tabbed} Step 4
And then we get back to $x$.


```{math} 
 \dfrac{1}{5}u^{5/2}-\dfrac{1}{3}u^{3/2} +C = \dfrac{1}{5}(1+x^2)^{5/2}-\dfrac{1}{3}(1+x^2)^{3/2} +C  
```
````
