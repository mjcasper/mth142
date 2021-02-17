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

## U-Substitution?

Even if we see a square root term in our integral, we don't always need to use a trig substitution. Let's compare the following two integrals:

````{panels}
Substitution Rule
^^^
```{math}
\int \dfrac{x}{\sqrt{x^2-9}}\, dx
```

---

Trig Substitution
^^^
```{math}
\int \dfrac{1}{\sqrt{x^2-9}}\, dx
```
````

The obvious choice for $u$ in each of these is $u=x^2-9$. However, when we calculate $du$, we see that we can only make the differentials match in the first integral. This is because if $u=x^2-9$ then,

```{math}
du= 2x \, dx
```

The first integral has an $x\, dx$, but our second integral only has the $dx$.


## General Trig Sub

Occasionally, we come across integrals involving square root terms of the form:


````{panels}
:column: col-4
```{math}
\sqrt{a^2-b^2x^2}
```
---
```{math}
\sqrt{a^2+b^2x^2}
```
---
```{math}
\sqrt{b^2x^2-a^2}
```
````
In which case we would use:
````{panels}
:column: col-4
```{math}
x = \tfrac{a}{b}\sin \theta
```
---
```{math}
x = \tfrac{a}{b}\tan \theta
```
---
```{math}
x = \tfrac{a}{b}\sec \theta
```
````

## Example 5
Use a trigonometric substitution to rewrite this integral as a trig integral. 

$$
\int \dfrac{1}{(9x^2-25)^{3/2}}\;dx
$$

``````{dropdown} Solution (Click to see the steps.)

````{tabbed} Step 1
**Identify Trig Sub:** It may be helpful to rewrite this integral with an explicit square root:


```{math}
\int \dfrac{1}{(9x^2-25)^{3/2}}\;dx &= \int \dfrac{1}{\left((9x^2-25)^{1/2}\right)^3}\;dx\\[10pt]
&= \int \dfrac{1}{\left(\sqrt{9x^2-25}\right)^3}\;dx\\
```
From here, we can see that it is in the form $\sqrt{b^2x^2-a^2}$ so we choose $x=\tfrac{a}{b}\sec\theta$.

Note that:
- $a=5$, since $\sqrt{25}=5$
- $b=3$, since $\sqrt{9}=3$

This means we choose: $x=\tfrac{5}{3}\sec\theta$.

````



````{tabbed} Step 2
**Calculate All Pieces:** We have $x=\tfrac{5}{3}\sec\theta$, which means:

```{math}
x&=\tfrac{5}{3}\sec\theta\\
dx&=\tfrac{5}{3}\sec\theta\tan\theta \, d\theta\\
\sqrt{9x^2-25}&=5\tan\theta
```

Let's check that square root simplication:

```{math}
\sqrt{9x^2-25}&= \sqrt{9 \left(\tfrac{5}{3}\sec\theta \right)^2-25}\\[10pt]
&= \sqrt{9 \left(\tfrac{25}{9}\sec^2\theta \right)-25}\\[10pt]
&= \sqrt{25\sec^2\theta -25}\\[10pt]
&= \sqrt{25\left(\sec^2\theta -1\right)}\\[10pt]
&= \sqrt{25\tan^2\theta}\\[10pt]
&= 5\tan\theta\\[10pt]
```
````

`````{tabbed} Step 3
**Trig Integral:** Now we have all our pieces:

```{math}
x&=\tfrac{5}{3}\sec\theta\\
dx&=\tfrac{5}{3}\sec\theta\tan\theta \, d\theta\\
\sqrt{9x^2-25}&=5\tan\theta
```
So let's plug everything into our integral:-

```{math}
&= \int \dfrac{1}{\left(\sqrt{9x^2-25}\right)^3}\;dx\\[10pt]
&= \int \dfrac{1}{\left(5\tan \theta\right)^3}\cdot\tfrac{5}{3}\sec\theta\tan\theta \, d\theta\\[10pt]
&= \int \dfrac{1}{\left(5\tan \theta\right)^2}\cdot\tfrac{1}{3}\sec\theta \, d\theta\\[10pt]
&= \dfrac{1}{75}\int \dfrac{\sec\theta}{\tan^2 \theta} \, d\theta\\
```



`````

``````

## Example 6

Integrate the following:

$$
\int_{-1}^{0} \dfrac{x}{\sqrt{3-2x-x^2}} \, dx 
$$


``````{dropdown} Solution (Click to see the steps.)

````{tabbed} Step 0
Looking at this integral, we see that the function is not explicitly in the correct format for a trig substitution. So to get started, we're going to first:
- complete the square for that term under the square root
- apply a $u$-substitution

Once we do all of this, we'll have an integral in the correct format for a trig substitution. 

**Completing the Square:** 

Factor off any constants, so that our first term is an $x^2$

```{math}
3-2x-x^2 &= -\left( x^2+2x \qquad -3\right)\\
```
We've intentially left a space in between the $2x$ and the $-3$. Because we're going to take the constant in front of the $x$, divide whatever it is by $2$, square that result and then add in fancy 0. 

