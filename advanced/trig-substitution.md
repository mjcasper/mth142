# (AI-1 and AI-2) Trigonometric Substitutions

In this lesson we are going to see how to use a trigonometric substitution to convert an integral involving a square root function into a trig integral (powers of trig functions).






## Trig Substitutions

We identify which trigonometric substitution to use, based on the square root term that shows up in our integral. There are generally three cases we consider:

| Square Root Term | Choice for $x$ | Differential $dx$ | Simplified $\sqrt{\cdots}$ |
|------------------|-----|------|----------------|
| $\sqrt{a^2-x^2}$ | $x=a\sin\theta$ | $dx = a \cos \theta \, d\theta$ | $\sqrt{a^2-x^2}=a\cos\theta$ |
| $\sqrt{a^2+x^2}$ | $x=a\tan\theta$ | $dx = a \sec^2 \theta \, d\theta$ | $\sqrt{a^2+x^2}=a\sec\theta$ |
| $\sqrt{x^2-a^2}$ | $x=a\sec\theta$ | $dx = a \sec \theta \tan \theta \, d\theta$ | $\sqrt{x^2-a^2}=a\tan\theta$ |


## The Process
1. Identify the necessary  trig substitution for $x$.
2. Calculate the pieces: $dx$ and $\sqrt{\cdots}$
3. Substitute all of these pieces into the integral.
4. Calculate the resulting trigonometric integral.
5. Convert the antiderivative back to $x$.


### How do we find a?
For expressions like $\sqrt{x^2-9}$, we look for the constant term under the square root (just the postive part). The value for $a$ is just the positive square root of this constant. For instance with $\sqrt{x^2-9}$, we would let $a=\sqrt{9}=3$.






### Converting Back

In many of our examples, we will be using a right triangle to help us convert back to our original variable. We can write the value of our trig functions in terms of the sides of the triangle. We will use:

- **opp** to denote the side opposite angle $\theta$
- **adj** to denote the side adjacent to angle $\theta$
- **hyp** to denote the side opposite the right angle


![triangle](../images/triangle-ai1.png)

With this we can write:

````{panels}
:column: col-4
```{math}
\sin \theta = \dfrac{opp}{hyp}
```
---
```{math}
\cos \theta = \dfrac{adj}{hyp}
```
---
```{math}
\tan \theta = \dfrac{opp}{adj}
```
````
And then we can use the definitions of the other trig functions to find similar expressions for them:
````{panels}
:column: col-4
```{math}
\csc \theta = \dfrac{1}{\sin\theta}
```
---
```{math}
\sec \theta = \dfrac{1}{\cos \theta}
```
---
```{math}
\cot \theta = \dfrac{1}{\tan \theta}
```
````



## Example 1
Integrate the following:

$$
\int \dfrac{1}{\sqrt{x^2-9}} \, dx 
$$


``````{dropdown} Solution (Click to see the steps.)

````{tabbed} Step 1
**Identify All Pieces** We start by looking at our square root term to help us identify our choice for $x$.

```{math}
\sqrt{x^2-9}=\sqrt{x^2-3^2}
```

We see that it is of the form $\sqrt{x^2-a^2}$. So we choose: $x=3\sec \theta$. 

Note that $a=3$, since $\sqrt{9}=3$

````

````{tabbed} Step 2
**Calculate All Pieces:** We have $x=3\sec \theta$, which means:

```{math}
x&=3\sec\theta\\
dx&=3\sec\theta \tan \theta \, d\theta\\
\sqrt{9-x^2}&=3\tan \theta
```

Plugging all of this into the integral gives us:

```{math}
\int \dfrac{1}{\sqrt{x^2-9}} \, dx   =\int \dfrac{1}{3\tan \theta}\cdot 3 \sec\theta \tan\theta  \, d\theta 
```
````

`````{tabbed} Step 3
**Trig Integral:** Now we can simplify the resulting trig integral and integrate using all of our trig integral techniques:

```{math}
 &= \int \dfrac{1}{3\tan \theta}\cdot 3 \sec\theta \tan\theta  \, d\theta  \\
 &= \int {\sec\theta} \, d\theta \\
