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
**Identify Trig Sub:** We start by looking at our square root term to help us identify our choice for $x$.

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
x&=3\sec\theta \quad &\longrightarrow \quad&\sec\theta =\dfrac{x}{3}\\
\sqrt{x^2-9}&=3\tan\theta  \quad &\longrightarrow \quad&\tan\theta =\dfrac{\sqrt{x^2-9}}{3}\\
```

And finally plugging these into our antiderivative gives us the answer:
```{math}
 &= \ln \left|\sec\theta + \tan \theta \right|+C\\[10pt]
 &= \ln \left|\dfrac{x}{3} + \dfrac{\sqrt{x^2-9}}{3} \right|+C\\
```
``````



## Example 2
Integrate the following:

$$
\int \dfrac{\sqrt{25-x^2}}{x^2} \, dx 
$$


``````{dropdown} Solution (Click to see the steps.)

````{tabbed} Step 1
**Identify Trig Sub:** We start by looking at our square root term to help us identify our choice for $x$.

```{math}
\sqrt{25-x^2}=\sqrt{5^2-x^2}
```

We see that it is of the form $\sqrt{a^2-x^2}$. So we choose: $x=5\sin \theta$. 

Note that $a=5$, since $\sqrt{25}=5$

````

````{tabbed} Step 2
**Calculate All Pieces:** We have $x=5\sin \theta$, which means:

```{math}
x&=5\sin\theta\\
dx&=5\cos\theta \, d\theta\\
\sqrt{25-x^2}&=5\cos \theta
```

Plugging all of this into the integral gives us:

```{math}
\int \dfrac{\sqrt{25-x^2}}{x^2} \, dx   =\int \dfrac{5\cos \theta}{(5\sin \theta)^2}\cdot 5 \cos\theta   \, d\theta 
```
````

`````{tabbed} Step 3
**Trig Integral:** Now we can simplify the resulting trig integral and integrate using all of our trig integral techniques:

```{math}
 &= \int \dfrac{5\cos \theta}{(5\sin \theta)^2}\cdot 5 \cos\theta   \, d\theta  \\[10pt]
 &= \int \dfrac{5^2\cos^2\theta}{5^2\sin^2\theta} \, d\theta \\[10pt]
 &= \int \dfrac{\cos^2\theta}{\sin^2\theta} \, d\theta \\
```

Now if we use our $\sin^2\theta +\cos^2\theta =1$ trig identity in the numerator we get: 

```{math}
 &= \int \dfrac{1-\sin^2\theta}{\sin^2\theta} \, d\theta \\[10pt]
 &= \int \left(\dfrac{1}{\sin^2\theta}-\dfrac{\sin^2\theta}{\sin^2\theta} \right)\, d\theta \\[10pt]
 &= \int {\csc^2\theta}-1 \, d\theta \\[10pt]
```

And we get the antiderivative:

```{math}
 &=  -\cot\theta-\theta +C \\[10pt]
```



`````

`````{tabbed} Step 4
**Convert Back:** Now we need to convert back to our original variable $x$. So far at this point we have:
```{math}
 &=  -\cot\theta-\theta +C \\[10pt]

```
This means we need to convert both that $\cot \theta$ term and the single $\theta$ term. 

**Single $\theta$ term:** Whenever we have a lone $\theta$ value (not part of a trig function), we can use inverse trig functions to help us solve for $\theta$. Start with our original trig substitution, solve for $\sin\theta$, and then apply the appropriate inverse function:

```{math}
x&=5\sin\theta \\[10pt]
\dfrac{x}{5}&=\sin\theta \\[10pt]
\sin^{-1}\left(\tfrac{x}{5}\right)&=\theta \\

```

**Trig Terms:** Next we need to convert the $\cot \theta$ term by constructing our right triangle and finding the sides: $opp$, $adj$, and $hyp$ all in terms of $x$.

We start with our original trig substitution: $x=5\sin\theta$, solve for $\sin\theta$, and pair this up with what we know about $\sin \theta$.


````{panels}

```{math}
\dfrac{x}{5}=\sin\theta
```
---

```{math}
\sin\theta=\dfrac{opp}{hyp}
```