So in this case specifically we're going to take the $2$ from the $2x$ and:

```{math}
2 \quad \longrightarrow \quad \dfrac{2}{2}=1 \quad \longrightarrow \quad 1^2=1 \quad \longrightarrow \quad +1 -1
```

And that $+1-1$ is what we're going to put in that extra space:

```{math}
3-2x-x^2 &= -\left( x^2+2x \qquad -3\right)\\[5pt]
&= -\left( x^2+2x +1 -1 -3\right)\\[5pt]
&= -\left( (x^2+2x +1) + (-1 -3)\right)\\[5pt]
&= -\left( (x+1)^2 -4\right)\\[5pt]
&= 4- (x+1)^2 \\
```

Let's rewrite our function using this, to see where we're at:

```{math}
\int_{-1}^{0} \dfrac{x}{\sqrt{3-2x-x^2}} \, dx  &= \int_{-1}^{0} \dfrac{x}{\sqrt{4- (x+1)^2}} \, dx \\
```

**U-Substitution:** It's looking better, but finally to get our usual trig substitution form we need to do a $u$-substitution with:

```{math}
u &= x+1 \quad \longrightarrow \quad x=u-1\\
du &= dx
```

And converting the limits of integration:

```{math}
x = 0 &\quad \longrightarrow \quad u=1\\
x = -1 &\quad \longrightarrow \quad u=0
```

Putting all of this together gives us:

```{math}
&= \int_{-1}^{0} \dfrac{x}{\sqrt{4- (x+1)^2}} \, dx \\
&= \int_{0}^{1} \dfrac{u-1}{\sqrt{4- u^2}} \, du \\
```

And there we go, that's our usual $\sqrt{a^2-u^2}$ form!

````


````{tabbed} Step 1
Now it comes down to calculating:

```{math}
&= \int_{0}^{1} \dfrac{u-1}{\sqrt{4- u^2}} \, du \\
```


**Identify Trig Sub:** We start by looking at our square root term to help us identify our choice for $u$.

```{math}
\sqrt{4-u^2}=\sqrt{2^2-u^2}
```

We see that it is of the form $\sqrt{a^2-u^2}$. So we choose: $u=2\sin \theta$. 

Note that $a=2$, since $\sqrt{4}=2$

````

````{tabbed} Step 2
**Calculate All Pieces:** We have $u=2\sin \theta$, which means:

```{math}
u&=2\sin\theta\\
du&=2\cos\theta d\theta\\
\sqrt{4-u^2}&=2\cos \theta
```

Plugging all of this into the integral gives us:

```{math}
\int_{0}^{1} \dfrac{u-1}{\sqrt{4- u^2}} \, du  = \int_{u=0}^{u=1} \dfrac{2\sin\theta-1}{2\cos \theta}   \cdot 2 \cos \theta \, d\theta 
```
````

`````{tabbed} Step 3
**Trig Integral:** Now we can simplify the resulting trig integral and integrate using all of our trig integral techniques:

```{math}
 &= \int_{u=0}^{u=1} \dfrac{2\sin\theta-1}{2\cos \theta}   \cdot 2 \cos \theta \, d\theta  \\[10pt]
 &= \int_{u=0}^{u=1} \left(2\sin\theta-1\right) \, d\theta  \\
```

We can just do the integration here to get:

```{math}
 &= -2\cos\theta-\theta \biggr|_{u=0}^{u=1}  \\
```



`````

`````{tabbed} Step 4
So far we have:
```{math}
 &= -2\cos\theta-\theta \biggr|_{u=0}^{u=1}  \\
```


**Convert Back:** At this point we need to convert back to $u$, so let's start with the pieces we calculated: 
```{math}
u&=2\sin\theta\\
du&=2\cos\theta \, d\theta\\
\sqrt{4-u^2}&=2\cos \theta
```
From these pieces we see: $\cos \theta = \sqrt{4-u^2}$, so we'll be able to use that.

We then use our choice of $u$ to solve for $\theta$:
```{math}
u=2\sin\theta \hspace{0.5em} \longrightarrow \hspace{0.5em} \sin\theta = \tfrac{u}{2 }\hspace{0.5em} \longrightarrow \hspace{0.5em}\theta = \sin^{-1}\left(\tfrac{u}{2}\right)

```

Putting this all together gives us:
```{math}
 &= -2\cos\theta-\theta \biggr|_{u=0}^{u=1}  \\[10pt]
 &= -\sqrt{4-u^2}-\sin^{-1}\left(\tfrac{u}{2}\right) \biggr|_{u=0}^{u=1}  \\[10pt]
 &= \bigg(-\sqrt{3}-\sin^{-1}\left(\tfrac{1}{2}\right)\bigg)- \bigg( -\sqrt{4}-\sin^{-1}\left(\tfrac{0}{2}\right)  \bigg) \\[10pt]
  &= \bigg(-\sqrt{3}-\frac{\pi}{6}\bigg)- \bigg( -\sqrt{4}-0  \bigg) \\[10pt]
  &= 2-\sqrt{3}-\frac{\pi}{6} 
```
``````
