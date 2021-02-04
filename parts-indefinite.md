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

```{math}
&\int e^{kx}\, dx = \tfrac{1}{k}e^{kx}+C\\
&\int \sin(kx)\, dx = -\tfrac{1}{k}\cos(kx)+C\\
&\int \cos(kx)\, dx = \tfrac{1}{k}\sin(kx)+C
```