````
This tells us values for sides $opp$ and $hyp$ and then the remaining unknown side is just the original square root term (check this with the Pythagorean Theorem).

```{math}
opp&=x\\
hyp&=5\\
adj&=\sqrt{25-x^2}\\
```

Finally, we can determine the value for $\cot \theta$:
```{math}
\cot \theta = \dfrac{1}{\tan\theta}=\dfrac{adj}{opp}=\dfrac{\sqrt{25-x^2}}{x}
```

And finally plugging these into our antiderivative gives us the answer:
```{math}
 &=  -\cot\theta-\theta +C \\[10pt]
 &= -\dfrac{\sqrt{25-x^2}}{x}-\sin^{-1}\left(\dfrac{x}{5}\right)+C\\
```
``````


## Example 3
Integrate the following:

$$
\int \dfrac{1}{x^2\sqrt{4+x^2}} \, dx 
$$


``````{dropdown} Solution (Click to see the steps.)

````{tabbed} Step 1
**Identify Trig Sub:** We start by looking at our square root term to help us identify our choice for $x$.

```{math}
\sqrt{4+x^2}=\sqrt{2^2+x^2}
```

We see that it is of the form $\sqrt{a^2+x^2}$. So we choose: $x=2\tan \theta$. 

Note that $a=2$, since $\sqrt{4}=2$

````

````{tabbed} Step 2
**Calculate All Pieces:** We have $x=2\tan \theta$, which means:

```{math}
x&=2\tan\theta\\
dx&=2\sec^2\theta \, d\theta\\
\sqrt{4+x^2}&=2\sec \theta
```

Plugging all of this into the integral gives us:

```{math}
\int \dfrac{1}{x^2\sqrt{4+x^2}} \, dx   =\int \dfrac{1}{\left(2\tan\theta\right)^2\cdot2\sec\theta}\cdot 2 \sec^2\theta   \, d\theta 
```
````

`````{tabbed} Step 3
**Trig Integral:** Now we can simplify the resulting trig integral and integrate using all of our trig integral techniques:

```{math}
 &= \int \dfrac{1}{\left(2\tan\theta\right)^2\cdot2\sec\theta}\cdot 2 \sec^2\theta   \, d\theta  \\[10pt]
 &= \dfrac{1}{4} \int \dfrac{1}{\tan^2\theta} \cdot\sec\theta \, d\theta \\
```

From here we can rewrite everything in terms of sine and cosine: 

```{math}
&= \dfrac{1}{4} \int \dfrac{\cos^2\theta}{\sin^2\theta} \cdot\dfrac{1}{\cos\theta} \, d\theta \\[10pt]
&= \dfrac{1}{4} \int \dfrac{1}{\sin^2\theta} \cdot{\cos\theta} \, d\theta \\
```

We now have an **odd power** of cosine so we can go through our usual $u$-substitution:
```{math}
u&= \sin \theta\\
du&=\cos \theta\, d\theta
```

Plugging this in and finish integrating!

```{math}
= \dfrac{1}{4} \int \dfrac{1}{u^2}  \, du = -\dfrac{1}{4} \cdot \dfrac{1}{u}+C= -\dfrac{1}{4} \cdot \dfrac{1}{\sin \theta}+C
```



`````

