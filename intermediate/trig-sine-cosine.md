# (I-5) Trigonometric Integrals Involving Powers of Sine and Cosine

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


## Even Powers

If **both** of the $\sin x$ and $\cos x$ terms have an **even power** then we:

1. Break up our function into multiples of $\sin^2 x$ and $\cos^2 x$
2. Apply the half-angle identities.
3. Multiply all of the terms out.
4. Repeat the half-angle identities as needed. 


````{admonition} Half-Angle Identities
```{math}
\sin^2 \theta &=\tfrac{1}{2}(1-\cos 2\theta)\\
\cos^2 \theta &=\tfrac{1}{2}(1+\cos 2\theta)
```
````

It may also be helpful to occasionally use:

````{admonition} Yet Another Trig Identity
```{math}
\sin x \cos x =\tfrac{1}{2}\sin 2x
```
````

## K-form Integrals

We've mentioned these before, but it will be helpful to recall our K-form Integrals:

````{admonition} K-form Integrals

```{math}
&\int \sin(kx)\, dx = -\tfrac{1}{k}\cos(kx)+C\\
&\int \cos(kx)\, dx = \tfrac{1}{k}\sin(kx)+C
```
````


## Example 4
Integrate the following:

$$
\int_0^{\pi/2} \sin^2 x \, dx
$$

``````{dropdown} Solution (Click to see the steps.)

`````{tabbed} Step 1
**Half-Angle:** Our function is already written as a multiple of $\sin^2 x$, so we can start by applying our half-angle identity.
```{math}
\int_0^{\pi/2} \sin^2 x \, dx= \int_0^{\pi/2} \left(\tfrac{1}{2}-\tfrac{1}{2}\cos 2x \right)\, dx
```

````{admonition} Half-Angle Identity
```{math}
\sin^2 \theta =\tfrac{1}{2}(1-\cos 2\theta)=\tfrac{1}{2}-\tfrac{1}{2}\cos 2\theta
```
````

`````

`````{tabbed} Step 2
**Antiderivative:** We've reduced our even power of sine, down to one of our K-form integrals. So at this point we can find the antiderivative.
```{math}
\int_0^{\pi/2} \left(\tfrac{1}{2}-\tfrac{1}{2}\cos 2x \right)\, dx= \tfrac{1}{2}x-\tfrac{1}{2}\cdot \left(\tfrac{1}{2}\sin 2x\right) \biggr|_{x=0}^{x=\pi/2}
```

````{admonition} K-form Integral

```{math}
\int \cos(kx)\, dx = \tfrac{1}{k}\sin(kx)+C
```
````

`````

`````{tabbed} Step 3
**Evaluate:** Finally we can evaluate: 
```{math}
\tfrac{1}{2}x-\tfrac{1}{4}\sin 2x \biggr|_{x=0}^{x=\pi/2} = \biggr( \tfrac{1}{2}\cdot \tfrac{\pi}{2}-\tfrac{1}{4}\sin \pi \biggr) -\biggr( \tfrac{1}{2}\cdot 0-\tfrac{1}{4}\sin 0 \biggr)
```

And if we remember that $\sin \pi=0$ and $\sin 0 = 0$ we can simplify this down to get:

```{math}
\int_0^{\pi/2} \sin^2 x \, dx =\dfrac{\pi}{4}
```

`````


``````



---




## Example 5
Integrate the following:

$$
\int \sin^2 x \cos^2 x \, dx
$$

``````{dropdown} Solution (Click to see the steps.)

`````{tabbed} Step 1
**Half-Angle:** Our function is already written as a multiple of $\sin^2 x$ and $\cos^2 x$ terms, so we can start by applying our half-angle identities.
```{math}
\int \sin^2 x \cos^2 x \, dx&= \int \tfrac{1}{2}(1-\cos 2x)\cdot \tfrac{1}{2}(1+\cos 2x)\, dx \\
&= \tfrac{1}{4}\int (1-\cos 2x)\cdot (1+\cos 2x)\, dx 
```

````{admonition} Half-Angle Identities
```{math}
\sin^2 \theta &=\tfrac{1}{2}(1-\cos 2\theta)\\
\cos^2 \theta &=\tfrac{1}{2}(1+\cos 2\theta)
```
````

`````

`````{tabbed} Step 2
**Multiply:** In order to continue the integration, we need to multiply out the terms in our integral:
```{math}
\tfrac{1}{4}\int (1-\cos 2x)\cdot (1+\cos 2x)\, dx = \tfrac{1}{4}\int (1-\cos^2 2x)\, dx
```
It may help to remember FOIL when you do this:

```{math}
(1-\cos 2x)\cdot (1+\cos 2x) = 1+\cos 2x -\cos 2x- \cos^2 2x
```


`````

`````{tabbed} Step 3
**Half-Angle:** Doing the multiplication in the last step increased the exponent on our cosine term (back up to a square). So we need to use our half-angle identities again.
```{math}
\tfrac{1}{4}\int (1-\cos^2 2x)\, dx  &= \tfrac{1}{4}\int 1-\left(\tfrac{1}{2}+\tfrac{1}{2}\cos 2(2x)\right)\, dx\\
 &=\tfrac{1}{4}\int \left( \tfrac{1}{2}-\tfrac{1}{2}\cos 4x \right)\, dx\\
 &=\tfrac{1}{8}\int \left( 1-\cos 4x \right)\, dx
```

````{admonition} Half-Angle Identity
```{math}
\cos^2 \theta =\tfrac{1}{2}(1+\cos 2\theta)=\tfrac{1}{2}+\tfrac{1}{2}\cos 2\theta
```
````

`````



