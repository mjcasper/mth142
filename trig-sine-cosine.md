# Trigonometric Integrals Involving Powers of Sine and Cosine

In this lesson we are going to see how to calculate integrals of the form:

$$
\int \sin^m x \cos^n x \, dx
$$


## Odd Powers

If one (or both) of the $\sin x$ or $\cos x$ terms has an **odd power** then we:

1. Factor off one trig term from this odd power and put it next to the $dx$.
2. Convert all remaining terms to the opposite trig function.
3. Set $u$ equal to the opposite trig function.
4. Finish integrating using Substitution Rule.


````{admonition} Trigonometric Identity
```{math}
\sin^2 \theta +\cos^2 \theta =1
```
````






## Example 1
Integrate the following:

$$
\int \cos^3 x \, dx
$$

``````{dropdown} Solution (Click to see the steps.)

````{tabbed} Step 1
**Separate:** We see that cosine has the odd power, so we begin by separating off one of these cosine factors:
```{math}
\int \cos^3 x \, dx = \int \cos^2 x \cdot \cos x\, dx
```

````

````{tabbed} Step 2
**Convert:** Next, we convert all remaining terms to the opposite trig function. In this case we convert all remaining cosine terms into sine terms.
```{math}
\int \cos^2 x \cdot \cos x\, dx = \int \left(1-\sin^2 x\right) \cdot \cos x\, dx 
```
This is where we use the trig identity: $\sin^2 \theta +\cos^2 \theta =1$
````

`````{tabbed} Step 3
**Choose u:** Now we're ready for a $u$-substitution, so we choose $u$ to be the opposite trig function. In this case we choose: 
```{math}
 u=\sin x
```
and then we calculate $du$ to get:
```{math}
 du = \cos x \, dx
```

And then substituting our $u$ and $du$ into the integral gives us:
```{math}
\int \left(1-\sin^2 x\right) \cdot \cos x\, dx = \int \left(1-u^2 \right) \, du
```


`````

````{tabbed} Step 4
**Finish It!** And finally we finish the integration:

```{math}
\int \left(1-u^2 \right) \, du &= u-\tfrac{1}{3}u^3+C \\
&= \sin x-\tfrac{1}{3}(\sin x)^3+C \\
```
(Don't forget $+C$ for indefinite integrals!)
````
``````



---


## Example 2
Integrate the following:

$$
\int \sin x \cos x \, dx
$$


``````{dropdown} Solution (Click to see the steps.)

````{tabbed} Step 1
**Separate:** We see that cosine has an odd power, so we begin by separating off one of these cosine factors:
```{math}
\int \sin x \cos x \, dx= \int \sin x \cdot \cos x\, dx
```

````

````{tabbed} Step 2
**Convert:** Next, we would need to convert any remaining cosine terms into sine terms (besides that one copy of $\cos x$ we moved next to the $dx$). But our integral is already in this form!
```{math}
\int \sin x \cdot \cos x\, dx
```

 So we're all set with this step.

````

`````{tabbed} Step 3
**Choose u:** Now we're ready for a $u$-substitution, so we choose $u$ to be the opposite trig function. In this case we choose: 
```{math}
 u=\sin x
```
and then we calculate $du$ to get:
```{math}
 du = \cos x \, dx
```

And then substituting our $u$ and $du$ into the integral gives us:
```{math}
\int \sin x \cdot \cos x\, dx = \int u \, du
```


`````

````{tabbed} Step 4
**Finish It!** And finally we finish the integration:

```{math}
\int u \, du &= \tfrac{1}{2}u^2+C \\
&= \tfrac{1}{2}(\sin x)^2+C \\
```
(Don't forget $+C$ for indefinite integrals!)
````
``````


## Example 3
Integrate the following:

$$
\int \sin^5 x \cos^2 x \, dx
$$

``````{dropdown} Solution (Click to see the steps.)

````{tabbed} Step 1
**Separate:** We see that sine has an odd power, so we begin by separating off one of these sine factors:
```{math}
\int \sin^5 x \cos^2 x \, dx= \int \sin^4 x \cdot \cos^2 x\cdot \sin x \, dx
```
and we move it next to the $dx$.

````

````{tabbed} Step 2
**Convert:** Next, we need to convert those remaining sine terms into cosine terms (besides that one copy of $\sin x$ we moved next to the $dx$). 
```{math}
\int \sin^4 x \cdot \cos^2 x\cdot \sin x \, dx
```

This is where we use the trig identity: $\sin^2 \theta +\cos^2 \theta =1$

```{math}
& = \int \sin^2 x\cdot \sin^2 x \cdot \cos^2 x\cdot \sin x \, dx \\
&= \int \left(1-\cos^2 x\right)\cdot \left(1-\cos^2 x\right)  \cdot \cos^2 x\cdot \sin x \, dx 
```
````

`````{tabbed} Step 3
**Choose u:** Now we're ready for a $u$-substitution, so we choose $u$ to be the opposite trig function. In this case we choose: 
```{math}
 u=\cos x
```
and then we calculate $du$ to get:
```{math}
 du = -\sin x \, dx \longrightarrow (-1)du= \sin x \, dx
```

And then substituting our $u$ and $(-1)du$ into the integral gives us:
```{math}
&= \int \left(1-\cos^2 x\right)\cdot \left(1-\cos^2 x\right)  \cdot \cos^2 x\cdot \sin x \, dx \\
&= \int \left(1-u^2\right)\cdot \left(1-u^2\right)  \cdot u^2 \cdot (-1) du
```


`````

````{tabbed} Step 4
**Finish It!** In order to finish the integration we first need to multiply everything out:

```{math}
&= \int \left(1-u^2\right)\cdot \left(1-u^2\right)  \cdot u^2 \, (-1) du\\
&= \int \left(1-2u^2+u^4\right) \cdot u^2 \, (-1) du\\
&= \int \left(u^2-2u^4+u^6\right)  \, (-1) du\\
&= \int \left(-u^2+2u^4-u^6\right)  \,  du
```
And finally we can find the antiderivative:
```{math}
&= -\tfrac{1}{3}u^3+\tfrac{2}{5}u^5-\tfrac{1}{7}u^7 +C\\
&= -\tfrac{1}{3}\cos^3 x+\tfrac{2}{5}\cos^5 x-\tfrac{1}{7}\cos^7 x +C

```

(Don't forget $+C$ for indefinite integrals!)
````
``````
