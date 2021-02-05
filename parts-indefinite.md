# Integration By Parts for Indefinite Integrals

## The Product Rule

We're going to start by first recalling one of our derivative rules, the **product rule.**

$$
\dfrac{d}{dx}\big[f(x)\cdot g(x)\big] = \big[f(x)\big]' \cdot g(x) + f(x)\cdot \big[g(x)\big]'
$$ 

If we integrate both sides of this equation we get:

$$
f(x)\cdot g(x)= \int \big[f(x)\big]' \cdot g(x)\; dx + \int f(x)\cdot \big[g(x)\big]'
\; dx
$$ 

And then finally we rearrange the terms to get our **integration by parts** formula:

$$
\int f(x)\cdot \big[g(x)\big]' \; dx = f(x)\cdot g(x) - \int   g(x)\cdot \big[f(x)\big]'\; dx
$$ 


## The Formula


````{admonition} Integration By Parts
```{math}
\int u \; dv = uv -\int v \; du
```
````


### How It Works

We tend to think of integration by parts as a process:

1. Choose $u$ and $dv$.
2. Calculate $du$ and $v$.
3. Plug all of these pieces into the formula.
4. Finish integrating.


## Example 1
Integrate the following:

$$
\int x \cdot e^x \, dx
$$


````{tabbed} Solution
Click through the steps to see what we do.

If you want, give it a try first! (Use the steps listed above as a guide to get you started.)
````

`````{tabbed} Step 1
Our first step is choose $u$ and $dv$: 
````{panels}
:column: col-sm
:card: border-2
Our choice for $u$
^^^
```{math}
u=x
```
---
Our choice for $dv$
^^^
```{math}
dv = e^x \; dx
```
````
`````

`````{tabbed} Step 2
Next, we calculate $du$ and $v$ by differentiating and integrating respectively:
````{panels}
:column: col-sm
:card: border-2
Differentiate
^^^
\begin{align*}
u &=x \\
du &= 1\cdot dx
\end{align*}

---
Integrate
^^^
\begin{align*}
dv &=e^x \; dx \\
v &=e^x
\end{align*}

````
`````

`````{tabbed} Step 3
Now we take the pieces we just calculated and plug them into the integration by parts formula.

````{panels}
:column: col-sm
:card: border-2
Our pieces
^^^
\begin{align*}
u &=x & dv &=e^x \; dx \\
du &=  dx & v &=e^x
\end{align*}

---
The Formula
^^^
```{math}
\int u \; dv = uv -\int v \; du
```

````
Doing this we get:
```{math}
\int x \cdot e^x\; dx = x\cdot e^x -\int e^x \; dx
```


`````

````{tabbed} Step 4
And finally we finish calculating any remaining integrals:
\begin{align*}
\int x \cdot e^x\; dx & = x\cdot e^x -\int e^x \; dx \\
 & = x\cdot e^x - e^x +C