`````{tabbed} Step 4
**Antiderivative:** It took us a few tries, but at this point we've reduced our even powers of sine and cosine, down to one of our K-form integrals. So now we're ready to integrate:
```{math}
\tfrac{1}{8}\int \left( 1-\cos 4x \right)\, dx = \tfrac{1}{8}\left(x-\tfrac{1}{4}\sin 4x\right) + C
```

````{admonition} K-form Integral

```{math}
\int \cos(kx)\, dx = \tfrac{1}{k}\sin(kx)+C
```
````

`````




``````


## Example 6
Integrate the following:

$$
\int \sin^4 x  \, dx
$$

``````{dropdown} Solution (Click to see the steps.)


`````{tabbed} Step 1
**Break Up:** The first thing we need to do here is rewrite our function as multiples of $\sin^2 x$ and $\cos^2 x$ terms.
```{math}
\int \sin^4 x \, dx= \int \sin^2 x \sin^2 x \, dx
```

`````




`````{tabbed} Step 1
**Half-Angle:** Next we can apply our half-angle identities.
```{math}
\int \sin^2 x \sin^2 x \, dx&= \int \tfrac{1}{2}(1-\cos 2x)\cdot \tfrac{1}{2}(1-\cos 2x)\, dx \\
&= \tfrac{1}{4}\int (1-\cos 2x)\cdot (1-\cos 2x)\, dx 
```

````{admonition} Half-Angle Identities
```{math}
\sin^2 \theta &=\tfrac{1}{2}(1-\cos 2\theta)\\
\cos^2 \theta &=\tfrac{1}{2}(1+\cos 2\theta)
```
````

`````

`````{tabbed} Step 2
**Multiply:** In order to continue the integration, we need to multiply out the terms in our integral:
```{math}
&= \tfrac{1}{4}\int (1-\cos 2x)\cdot (1-\cos 2x)\, dx\\
& = \tfrac{1}{4}\int \bigg(1-2\cos 2x+\cos^2 2x\bigg)\, dx
```
It may help to remember FOIL when you do this:

```{math}
(1-\cos 2x)\cdot (1-\cos 2x) = 1-\cos 2x -\cos 2x+\cos^2 2x
```


`````

`````{tabbed} Step 3
**Half-Angle:** Doing the multiplication in the last step increased the exponent on our cosine term (back up to a square). So we need to use our half-angle identities again.
```{math}
& = \tfrac{1}{4}\int \bigg(1-2\cos 2x+\cos^2 2x\bigg)\, dx\\
& = \tfrac{1}{4}\int \bigg(1-2\cos 2x+\tfrac{1}{2}+\tfrac{1}{2}\cos 4x\bigg)\, dx\\
& = \tfrac{1}{4}\int \bigg(\tfrac{3}{2}-2\cos 2x+\tfrac{1}{2}\cos 4x\bigg)\, dx

```

````{admonition} Half-Angle Identity
```{math}
\cos^2 2x =\tfrac{1}{2}(1+\cos 2(2x))=\tfrac{1}{2}+\tfrac{1}{2}\cos 4x
```
````

`````



`````{tabbed} Step 4
**Antiderivative:** It took us a few tries, but at this point we've reduced our even powers of sine and cosine, down to one of our K-form integrals. So now we're ready to integrate:
```{math}
& = \tfrac{1}{4}\int \bigg(\tfrac{3}{2}-2\cos 2x+\tfrac{1}{2}\cos 4x\bigg)\, dx\\
&= \tfrac{1}{4}\bigg(\tfrac{3}{2}x-\sin 2x+\tfrac{1}{8}\sin 4x\bigg) + C
```
And as always when we do an indefinite integral, we need to remember the +C at the end.


````{admonition} K-form Integral

```{math}
\int \cos(kx)\, dx = \tfrac{1}{k}\sin(kx)+C
```
````

`````




``````


## Different Angles

Sometimes we will come across trig integrals where the inner functions, the angles, are different. In these cases it will be helpful to use: 


````{admonition} Different Angle Trig Identities
```{math}
\sin A \cos B &=\tfrac{1}{2}\bigg(\sin(A-B)+\sin(A+B)\bigg)\\
\sin A \sin B &=\tfrac{1}{2}\bigg(\cos(A-B)-\cos(A+B)\bigg)\\
\cos A \cos B &=\tfrac{1}{2}\bigg(\cos(A-B)+\cos(A+B)\bigg)
```
````


## Example 7
Integrate the following:

$$
\int \sin3x \cos7x  \, dx
$$

``````{dropdown} Solution (Click to see the steps.)

`````{tabbed} Step 1
**Different Angle:** The trig functions have different angles so we can apply our different angle identity.
```{math}
\int \sin3x \cos7x  \, dx &= \tfrac{1}{2}\int \bigg(\sin(3x-7x)+\sin(3x+7x)\bigg)\, dx \\
&= \tfrac{1}{2}\int \bigg(\sin(-4x)+\sin(10x)\bigg)\, dx

```
````{admonition} Different Angle Trig Identities
```{math}
\sin A \cos B =\tfrac{1}{2}\bigg(\sin(A-B)+\sin(A+B)\bigg)\\

```
````

`````

`````{tabbed} Step 2
**K-form Integrals:** Each of these is now one of our k-form integrals, which we can just integrate:
```{math}
&= \tfrac{1}{2}\int \bigg(\sin(-4x)+\sin(10x)\bigg)\, dx \\
&= \tfrac{1}{2}\bigg(\tfrac{1}{4}\cos(-4x)-\tfrac{1}{10}\cos(10x)\bigg)+C

```

And as always when we do an indefinite integral, we need to remember the +C at the end.



````{admonition} K-form Integrals

```{math}
\int \sin(kx)\, dx = -\tfrac{1}{k}\cos(kx)+C
```


`````





``````