`````{tabbed} Step 4
**Convert Back:** Now we need to convert back to our original variable $x$. So far at this point we have:
```{math}
= -\dfrac{1}{4} \cdot \dfrac{1}{\sin \theta}+C
```



**Trig Terms:** We need to convert that $1/\sin \theta$ term by constructing our right triangle and finding sides: $opp$, $adj$, and $hyp$ all in terms of $x$.

We start with our original trig substitution: $x=2\tan\theta$, solve for $\tan\theta$, and pair this up with what we know about $\tan\theta$.


````{panels}

```{math}
\dfrac{x}{2}=\tan\theta
```
---

```{math}
\tan\theta=\dfrac{opp}{adj}
```

````
This tells us values for sides $opp$ and $adj$ and then the remaining unknown side is just the original square root term (check this with the Pythagorean Theorem).

```{math}
opp&=x\\
hyp&=\sqrt{4+x^2}\\
adj&=2\\
```

Finally, we can determine the value for $1/\sin \theta$:
```{math}
\dfrac{1}{\sin \theta} = \dfrac{hyp}{opp}=\dfrac{\sqrt{4+x^2}}{x}
```

And then plugging these into our antiderivative gives us the answer:
```{math}
&= -\dfrac{1}{4} \cdot \dfrac{1}{\sin \theta}+C\\[10pt]
&= -\dfrac{1}{4} \cdot \dfrac{\sqrt{4+x^2}}{x}+C
```
``````


<!--
    - Integrating Powers of Sine and Cosine
    - Integrating Powers of Secant and Tangent


### Calculate all pieces

It is really important to remember to convert differentials correctly by calculating the differential $dx$. **This is the most common mistake

-->

## Example 4
Integrate the following:

$$
\int \dfrac{x^2}{\sqrt{4-x^2}} \, dx 
$$


``````{dropdown} Solution (Click to see the steps.)

````{tabbed} Step 1
**Identify Trig Sub:** We start by looking at our square root term to help us identify our choice for $x$.

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
 &= \int \dfrac{\left(2\sin\theta\right)^2}{2\cos \theta} \cdot 2 \cos \theta \, d\theta \\[10pt]
 &= \int {4\sin^2\theta} \, d\theta \\
```

This is an **even power** of sine, so we use our half-angle trig identities to reduce the exponent:

```{math}
 &= \int 4\cdot\bigg(\tfrac{1}{2}-\tfrac{1}{2} \cos 2\theta\bigg)  \, d\theta \\[10pt]
 &= \int \bigg(2-2 \cos 2\theta\bigg)  \, d\theta \\[10pt]
 &= 2\theta-2\cdot \tfrac{1}{2} \sin 2\theta +C \\[10pt]
 &= 2\theta- \sin 2\theta +C \\
```

We were able to integrate using our $k$-form integrals.


`````

`````{tabbed} Step 4
**Convert Back:** At this point we need to convert back to $x$, but before we do this we rewrite our $\sin 2\theta$ expression using a trig identity:
```{math}
 &= 2\theta- \sin 2\theta +C \\[10pt]
  &= 2\theta- 2\sin \theta \cos\theta +C \\[10pt]
```
This will make it easier to use a right triangle to find $\sin \theta \cos \theta$  instead of $\sin 2\theta$.


**Trig Terms:** Let's start converting the $\sin  \theta$ and  $\cos  \theta$ terms by first constructing our right triangle and finding the sides: $opp$, $adj$, and $hyp$ all in terms of $x$.

We start with our original trig substitution: $x=2\sin\theta$, solve for $\sin\theta$, and pair this up with what we know about $\sin \theta$.


````{panels}

```{math}
\dfrac{x}{2}=\sin\theta
```
---

```{math}
\sin\theta=\dfrac{opp}{hyp}
```

````
This tells us values for sides $opp$ and $hyp$ and then the remaining unknown side is just the original square root term (check this with the Pythagorean Theorem).

```{math}
opp&=x\\
hyp&=2\\
adj&=\sqrt{4-x^2}\\
```

We can then determine the value for $\cos \theta$:
```{math}
\cos \theta = \dfrac{adj}{hyp}=\dfrac{\sqrt{4-x^2}}{2}
```

**Single $2\theta$ term:** Just as we have seen before, whenever we have a lone $\theta$ value (not part of a trig function), we can use inverse trig functions to help us solve for $\theta$. Start with our original trig substitution, solve for $\sin\theta$, and then apply the appropriate inverse function:

```{math}
x&=2\sin\theta \\[10pt]
\dfrac{x}{2}&=\sin\theta \\[10pt]
\sin^{-1}\left(\tfrac{x}{2}\right)&=\theta \\

```

And finally plugging all of these pieces into our antiderivative gives us the answer:
```{math}
  &= 2\theta- 2\sin \theta \cos\theta +C \\[10pt]
  &= 2\sin^{-1}\left(\dfrac{x}{2}\right)- 2\cdot \dfrac{x}{2} \cdot \dfrac{\sqrt{4-x^2}}{2} +C \\[10pt]
  &= 2\sin^{-1}\left(\dfrac{x}{2}\right)- \tfrac{1}{2}\cdot x\sqrt{4-x^2} +C \\[10pt]
```
``````
