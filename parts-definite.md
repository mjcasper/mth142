# Integration By Parts for Definite Integrals




## The Notation

When calculating a definite integral using integration by parts, we have two slightly different ways we can handle the evaluation (all of the integration-by-parts work will be exactly the same).

We can either evaluate each part of the formula separately: 

$$
\int_a^b f(x)\cdot g'(x) \; dx = f(x)\cdot g(x) \biggr\rvert_{a}^{b} - \int_a^b   g(x)\cdot f'(x)\; dx
$$ 

or we can just wait until we have fully finished finding the antiderivative and then evaluate everything all at once:

$$
\int_a^b f(x)\cdot g'(x) \; dx = \biggr[f(x)\cdot g(x)  - \int   g(x)\cdot f'(x)\; dx \biggr]_{a}^{b}
$$ 



---


## Example 1
Integrate the following:

$$
\int_{-1}^2 \dfrac{2x+5}{e^{3x}} \, dx
$$

``````{dropdown} Solution (Click to see the steps.)

````{tabbed} Step 0
Before we start any integration, it will be helpful to rewrite this function as a product:
```{math}
\int_{-1}^2 \dfrac{2x+5}{e^{3x}} \, dx = \int_{-1}^2 (2x+5)\cdot e^{-3x} \, dx
```

````

`````{tabbed} Step 1
We're going to use integration by parts, so our first step is to choose $u$ and $dv$: 
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
dv = e^{-3x} \; dx
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
```{math}
u &=2x+5 \\
du &= 2\cdot dx
```

---
Integrate
^^^
```{math}
dv &=e^{-3x} \; dx \\
v &=-\tfrac{1}{3}e^{-3x}
```

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

**Our Pieces** 

````{panels}
```{math}
u &=2x+5 \\
du &= 2\cdot dx
```

---

```{math}
dv &=e^{-3x} \; dx \\
v &=-\tfrac{1}{3}e^{-3x}
```
````


Doing this we get:
```{math}
\int_{-1}^2 (2x+5)\cdot e^{-3x} \, dx = \biggr[ -\tfrac{1}{3}(2x+5)e^{-3x}+\tfrac{2}{3}\int e^{-3x}\, dx\biggr]_{x=-1}^{x=2}
```


`````

````{tabbed} Step 4
Finish calculating any remaining integrals:
```{math}
&= \biggr[ -\tfrac{1}{3}(2x+5)e^{-3x}+\tfrac{2}{3}\int e^{-3x}\, dx\biggr]_{x=-1}^{x=2} \\
&= \biggr[ -\tfrac{1}{3}(2x+5)e^{-3x}+\tfrac{2}{3}\left(\tfrac{-1}{3}e^{-3x}\right)\biggr]_{x=-1}^{x=2}
```

````

````{tabbed} Step 5
Finally, simplify the antiderivative as much as you desire and then **evaluate**.
```{math}
&= \biggr[ -\tfrac{1}{3}e^{-3x}\left(2x+5+\tfrac{2}{3}\right)\biggr]_{x=-1}^{x=2} \\
&= \biggr( -\tfrac{1}{3}e^{-6}\left(4+5+\tfrac{2}{3}\right) \biggr) -\biggr( -\tfrac{1}{3}e^{3}\left(-2+5+\tfrac{2}{3}\right) \biggr)
```

(Remember we plug the top number in first, the bottom number in second, and then we subtract.)

````

``````


---


## Example 2
Integrate the following:

$$
\int_0^1 \tan^{-1}x \, dx
$$



``````{dropdown} Solution (Click to see the steps.)



`````{tabbed} Step 1
We're trying to integrate an inverse function, so it might be helpful to remember back to our trick on how we integrated $\ln x$. There, we rewrote the function as a product, and that's what we're going to do here as well:

$$ 
\left(\tan^{-1} x\right)\cdot 1
$$

So that we have the integral:

$$
\int_0^1 \left(\tan^{-1} x\right)\cdot 1 \cdot \, dx
$$

Now we're ready to choose $u$ and $dv$ by classifing the two parts of our function and remembering LIATE.

````{panels}
:column: col-sm
:card: border-2
**A** for Algebraic
^^^
```{math}
1
```
---
**I** for Inverse Trigonometric
^^^
```{math}
\tan^{-1} x
```
````

Since we have an algebraic part and an inverse trigonometric part, the algebraic part is our choice for $dv$ and the inverse trigonometric part is our choice for $u$.

````{panels}
:column: col-sm
:card: border-2
Our choice for $u$
^^^
```{math}
u=\tan^{-1} x
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
```{math}
u &=\tan^{-1} x \\
du &= \dfrac{1}{1+x^2}\cdot dx
```

---
Integrate
^^^
```{math}
dv &=1 \cdot dx \\
v &=x
```

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

**Our Pieces** 

````{panels}
```{math}
u &=\tan^{-1} x \\
du &= \dfrac{1}{1+x^2}\cdot dx
```

---

```{math}
dv &=1 \cdot dx \\
v &=x
```
````


Doing this we get:
```{math}

\int_0^1 \tan^{-1} x \,& dx = uv \biggr|_0^1 -\int_0^1 v \; du \\
&= \left(\tan^{-1} x\right)\cdot x \biggr|_0^1 -\int_0^1 x\cdot  \dfrac{1}{1+x^2} \; dx
```

`````

`````{tabbed} Step 4a
We're eventually going to finish integrating, but since this will require substitution rule, let's evaluate that first piece to get it out of the way.

```{math}
&= x\tan^{-1} x \biggr|_0^1 -\int_0^1 x\cdot  \dfrac{1}{1+x^2} \; dx\\
&= \left(1\cdot \tan^{-1} 1\right)-\left(0\cdot \tan^{-1} 0\right) -\int_0^1 x\cdot  \dfrac{1}{1+x^2} \; dx \\
&= \dfrac{\pi}{4} -\int_0^1 x\cdot  \dfrac{1}{1+x^2} \; dx 
```

(Since $\tan^{-1} 1 = \pi/4$).

`````

`````{tabbed} Step 4b
Now, to calculate this remaining integral:

```{math}
\int_0^1   \dfrac{1}{1+x^2} \cdot x \; dx
```

We are going to do a $u$-substitution with:

```{math}
u &= 1+x^2 \\
du &= 2x \cdot dx \longrightarrow \tfrac{1}{2}\cdot du = x dx

```

And converting the limits of integration gives us the integral:

```{math}
\int_0^1   \dfrac{1}{1+x^2} \cdot x \; dx = \int_1^2   \dfrac{1}{u} \cdot \dfrac{1}{2} \; du
```
Next we fnd the antiderivative and evaluate to get:
```{math}
\int_1^2   \dfrac{1}{u} \cdot \dfrac{1}{2} \; du &= \tfrac{1}{2}\ln|u|\biggr|_{u=1}^{u=2}\\
&= \tfrac{1}{2}\ln|2|-\tfrac{1}{2}\ln|1|\\
&= \tfrac{1}{2}\ln 2
```


`````

`````{tabbed} Step 4c
Now, put it altogether to get our answer:

```{math}
\int_0^1 \tan^{-1} x \, dx & = \dfrac{\pi}{4} -\int_0^1 x\cdot  \dfrac{1}{1+x^2} \; dx \\
&=\tfrac{\pi}{4} -\tfrac{1}{2}\ln 2
```


`````



``````