```

And this is an integral we should just remember:

```{math}
 &= \ln \left|\sec\theta + \tan \theta \right|+C\\

```




`````

`````{tabbed} Step 4
**Convert Back:** Now we need to convert back to our original variable $x$. At this point we have:
```{math}
 &= \ln \left|\sec\theta + \tan \theta \right|+C\\

```
We need to convert both that $\sec \theta$ term and the $\tan \theta$ term, and we can do this using our original pieces:


````{panels}
```{math}
x=3\sec\theta
```
---
```{math}
\sqrt{x^2-9}=3\tan\theta 
```
````
Solving each gives us:

```{math}
x&=3\sec\theta \quad &\longrightarrow &\sec\theta =\dfrac{x}{3}\\
\sqrt{x^2-9}&=3\tan\theta  \quad &\longrightarrow &\tan\theta =\dfrac{\sqrt{x^2-9}}{3}\\
```

And finally plugging these into our antiderivative gives us the answer:
```{math}
 &= \ln \left|\sec\theta + \tan \theta \right|+C\\
 &= \ln \left|\tfrac{x}{3} + \tfrac{\sqrt{x^2-9}}{3} \right|+C\\
```
``````






<!--
    - Integrating Powers of Sine and Cosine
    - Integrating Powers of Secant and Tangent


### Calculate all pieces

It is really important to remember to convert differentials correctly by calculating the differential $dx$. **This is the most common mistake



## Example 2
Integrate the following:

$$
\int \dfrac{x^2}{\sqrt{4-x^2}} \, dx 
$$


``````{dropdown} Solution (Click to see the steps.)

````{tabbed} Step 1
**Identify All Pieces** We start by looking at our square root term to help us identify our choice for $x$.

```{math}
\sqrt{4-x^2}=\sqrt{2^2-x^2}
```

We see that it is of the form $\sqrt{a^2-x^2}$. So we choose: $x=2\sin \theta$. 

Note that $a=2$, since $\sqrt{4}=2$

````

````{tabbed} Step 2
**Calculate All Pieces:** We have $x=2\sin \theta$, which means:

```{math}
x&=2\sin\theta\\
dx&=2\cos\theta d\theta\\
\sqrt{4-x^2}&=2\cos \theta
```

Plugging all of this into the integral gives us:

```{math}
\int \dfrac{x^2}{\sqrt{4-x^2}} \, dx  = \int \dfrac{\left(2\sin\theta\right)^2}{2\cos \theta} \cdot 2 \cos \theta \, d\theta 
```
````

`````{tabbed} Step 3
**Trig Integral:** Now we can simplify the resulting trig integral and integrate using all of our trig integral techniques:

```{math}
 &= \int \dfrac{\left(2\sin\theta\right)^2}{2\cos \theta} \cdot 2 \cos \theta \, d\theta \\
 &= \int {4\sin^2\theta} \, d\theta \\
```

This is an **even power** of sine, so we use our half-angle trig identities to reduce the exponent:

```{math}
 &= \int 4\cdot\bigg(\tfrac{1}{2}-\tfrac{1}{2} \cos 2\theta\bigg)  \, d\theta \\
 &= \int \cdot\bigg(2-2 \cos 2\theta\bigg)  \, d\theta \\
 &= 2\theta-2\cdot \tfrac{1}{2} \sin 2\theta +C \\
 &= 2\theta- \sin 2\theta +C \\
```

We were able to integrate using our $k$-form integrals.


`````

````{tabbed} Step 4
**Convert Back:** Now we need to convert back to our original variable $x$. 

Let's start:



---
**Finish It!** And finally we finish the integration. First multiply everything out so that we have only power functions to integrate.

```{math}
&= \int u^6 \left(1+u^2\right) \, du\\
&= \int \left(u^6+u^8\right)  \, du\\
&= \tfrac{1}{7}u^{7}+\tfrac{1}{9}u^9+C\\
```
And then convert back to $x$ to get our answer:
```{math}
&= \tfrac{1}{7}\tan^{7}x+\tfrac{1}{9}\tan^9x+C\\
```
(Don't forget $+C$ for indefinite integrals!)
````
``````

-->