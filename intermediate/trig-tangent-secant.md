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

## Get Creative

Unfortunately, the substitution strategy used in the first two examples doesn't always work. If this happens we have a few more things to try:

1. **Use Trig Identities:** Keep trying to use our main identity $\sec^2 \theta = 1 + \tan^2\theta$, you might still get something useful.
1. **Convert to sine and cosine:** We have techniques for integrating powers of $\sin x$ and $\cos x$ which might be helpful.
1. **Integration by parts:** This can be a helpful way to move exponents between trig functions. Maybe try making the $dv$ term either $\sec^2 x$ or $\sec x \tan x$.

A lot of times, success with the above methods comes down to also knowing:

````{admonition} Helpful Antiderivatives
```{math}
\int \tan x \, dx & = \ln \left|\sec x \right| +C\\
\int \sec x \, dx & = \ln \left|\sec x +\tan x \right| +C\\
```
````

## Example 3

Integrate the following:

$$
\int \tan^3 x  \, dx
$$

``````{dropdown} Solution 1 (Trig identities)

````{tabbed} Step 1
**Separate:** We are still going to try using our trig identity: $\sec^2 x = 1 + \tan^2x$. Since this has a $\tan^2 x$ term, let's start by breaking our function up:
```{math}
\int \tan^3 x  \, dx = \int \tan x \tan^2 x\, dx
```

````

````{tabbed} Step 2
**Trig Identity:** Now we can apply the trig identity $\sec^2 x = 1 + \tan^2x$ to get:
```{math}
\int \tan x \tan^2 x\, dx &= \int \tan x \left(\sec^2 x -1\right) \, dx  \\
&= \int \left(\tan x \cdot \sec^2 x -\tan x\right) \, dx  \\
```
And we also multiply everything out.
````

`````{tabbed} Step 3
Now it comes down to 2 integrals:

````{panels}
```{math}
\int \tan x \sec^2 x\, dx
```
Here we have an **even power** of secant, so we can use our usual strategy: **substitution rule.**
```{math}
u&=\tan x\\
du&=\sec^2 x
```
---

```{math}
\int \tan x \, dx
```
This is just one of our helpful antiderivatives which we can just look up:

```{math}
\int \tan x \, dx  = \ln \left|\sec x \right| +C

```

````


`````

````{tabbed} Step 4
**Finish It!** And finally we put it all together and get:

```{math}
&= \int \left(\tan x \cdot \sec^2 x -\tan x\right) \, dx  \\
&= \int \tan x \cdot \sec^2 x \, dx -\int \tan x \, dx  \\
&= \tfrac{1}{2}\tan^2 x -\ln \left|\sec x \right| +C \\
```

