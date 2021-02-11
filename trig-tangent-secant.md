# (I-6) Trigonometric Integrals Involving Powers of Tangent and Secant

In this lesson we are going to see how to calculate integrals of the form:

$$
\int \tan^m x \sec^n x \, dx
$$


## Substitution Rule

Our main strategy is going to be a $u$-substitution with either $u=\sec x$ or $u=\tan x$. Which one we choose, ultimately comes down to the differentials.


````{panels}
:column: col-sm
:card: border-2
```{math}
u&=\sec x\\
du&=\sec x\tan x \, dx
```
---

```{math}
u&=\tan x\\
du&=\sec^2 x \, dx
```

````

In order to make the differentials match with what's actually in our integral, we start with the function we're integrating and factor off either a $\left(\sec x \tan x\right)$ term or a $\left(\sec^2 x\right)$ term and put it next to the $dx$.

````{panels}
If we factor off $\left(\sec x \tan x\right)$
^^^
1. Convert all remaining trig terms to $\sec x$.
2. Choose $u=\sec x$ for our subsitution
3. Finish integrating using Substitution Rule

---
If we factor off $\left(\sec^2 x\right)$ 
^^^
1. Convert all remaining trig terms to $\tan x$.
2. Choose $u=\tan x$ for our subsitution
3. Finish integrating using Substitution Rule

````
In order to convert between powers of $\sec x$ and powers of $\tan x$ we use the following identity:

````{admonition} Trigonometric Identity
```{math}
\sec^2 \theta = 1+\tan^2 \theta
```
````


## Example 1
Integrate the following:

$$
\int \tan^6 x \sec^4 x \, dx
$$

``````{dropdown} Solution (Click to see the steps.)

````{tabbed} Step 1
**Separate:** We start by separating off a $\left(\sec^2 x \right)$ term to get:
```{math}
\int \tan^6 x \sec^4 x \, dx = \int \tan^6 x \sec^2 x \cdot \left(\sec^2 x \right)\, dx
```

````

````{tabbed} Step 2
**Convert:** Since we factored off a $\left(\sec^2 x \right)$ term, this means we need to convert all remaining trig functions into powers of $\tan x$.
```{math}
&= \int \tan^6 x \sec^2 x \cdot \left(\sec^2 x \right)\, dx\\
&= \int \tan^6 x \left(1+\tan^2 x\right) \cdot \left(\sec^2 x \right)\, dx\\
```
This is where we use the trig identity: $\sec^2 \theta = 1+\tan^2 \theta$
````

`````{tabbed} Step 3
**Choose u:** Now we're ready for a $u$-substitution. Since we factored off a $\left(\sec^2 x \right)$  term, we choose: 
```{math}
 u=\tan x
```
and then we calculate $du$ to get:
```{math}
 du = \sec^2 x  \, dx
```

And then substituting our $u$ and $du$ into the integral gives us:
```{math}
&= \int \tan^6 x \left(1+\tan^2 x\right) \cdot \left(\sec^2 x \right)\, dx\\
&= \int u^6 \left(1+u^2\right) \, du\\
```


`````

````{tabbed} Step 4
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

---



## Example 2
Integrate the following:

$$
\int \tan^5 x \sec^7 x \, dx
$$

``````{dropdown} Solution (Click to see the steps.)

````{tabbed} Step 1
**Separate:** We start by separating off a $\left(\sec x \tan x \right)$ term to get:
```{math}
\int \tan^5 x \sec^7 x \, dx = \int \tan^4 x \sec^6 x \cdot \left(\sec x \tan x \right)\, dx
```

````

````{tabbed} Step 2
**Convert:** Since we factored off a $\left(\sec x \tan x \right)$ term, this means we need to convert all remaining trig functions into powers of $\sec x$.
```{math}
&= \int \tan^4 x \cdot \sec^6 x \cdot  \left(\sec x \tan x \right)\, dx\\
&= \int \tan^2 x \cdot \tan^2 x \cdot \sec^6 x \cdot \left(\sec x \tan x \right)\, dx\\
&= \int \left(\sec^2 x-1\right)\left(\sec^2 x-1\right) \sec^6 x \cdot \left(\sec x \tan x \right)\, dx\\
```
This is where we use the trig identity: $\sec^2 \theta = 1+\tan^2 \theta$
````

`````{tabbed} Step 3
**Choose u:** Now we're ready for a $u$-substitution. Since we factored off a $\left(\sec x \tan x \right)$ term, we choose: 
```{math}
 u=\sec x
```
and then we calculate $du$ to get:
```{math}
 du = \sec x \tan x \, dx
```

And then substituting our $u$ and $du$ into the integral gives us:
```{math}
&= \int \left(\sec^2 x-1\right)\left(\sec^2 x-1\right) \sec^6 x \cdot \left(\sec x \tan x \right)\, dx\\
&= \int \left(u^2-1\right)\left(u^2-1\right) u^6 \, du\\
```


`````

````{tabbed} Step 4
**Finish It!** And finally we finish the integration. First multiply everything out so that we have power functions to integrate.

```{math}
&= \int \left(u^2-1\right)\left(u^2-1\right) u^6 \, du\\
&= \int \left(u^4-2u^2+1\right) u^6 \, du\\
&= \int \left(u^{10}-2u^8+u^6\right) \, du\\
&= \tfrac{1}{11}u^{11}-\tfrac{2}{9}u^9+\tfrac{1}{7}u^7+C\\
```
And then finally we convert back to $x$ to get our answer:
```{math}
&= \tfrac{1}{11}\sec^{11}x-\tfrac{2}{9}\sec^9x+\tfrac{1}{7}\sec^7x+C\\
```
(Don't forget $+C$ for indefinite integrals!)
````
``````