\end{align*}
(Don't forget $+C$ for indefinite integrals!)
````








## How to Choose?

So the question is, how do we choose $u$ and $dv$? Well, just like with substitution rule, there are a few strategies we can keep in mind, but it does come down to practice and a little trial-and-error.

```{note}
In both strategies listed below we first need to break the function into **two pieces** *or parts.*
```


````{panels}
:column: col-sm
:card: border-2
Meta-Strategy
^^^
We look at the **two parts** of our function and choose $u$ and $dv$ such that the:
- $u$ term **simplifies when differentiated**
- $dv$ term is **easily integrated**


---
**L I A T E** - Strategy
^^^
A more specific strategy is to remember the acronym LIATE

- **L** - logarithmic functions
- **I** - inverse trigonometric functions 
- **A** - algebraic functions 
- **T** - trigonometric functions
- **E** - exponential functions.

We classify each **part** of our function based on these 5 categories.
- Choose $u$ to be the part higher on this list
- Choose $dv$ to be the part lower on this list
````




---


## Example 2
Integrate the following:

$$
\int (2x+5) \cdot \sin(3x) \, dx
$$

```{dropdown} **Question:** What do <em>you</em> think we should pick for $u$ and $dv$ in this example?
**Answer:** Maybe give $u=2x+5$ and $dv= \sin(3x) \cdot dx$ a try?
```


````{tabbed} Solution
Click through the steps to see what we do.

If you want, give it a try first! (Use the steps listed above as a guide to get you started.)
````

`````{tabbed} Step 1
Our first step is to choose $u$ and $dv$. To help with this decision we classify the two parts of our function. 

````{panels}
:column: col-sm
:card: border-2
**A** for Algebraic
^^^
```{math}
2x+5
```
---
**T** for Trigonometric
^^^
```{math}
\sin(3x) 
```
````

Since we have an algebraic part and a trigonometric part, the algebraic part is our choice for $u$ and the trigonometric part is our choice for $dv$.

````{panels}
:column: col-sm
:card: border-2
Our choice for $u$
^^^
```{math}
u=2x+5
```
---
Our choice for $dv$
^^^
```{math}
dv = \sin(3x) \; dx
```
````
`````

`````{tabbed} Step 2
Next, we calculate $du$ and $v$ by differentiating and integrating respectively:
````{panels}
:column: col-sm
:card: border-2
Differentiate
^^^
\begin{align*}
u &=2x+5 \\
du &= 2\cdot dx
\end{align*}

---
Integrate
^^^
\begin{align*}
dv &=\sin(3x) \; dx \\
v &=-\tfrac{1}{3}\cos(3x)
\end{align*}

````
`````

`````{tabbed} Step 3
Now we take the pieces we just calculated and plug them into the integration by parts formula.

````{panels}
:column: col-sm
:card: border-1
The Formula
^^^
```{math}
\int u \; dv = uv -\int v \; du
```

````

````{panels}
:column: col-sm
:card: border-1
Our pieces
^^^
\begin{align*}
u &=2x+5 & dv &=\sin(3x) \; dx \\
du &=  2\cdot dx & v &=-\tfrac{1}{3}\cos(3x)
\end{align*}

````


Doing this we get:
\begin{align*}
\int (2x+5) \cdot \sin(3x) & \, dx = uv -\int v \; du \\
& = (2x+5)\cdot \left(-\tfrac{1}{3}\cos(3x) \right) -\int \left(-\tfrac{1}{3}\cos(3x) \right) \cdot 2 \; dx
\end{align*}


`````

````{tabbed} Step 4
And finally we finish calculating any remaining integrals:
\begin{align*}
&= -\tfrac{1}{3}(2x+5)\cdot \cos(3x)  + \tfrac{2}{3}\int \cos(3x)  \; dx \\
& = -\tfrac{1}{3}(2x+5)\cdot \cos(3x) + \tfrac{2}{3}\left( \tfrac{1}{3}\sin(3x)\right)+C
\end{align*}
(Don't forget $+C$ for indefinite integrals!)
````


## K-form Integrals

Below are a few helpful integral formulas that we will need to use pretty frequently. (You can prove each of these using substitution rule with $u=kx$).

````{admonition} K-form Integrals

```{math}
&\int e^{kx}\, dx = \tfrac{1}{k}e^{kx}+C\\
&\int \sin(kx)\, dx = -\tfrac{1}{k}\cos(kx)+C\\
&\int \cos(kx)\, dx = \tfrac{1}{k}\sin(kx)+C
```
````

## Example 3
Integrate the following:

$$
\int x^2 \cdot \ln(2x) \, dx
$$

```{dropdown} **Question:** What do <em>you</em> think we should pick for $u$ and $dv$ in this example?
**Answer:** Maybe give $u=\ln(2x)$ and $dv= x^3 \cdot dx$ a try?
```


````{tabbed} Solution
Click through the steps to see what we do.

If you want, give it a try first! (Use the steps listed above as a guide to get you started.)
````

`````{tabbed} Step 1
Our first step is to choose $u$ and $dv$. To help with this decision we classify the two parts of our function. 

````{panels}
:column: col-sm
:card: border-2
**A** for Algebraic
^^^
```{math}
x^2
```
---
**L** for Logarithmic
^^^
```{math}
\ln(2x) 
```
````

Since we have an algebraic part and a logarithmic part, the algebraic part is our choice for $dv$ and the logarithmic part is our choice for $u$.

````{panels}
:column: col-sm
:card: border-2
Our choice for $u$
^^^
```{math}
u=\ln(2x) 
```
---
Our choice for $dv$
^^^
```{math}
dv = x^2 \; dx
```
````
`````

`````{tabbed} Step 2
Next, we calculate $du$ and $v$ by differentiating and integrating respectively:
````{panels}
:column: col-sm
:card: border-2
Differentiate
^^^
\begin{align*}
u &=\ln(2x) \\
du &= \dfrac{1}{2x}\cdot \big[2x\big]'\cdot dx
\end{align*}

---
Integrate
^^^
\begin{align*}
dv &=x^2 \; dx \\
v &=\tfrac{1}{3}x^3
\end{align*}

````
`````

`````{tabbed} Step 3
Now we take the pieces we just calculated and plug them into the integration by parts formula.

````{panels}
:column: col-sm
:card: border-1
The Formula
^^^
```{math}
\int u \; dv = uv -\int v \; du
```

````

````{panels}
:column: col-sm
:card: border-2
Our pieces
^^^
\begin{align*}
u &=\ln(2x) & dv &=x^2 \; dx \\
du &=  \dfrac{1}{x}\cdot dx & v &=\tfrac{1}{3}x^3
\end{align*}

````


Doing this we get:
\begin{align*}

\int x^2 \cdot \ln(2x) \,& dx = uv -\int v \; du \\
&= \ln(2x)\cdot \left(\tfrac{1}{3}x^3 \right) -\int \left(\tfrac{1}{3}x^3 \right) \cdot \dfrac{1}{x} \; dx
\end{align*}


`````

````{tabbed} Step 4
And finally we finish calculating any remaining integrals. Notice that we need to multiply the $x^3$ and $1/x$ together, before we can actually do that integral.
\begin{align*}
&= \ln(2x)\cdot \left(\tfrac{1}{3}x^3 \right) -\int \left(\tfrac{1}{3}x^3 \right) \cdot \dfrac{1}{x} \; dx \\
&= \tfrac{1}{3}x^3\cdot \ln(2x) -\int \tfrac{1}{3}x^2 \; dx\\
&= \tfrac{1}{3}x^3\cdot \ln(2x) - \tfrac{1}{9}x^3 +C
\end{align*}
(Don't forget $+C$ for indefinite integrals!)

````

## Example 4 (Inverse)

```{note}
In this example we see the general strategy for integrating **inverse functions.**
```




Integrate the following:

$$
\int \ln x \, dx
$$

```{dropdown} **Question:** What do <em>you</em> think we should pick for $u$ and $dv$ in this example?
**Answer:** Maybe we could do: $u=\ln x$ and $dv= 1\cdot dx$?
```


````{tabbed} Solution
Click through the steps to see what we do.

If you want, give it a try first! (Use the steps listed above as a guide to get you started.)
````

`````{tabbed} Step 0
Looking at this function we see that:
 - its not one of our elementary forms and 
 - its not a composite function (so substitution rule most likely doesn't apply)

What can we do? A little bit of a trick: write the function as a product.

$$ 
\left(\ln x\right)\cdot 1
$$

So that we have the integral:

$$
\int \left(\ln x\right)\cdot 1 \cdot \, dx
$$

`````


`````{tabbed} Step 1
Our first step is to choose $u$ and $dv$. To help with this decision we classify the two parts of our function. 

````{panels}
:column: col-sm
:card: border-2
**A** for Algebraic
^^^
```{math}
1
```
---
**L** for Logarithmic
^^^
```{math}
\ln x 
```
````

Since we have an algebraic part and a logarithmic part, the algebraic part is our choice for $dv$ and the logarithmic part is our choice for $u$.

````{panels}
:column: col-sm
:card: border-2
Our choice for $u$
^^^
```{math}
u=\ln x 
```
---
Our choice for $dv$
^^^
```{math}
dv = 1\cdot dx
```
````
`````

`````{tabbed} Step 2
Next, we calculate $du$ and $v$ by differentiating and integrating respectively:
````{panels}
:column: col-sm
:card: border-2
Differentiate
^^^
\begin{align*}
u &=\ln x \\
du &= \dfrac{1}{x}\cdot dx
\end{align*}

---
Integrate
^^^
\begin{align*}
dv &=1 \cdot dx \\
v &=x
\end{align*}

````
`````

`````{tabbed} Step 3
Now we take the pieces we just calculated and plug them into the integration by parts formula.

````{panels}
:column: col-sm
:card: border-1
The Formula
^^^
```{math}
\int u \; dv = uv -\int v \; du
```

````

````{panels}
:column: col-sm
:card: border-2
Our pieces
^^^
\begin{align*}
u &=\ln x & dv &=1 \cdot dx \\
du &=  \dfrac{1}{x}\cdot dx & v &=x
\end{align*}

````


Doing this we get:
\begin{align*}

\int \ln x \,& dx = uv -\int v \; du \\
&= \left(\ln x\right)\cdot x -\int x\cdot  \dfrac{1}{x} \; dx
\end{align*}


`````

````{tabbed} Step 4
And finally we finish calculating any remaining integrals. Notice that we need to multiply the $x$ and $1/x$ together, before we can actually do that remaining integral.
\begin{align*}
&= \left(\ln x\right)\cdot x -\int x\cdot  \dfrac{1}{x} \; dx\\
&= x\ln x -\int 1 \; dx\\
&= x\ln x -x +C
\end{align*}
(Don't forget $+C$ for indefinite integrals!)

````


## Example 5 (Twice)

```{note}
In this example we see that when solving an integral, sometimes, we need to use integration-by-parts **more than once.**
```
Integrate the following:

$$
\int x^2 e^{-2x} \, dx
$$

```{dropdown} **Question:** What do <em>you</em> think we should pick for $u$ and $dv$ in this example?
**Answer:** Let's do $u=x^2$ and $dv= e^{-2x} \cdot dx$.
```


### First Time
````{tabbed} Solution
Click through the steps to see what we do.

If you want, give it a try first! (Use the steps listed above as a guide to get you started.)
````

`````{tabbed} Step 1
Our first step is to choose $u$ and $dv$. To help with this decision we classify the two parts of our function. 

````{panels}
:column: col-sm
:card: border-2
**A** for Algebraic
^^^
```{math}
x^2
```
---
**E** for Exponential
^^^
```{math}
e^{-2x}
```
````

Since we have an algebraic part and an exponential part, the algebraic part is our choice for $u$ and the exponential part is our choice for $dv$.

````{panels}
:column: col-sm
:card: border-2
Our choice for $u$
^^^
```{math}
u= x^2
```
---
Our choice for $dv$
^^^
```{math}
dv = e^{-2x} \; dx
```
````
`````

`````{tabbed} Step 2
Next, we calculate $du$ and $v$ by differentiating and integrating respectively:
````{panels}
:column: col-sm
:card: border-2
Differentiate
^^^
\begin{align*}
u &=x^2 \\
du &= 2x\cdot dx
\end{align*}

---
Integrate
^^^
\begin{align*}
dv &= e^{-2x} \; dx \\
v &=-\tfrac{1}{2}e^{-2x}
\end{align*}

````
`````

`````{tabbed} Step 3
Now we take the pieces we just calculated and plug them into the integration by parts formula.

````{panels}
:column: col-sm
:card: border-1
The Formula
^^^
```{math}
\int u \; dv = uv -\int v \; du
```

````

````{panels}
:column: col-sm
:card: border-1
Our pieces
^^^
\begin{align*}
u &=x^2 & dv &= e^{-2x} \; dx \\
du &=  2x\cdot dx & v &=-\tfrac{1}{2}e^{-2x}
\end{align*}

````


Doing this we get:
\begin{align*}
\int x^2 \cdot e^{-2x} & \, dx = uv -\int v \; du \\
& = x^2\cdot \left(-\tfrac{1}{2}e^{-2x}\right) -\int \left(-\tfrac{1}{2}e^{-2x} \right) \cdot 2x \; dx
\end{align*}


`````

````{tabbed} Step 4
And finally we finish calculating any remaining integrals:
\begin{align*}
& = x^2\cdot \left(-\tfrac{1}{2}e^{-2x}\right) -\int \left(-\tfrac{1}{2}e^{-2x} \right) \cdot 2x \; dx \\
&= -\tfrac{1}{2}x^2e^{-2x}  + \int x \cdot e^{-2x}  \; dx
\end{align*}
But at this point we might realize the resulting integral is still a product of an algebraic part and an exponential part ... so we need to use integration by parts again!

````



### Second Time






````{tabbed} Step 0
So now it becomes a problem of integrating:


```{math}
\int x \cdot e^{-2x}  \; dx
```
````

`````{tabbed} Step 1
Our first step is to choose $u$ and $dv$. To help with this decision we classify the two parts of our function. 

````{panels}
:column: col-sm
:card: border-2
**A** for Algebraic
^^^
```{math}
x
```
---
**E** for Exponential
^^^
```{math}
e^{-2x}
```
````

Since we have an algebraic part and an exponential part, the algebraic part is our choice for $u$ and the exponential part is our choice for $dv$. You may notice that this integral is similar to the one we started with, and so our choice for $u$ and $dv$ here are similar to what we used the first time.

````{panels}
:column: col-sm
:card: border-2
Our choice for $u$
^^^
```{math}
u= x
```
---
Our choice for $dv$
^^^
```{math}
dv = e^{-2x} \; dx
```
````
`````

`````{tabbed} Step 2
Next, we calculate $du$ and $v$ by differentiating and integrating respectively:
````{panels}
:column: col-sm
:card: border-2
Differentiate
^^^
\begin{align*}
u &=x \\
du &=  dx
\end{align*}

---
Integrate
^^^
\begin{align*}
dv &= e^{-2x} \; dx \\
v &=-\tfrac{1}{2}e^{-2x}
\end{align*}

````
`````

`````{tabbed} Step 3
Now we take the pieces we just calculated and plug them into the integration by parts formula.

````{panels}
:column: col-sm
:card: border-1
The Formula
^^^
```{math}
\int u \; dv = uv -\int v \; du
```

````

````{panels}
:column: col-sm
:card: border-1
Our pieces
^^^
\begin{align*}
u &=x & dv &= e^{-2x} \; dx \\
du &=  dx & v &=-\tfrac{1}{2}e^{-2x}
\end{align*}

````


Doing this we get:
\begin{align*}
\int x \cdot e^{-2x} & \, dx = uv -\int v \; du \\
& = x\cdot \left(-\tfrac{1}{2}e^{-2x}\right) -\int \left(-\tfrac{1}{2}e^{-2x} \right) \; dx
\end{align*}


`````

````{tabbed} Step 4
And finally we finish calculating any remaining integrals:
\begin{align*}
& = x\cdot \left(-\tfrac{1}{2}e^{-2x}\right) -\int \left(-\tfrac{1}{2}e^{-2x} \right) \; dx\\
&= -\tfrac{1}{2}xe^{-2x}  + \tfrac{1}{2} \int  e^{-2x}  \; dx \\
&= -\tfrac{1}{2}xe^{-2x}  + \tfrac{1}{2} \left(\tfrac{-1}{2} e^{-2x}\right) +C
\end{align*}
But we're not done yet ...

````



### All Together

````{panels}
:column: col-sm
:card: border-2

First Time
^^^

From our first integration by parts we found:

```{math}
\int x^2 e^{-2x} \, dx =-\tfrac{1}{2}x^2e^{-2x}  + \int x \cdot e^{-2x}  \; dx
```
---

Second Time
^^^
From our second integration by parts we found:

```{math}
\int x \cdot e^{-2x}  \; dx = -\tfrac{1}{2}xe^{-2x}  - \tfrac{1}{4}  e^{-2x} +C
```

````

So putting this all together we get:

```{math}
\int x^2 e^{-2x} \, dx =-\tfrac{1}{2}x^2e^{-2x}  -\tfrac{1}{2}xe^{-2x}  - \tfrac{1}{4}  e^{-2x} +C
```

And if we wanted to, we could simplify by factoring out $-\tfrac{1}{2} e^{-2x}$ on the right:

```{math}
-\tfrac{1}{2}e^{-2x}(x^2+x+\tfrac{1}{2})+C
```


## Example 6

Integrate the following:

$$
\int e^x \sin (5x) \, dx
$$

```{dropdown} **Question:** What do <em>you</em> think we should pick for $u$ and $dv$ in this example?
**Answer:** Let's do $u=\sin (5x)$ and $dv= e^{x} \cdot dx$.
```


````{tabbed} Solution
Click through the steps to see what we do.

If you want, give it a try first! (Use the steps listed above as a guide to get you started.)
````

`````{tabbed} First Time
Using our LIATE strategy, we choose $u$ to be the trigonometric part of our function and $dv$ to be the exponential part. Then to get all of our ingredients, we calculate $du$ and $v$ by differentiating and integrating respectively.

````{panels}
:column: col-sm
:card: border-1
Our pieces
^^^
\begin{align*}
u &=\sin(5x) & dv &= e^x \; dx \\
du &=  5\cos(5x)\cdot dx & v &=e^x
\end{align*}

````

Applying the integration by parts formula we get:

```{math}
\int e^x \sin (5x) \, dx = e^x\sin(5x)-\int  e^x\cdot 5 \cos(5x) \, dx
```

After this, it doesn't feel like we got anywhere, other than converting our integral with a sine term into an integral with a cosine term. Not to fear! There is a **trick** and its to do integration by parts again. 
`````

`````{tabbed} Second Time

We now need to integrate: 
```{math}
\int  e^x\cdot 5 \cos(5x) \, dx
```
Using our LIATE strategy again we choose $u$ to be the trigonometric part and $dv$ to be the exponential part. **Be consistent!** Then calculate $du$ and $v$ just like before.
````{panels}
:column: col-sm
:card: border-1
Our pieces
^^^
\begin{align*}
u &=5\cos(5x) & dv &= e^x \; dx \\
du &=  -25\sin(5x)\cdot dx & v &=e^x
\end{align*}

````

Applying the integration by parts formula again we get:

```{math}
\int  e^x\cdot 5 \cos(5x) \, dx = 5e^x\cos(5x)+25\int  e^x\sin(5x) \, dx
```

`````

`````{tabbed} All Together
````{panels}
:column: col-sm
:card: border-1

First Time
^^^

From our first integration by parts we found:

```{math}
\int e^x \sin (5x) \, dx = e^x\sin(5x)-\int  e^x\cdot 5 \cos(5x) \, dx
```
````
````{panels}
:column: col-sm
:card: border-1

Second Time
^^^
From our second integration by parts we found:

```{math}
\int  e^x\cdot 5 \cos(5x) \, dx = 5e^x\cos(5x)+25\int  e^x\sin(5x) \, dx
```

````

So putting this all together we get:

```{math}
\int e^x \sin (5x) \, dx = e^x\sin(5x)-\left(5e^x\cos(5x)+25\int  e^x\sin(5x) \, dx\right)
```

And simplify just a little:

```{math}
\int e^x \sin (5x) \, dx = e^x\sin(5x)-5e^x\cos(5x)-25\int  e^x\sin(5x) \, dx
```

You might be thinking: Great! We're back to where we started, the integral of $e^x$ times $\sin(5x)$

Well ... there's one more **trick!**



`````

`````{tabbed} Solve 
Let's recap where we are. We have the unknown integral  we're trying to figure out:
````{panels}
:column: col-sm
:card: border-2

Unknown Integral
^^^


```{math}
\int e^x \sin (5x) \, dx 
```

````
After going through integration by parts twice, we have the following equation and we notice that our **unknown integral** appears on both sides: 

```{math}
\int e^x \sin (5x) \, dx = e^x\sin(5x)-5e^x\cos(5x)-25\int  e^x\sin(5x) \, dx
```

To help picture this, let's replace our unknown integral by $Y$:

```{math}
Y = e^x\sin(5x)-5e^x\cos(5x)-25Y
```

How would we solve this for $Y$? Well, we would add $25Y$ to both sides to get:

```{math}
26Y = e^x\sin(5x)-5e^x\cos(5x)
```

And then divide both sides by $26$ to get:

```{math}
Y = \tfrac{1}{26}e^x\sin(5x)-\tfrac{5}{26}e^x\cos(5x)
```

And there we go! We have our unknown antiderivative:
```{math}
\int e^x \sin (5x) \, dx = \tfrac{1}{26}e^x\sin(5x)-\tfrac{5}{26}e^x\cos(5x) +C
```


`````