(Don't forget $+C$ for indefinite integrals!)
````
``````


``````{dropdown} Solution 2 (Convert to sine and cosine)

````{tabbed} Step 1
**Convert:** We are going to start by converting everything into sine and cosine terms:
```{math}
\int \tan^3 x  \, dx = \int \dfrac{\sin^3 x}{\cos^3 x}\, dx
```

````

````{tabbed} Step 2
**Powers of Sine:** Since we have an odd power of sine in the numerator, we can separate off one $\sin x$ and put it next to the $dx$
```{math}
\int \dfrac{\sin^3 x}{\cos^3 x}\, dx = \int \dfrac{\sin^2 x}{\cos^3 x}\cdot \sin x\, dx 
```
Putting a $\sin x$ next to $dx$ tells us we are going to use the opposite function $\cos x$ as our $u$-sub. So let's convert everything else remaining in our integral to cosine:
```{math}
= \int \dfrac{1-\cos^2 x}{\cos^3 x}\cdot \sin x\, dx 
```
Here we use our standard trig identity: $\sin^2\theta +\cos^2\theta =1$


````

`````{tabbed} Step 3
**Substitution:** Now we can do our $u$-substitution:

```{math}
u&=\cos x\\
du&=-\sin x \, dx \longrightarrow (-1)du=\sin x \, dx\\
```

And plugging all of this into our integral gives us:

```{math}
&= \int \dfrac{1-\cos^2 x}{\cos^3 x}\cdot \sin x\, dx\\
& = \int \dfrac{1-u^2}{u^3}\cdot (-1)\, du \\
& = \int \dfrac{u^2-1}{u^3}\, du \\
```



`````

````{tabbed} Step 4
**Finish It!** And finally if we do the division we can finish the integration:

```{math}
& = \int \dfrac{u^2-1}{u^3}\, du \\
& = \int \tfrac{1}{u}-\tfrac{1}{u^3}\, du \\
&= \ln\left|u\right|+\tfrac{1}{2}u^{-2} +C \\
```
And converting back to our original variable:
```{math}
&= \ln\left|\cos x\right|+\tfrac{1}{2}\cos^{-2} x +C \\
```

(Don't forget $+C$ for indefinite integrals!)
````
``````


## Example 4

Integrate the following:

$$
\int \sec^3 x  \, dx
$$

``````{dropdown} Solution (Using Integration By Parts and Trig Identities)

`````{tabbed} Step 1
**Separate:** We start by separating off a $\left(\sec^2 x \right)$ term to get:
```{math}
\int \sec^3 x  \, dx  = \int \sec x \cdot \sec^2 x \, dx
```

Now we can choose $u$ and $dv$:

````{panels}
```{math}
u&= \sec x\\
du&=\sec x \tan x \, dx
```
---
```{math}
dv&= \sec^2 x\, dx\\
v&=\tan x 
```
````

The reason why we factored off a $\sec^2 x $ term and chose that for $dv$ is because it is easy to integrate (its one of our elementary antiderivatives). 

Applying the integration by parts formula gives us:
```{math}
= \sec x \tan x-\int \sec x \tan^2 x \, dx
```




`````

````{tabbed} Step 2
**Trig Identity:** The resulting integral from the integration by parts is still tricky, so we try using a trig identity:
```{math}
&= \sec x \tan x-\int \sec x \tan^2 x \, dx\\
&= \sec x \tan x-\int \sec x \left(\sec^2 x-1\right) \, dx\\
&= \sec x \tan x-\int \sec^3 x -\sec x \, dx
```
And now it seems like we might be back where we started, so let's formally state what we have so far:

```{math}
\int \sec^3 x \, dx = \sec x \tan x-\int \sec^3 x \, dx  +\int \sec x \, dx
```
````

`````{tabbed} Step 3
**Unknown Integral:** If we look at this resulting equation we see that our unknown integral shows up on both sides. 
```{math}
\int \sec^3 x \, dx = \sec x \tan x-\int \sec^3 x \, dx  +\int \sec x \, dx
```
So let's actually solve for it! And to help picture some of the algebra we'll rename our unknown integral:
```{math}
Y = \int \sec^3 x \, dx 
```
Giving us the (shortened) equation:

```{math}
Y= \sec x \tan x- Y  +\int \sec x \, dx
```

Now we just need to solve for $Y$. Add $Y$ to both sides to get:

```{math}
2Y= \sec x \tan x +\int \sec x \, dx
```

And then divide both sides by $2$:

```{math}
Y= \tfrac{1}{2}\sec x \tan x + \tfrac{1}{2}\int \sec x \, dx
```
And there we go!
```{math}
\int \sec^3 x \, dx = \tfrac{1}{2}\sec x \tan x + \tfrac{1}{2}\int \sec x \, dx
```
`````

`````{tabbed} Step 4
**Finish It!** And finally we can finish the remaining integral with the use of some helpful antiderivatives:
```{math}
\int \sec^3 x \, dx &= \tfrac{1}{2}\sec x \tan x + \tfrac{1}{2}\int \sec x \, dx \\
&=  \tfrac{1}{2}\sec x \tan x + \tfrac{1}{2}\ln \left|\sec x +\tan x \right| +C \\
```
(Don't forget $+C$ for indefinite integrals!)


````{admonition} Helpful Antiderivatives
```{math}
\int \tan x \, dx & = \ln \left|\sec x \right| +C\\
\int \sec x \, dx & = \ln \left|\sec x +\tan x \right| +C\\
```
````


`````
``````

