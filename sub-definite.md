# Substitution Rule for Definite Integrals

## Two Methods
Essentially there are two methods when calculating definite integrals using substitution rule, and they both center around how we handle the limits of integration:


````{panels}
:column: col-sm
:card: border-2
Method 1
^^^
**Change the limits** of integration from $x$ to $u$.


When you go through the integration, you do **not** need to convert the antiderivative back to $x$. You can leave it in terms of $u$, and then go right to evaluating.
---
Method 2
^^^
**Do not change the limits.** Keep them in terms of $x$.


When you go through the integration here, you do need to go a little bit further and convert the antiderivative back to the original variable $x$.
````

## Example 1

Evaluate the following integral:

$$
\int_0^1 2x(x^2+1)^5 \;dx
$$


```{dropdown} **Question:** What do <em>you</em> think we should pick for $u$ in this example?
**Answer:** Could we try $u=x^2+1$?
```







### Method 1

Let's calculate this by **converting the limits of integration.**

````{tabbed} Solution
Click through the steps to see what we do.

If you want, give it a try first! 
````



````{tabbed} Step 1a
We choose $u$ to be what's inside the parentheses:

```{math}
u=x^2+1
```

And then calculate $du$
```{math}
du=\big[x^2+1\big]' dx \longrightarrow du = 2x\cdot dx
```

````

`````{tabbed} Step 1b
Next, we need to compare:
````{panels}
:column: col-sm
:card: border-2
Our calculated $du$
^^^
```{math}
du = 2x\cdot dx
```
---
Leftovers in the Integral
^^^
```{math}
2x\cdot dx
```
````

This is a perfect match, so no other work is needed here.

`````

`````{tabbed} Step 1c
Next, let's convert the limits of integration
- **Upper limit:** $x=1 \longrightarrow u=(1)^2+1 \longrightarrow u=2$
- **Lower limit:** $x=0 \longrightarrow u=(0)^2+1 \longrightarrow u=1$

`````


````{tabbed} Step 2
Now we're ready to substitute our $u$ and $du$ and new limits of integration into the original integral:

```{math}
\int_0^1 (x^2+1)^5 \cdot 2x\;dx = \int_{1}^{2} u^{5} \; du
```

````

````{tabbed} Step 3
We do a little power rule:

```{math}
\int_{1}^{2} u^{5} \; du= \frac{1}{6} u^{6}\biggr\rvert_{u=1}^{u=2}
```

````

````{tabbed} Step 4
And then finally we evaluate:


```{math} 
\frac{1}{6} u^{6}\biggr\rvert_{u=1}^{u=2}= \left(\dfrac{1}{6}\cdot 2^6\right)-\left(\dfrac{1}{6}\cdot 1^6\right)
```

(Remember that the top number goes in first, bottom number goes in second, and we subtract.)
````


### Method 2

Now let's try this example again but this time **leave our limits of integration in terms of $x$.**

````{tabbed} Solution
Click through the steps to see what we do.

If you want, give it a try first! 
````



````{tabbed} Step 1a
We choose $u$ to be what's inside the parentheses:

```{math}
u=x^2+1
```

And then calculate $du$
```{math}
du=\big[x^2+1\big]' dx \longrightarrow du = 2x\cdot dx
```

````

`````{tabbed} Step 1b
Next, we need to compare:
````{panels}
:column: col-sm
:card: border-2
Our calculated $du$
^^^
```{math}
du = 2x\cdot dx
```
---
Leftovers in the Integral
^^^
```{math}
2x\cdot dx
```
````

This is a perfect match, so no other work is needed here.

`````

````{tabbed} Step 2
Now we're ready to substitute our $u$ and $du$ into the original integral:

```{math}
\int_0^1 (x^2+1)^5 \cdot 2x\;dx = \int_{x=0}^{x=1} u^{5} \; du
```

````

````{tabbed} Step 3
We do a little power rule:

```{math}
\int_{x=0}^{x=1} u^{5} \; du= \frac{1}{6} u^{6}\biggr\rvert_{x=0}^{x=1}
```

````

````{tabbed} Step 4
Convert the antiderivative back to $x$

```{math}
\frac{1}{6} u^{6}\biggr\rvert_{x=0}^{x=1} = \frac{1}{6} (x^2+1)^{6}\biggr\rvert_{x=0}^{x=1}
```

````


````{tabbed} Step 5
And then finally we evaluate:


```{math} 
\frac{1}{6} (x^2+1)^{6}\biggr\rvert_{x=0}^{x=1}= \left(\frac{1}{6} (1^2+1)^{6}\right)-\left(\frac{1}{6} (0^2+1)^{6}\right)
```

(Remember that the top number goes in first, bottom number goes in second, and we subtract.)
````



## Example 2

Evaluate the integral.

$$
\int_1^2 \dfrac{dx}{(3-5x)^2} 
$$

```{dropdown} **Question:** What do <em>you</em> think we should pick for $u$ in this example?
**Answer:** How about $u=3-5x$?
```



### Method 1

Let's try calculating this by **converting the limits of integration.**

````{tabbed} Solution
Click through the steps to see what we do.

If you want, give it a try first! 
````

````{tabbed} Step 0
We start by rewriting this fraction with a **negative exponent.**
```{math}
\int_1^2 \dfrac{dx}{(3-5x)^2} = \int_1^2 (3-5x)^{-2} \; dx
```


(This just helps us later on, if we have to use the power rule.)

````


````{tabbed} Step 1a
We choose $u$ to be what's inside the parentheses:

```{math}
u=3-5x
```

And then calculate $du$
```{math}
du=\big[3-5x\big]' dx \longrightarrow du = -5\cdot dx
```

````

`````{tabbed} Step 1b
Next, we need to compare:
````{panels}
:column: col-sm
:card: border-2
Our calculated $du$
^^^
```{math}
du = -5\cdot dx
```
---
Leftovers in the Integral
^^^
```{math}
dx
```
````

Solving for the term(s) that shows up in both of these gives us:

```{math}
du = -5\cdot dx \longrightarrow \tfrac{-1}{5}\cdot du = dx
```

`````

`````{tabbed} Step 1c
Next, let's convert the limits of integration
- **Upper limit:** $x=2 \longrightarrow u=3-5(2) \longrightarrow u=-7$
- **Lower limit:** $x=1 \longrightarrow u=3-5(1) \longrightarrow u=-2$

`````


````{tabbed} Step 2
Now we're ready to substitute our $u$ and $\tfrac{-1}{5}\cdot du$ and new limits of integration into the original integral:

```{math}
\int_1^2 (3-5x)^{-2} \; dx = \int_{-2}^{-7} u^{-2} \cdot \frac{-1}{5}\; du
```

````

````{tabbed} Step 3
This gives us one of our basic integrals, which we can just do:

```{math}
\frac{-1}{5} \int_{-2}^{-7} u^{-2}  \; du = \frac{1}{5} u^{-1}\biggr\rvert_{u=-2}^{u=-7}
```

````

````{tabbed} Step 4
And then finally we evaluate:


```{math} 
\frac{1}{5u} \biggr\rvert_{u=-2}^{u=-7} = \left(\dfrac{1}{-35}\right)-\left(\dfrac{1}{-10}\right)
```

(Remember that the top number goes in first, bottom number goes in second, and we subtract.)
````

### Method 2

Now let's give the other method a go, where we **leave our limits of integration in terms of $x$.**

````{tabbed} Solution
Click through the steps to see what we do.

If you want, give it a try first! 
````

````{tabbed} Step 0
We start by rewriting this fraction with a **negative exponent.**
```{math}
\int_1^2 \dfrac{dx}{(3-5x)^2} = \int_1^2 (3-5x)^{-2} \; dx
```


(This just helps us later on, if we have to use the power rule.)

````


````{tabbed} Step 1a
We choose $u$ to be what's inside the parentheses:

```{math}
u=3-5x
```

And then calculate $du$
```{math}
du=\big[3-5x\big]' dx \longrightarrow du = -5\cdot dx
```

````

`````{tabbed} Step 1b
Next, we need to compare:
````{panels}
:column: col-sm
:card: border-2
Our calculated $du$
^^^
```{math}
du = -5\cdot dx
```
---
Leftovers in the Integral
^^^
```{math}
dx
```
````

Solving for the term(s) that shows up in both of these gives us:

```{math}
du = -5\cdot dx \longrightarrow \tfrac{-1}{5}\cdot du = dx
```

`````


````{tabbed} Step 2
Now we're ready to substitute our $u$ and $\tfrac{-1}{5}\cdot du$ into the original integral:

```{math}
\int_1^2 (3-5x)^{-2} \; dx = \int_{x=1}^{x=2} u^{-2} \cdot \frac{-1}{5}\; du
```
Since we are not converting the limits, we should write them in the form $x=\cdots$

````

````{tabbed} Step 3
This gives us one of our basic integrals, which we can just do:

```{math}
\frac{-1}{5} \int_{x=1}^{x=2} u^{-2}  \; du = \frac{1}{5} u^{-1}\biggr\rvert_{x=1}^{x=2}
```

````

````{tabbed} Step 4
And then we convert our antiderivative back to $x$:


```{math} 
\frac{1}{5u} \biggr\rvert_{x=1}^{x=2}= \frac{1}{5(3-5x)} \biggr\rvert_{x=1}^{x=2}

```
````

````{tabbed} Step 5
Now we can evaluate:


```{math} 
\frac{1}{5(3-5x)} \biggr\rvert_{x=1}^{x=2}= \left(\dfrac{1}{5(-7)}\right)-\left(\dfrac{1}{5(-2)}\right)
```
(Remember that the top number goes in first, bottom number goes in second, and we subtract.)

````







## Example 3


Evaluate the integral.

$$
\int_0^4 \dfrac{x}{\sqrt{2x+1}} \; dx
$$

```{dropdown} **Question:** What do <em>you</em> think we should pick for $u$ in this example?
**Answer:** Maybe give $u=2x+1$ a try?
```

### Method 1

````{tabbed} Solution
Click through the steps to see what we do.

If you want, give it a try first! 
````


````{tabbed} Step 0
We start by rewriting this **root function** as a power function:
```{math}
\int_0^4 \dfrac{x}{\sqrt{2x+1}} \; dx = \int_0^4 x(2x+1)^{-1/2} \; dx
```


(This just helps us later on, if we have to use the power rule.)

````

````{tabbed} Step 1a
Since the more complicated piece of our function is $(2x+1)^{-1/2}$, we choose $u$ to be the inner function:

```{math}
u=2x+1
```

And then calculate $du$
```{math}
du=\big[2x+1\big]' dx \longrightarrow du = 2\cdot dx
```

````

`````{tabbed} Step 1b
Next, we need to compare:
````{panels}
:column: col-sm
:card: border-2
Our calculated $du$
^^^
```{math}
du = 2\cdot dx
```
---
Leftovers in the Integral
^^^
```{math}
x\cdot dx
```
````

Since $dx$ is the only term that shows up in both, we solve for $dx$:

```{math}
du = 2\cdot dx \longrightarrow \tfrac{1}{2}\cdot du = dx
```

`````


`````{tabbed} Step 1c
Next, let's convert the limits of integration
- **Upper limit:** $x=4 \longrightarrow u=2(4)+1 \longrightarrow u=9$
- **Lower limit:** $x=0 \longrightarrow u=2(0)+1 \longrightarrow u=1$

`````


````{tabbed} Step 2
Now we're ready to substitute our $u$ and $\frac{1}{2}du$ and new limits of integration into the original integral:

```{math}
\int_0^4 (2x+1)^{-1/2} \cdot x\; dx = \int_1^9 u^{-1/2} \cdot x \cdot \tfrac{1}{2}\;  du 
```

But... we can't go any further yet since we still have some $x$-terms that we haven't gotten rid of yet. So we turn to our "solve for $x$ strategy."



$$
u=2x+1\longrightarrow x=\dfrac{u-1}{2}
$$

And then we plug this in for $x$:

```{math}
\int_1^9 u^{-1/2} \cdot x \cdot \tfrac{1}{2}\;  du = \int_1^9 u^{-1/2} \cdot \dfrac{u-1}{2} \cdot \tfrac{1}{2}\;  du 
```

````

````{tabbed} Step 3
This gives us a basic integral, which can be solved by multiplying out the integrand and then using power rule:

```{math}
\begin{split}
\dfrac{1}{4}\int_1^9 u^{-1/2} \cdot (u-1)\;  du  &= \dfrac{1}{4} \cdot \int_1^9 u^{1/2}-u^{-1/2} \; du \\
& = \dfrac{1}{4}\cdot \left( \dfrac{2}{3}u^{3/2}-2u^{1/2}\right)\biggr\rvert_{u=1}^{u=9}
\end{split}
```

````

````{tabbed} Step 4
And then evaluate!


```{math} 
\tfrac{1}{6}u^{3/2}-\tfrac{1}{2}u^{1/2}\biggr\rvert_{u=1}^{u=9} = \bigg(\tfrac{1}{6}\cdot 9^{3/2}-\tfrac{1}{2}\cdot 9^{1/2}\bigg)- \bigg(\tfrac{1}{6}\cdot 1^{3/2}-\tfrac{1}{2}\cdot 1^{1/2}\bigg)
```

Simplify as desired!
````



### Method 2

````{tabbed} Solution
Click through the steps to see what we do.

If you want, give it a try first! 
````


````{tabbed} Step 0
We start by rewriting this **root function** as a power function:
```{math}
\int_0^4 \dfrac{x}{\sqrt{2x+1}} \; dx = \int_0^4 x(2x+1)^{-1/2} \; dx
```


(This just helps us later on, if we have to use the power rule.)

````

````{tabbed} Step 1a
Since the more complicated piece of our function is $(2x+1)^{-1/2}$, we choose $u$ to be the inner function:

```{math}
u=2x+1
```

And then calculate $du$
```{math}
du=\big[2x+1\big]' dx \longrightarrow du = 2\cdot dx
```

````

`````{tabbed} Step 1b
Next, we need to compare:
````{panels}
:column: col-sm
:card: border-2
Our calculated $du$
^^^
```{math}
du = 2\cdot dx
```
---
Leftovers in the Integral
^^^
```{math}
x\cdot dx
```
````

Since $dx$ is the only term that shows up in both, we solve for $dx$:

```{math}
du = 2\cdot dx \longrightarrow \tfrac{1}{2}\cdot du = dx
```

`````


````{tabbed} Step 2
Now we're ready to substitute our $u$ and $\frac{1}{2}du$ into the original integral:

```{math}
\int_0^4 (2x+1)^{-1/2} \cdot x\; dx = \int_{x=0}^{x=4} u^{-1/2} \cdot x \cdot \tfrac{1}{2}\;  du 
```

But... we can't go any further yet since we still have some $x$-terms that we haven't gotten rid of yet. So we turn to our "solve for $x$ strategy."



$$
u=2x+1\longrightarrow x=\dfrac{u-1}{2}
$$

And then we plug this in for $x$:

```{math}
\int_{x=0}^{x=4} u^{-1/2} \cdot x \cdot \tfrac{1}{2}\;  du = \int_{x=0}^{x=4} u^{-1/2} \cdot \dfrac{u-1}{2} \cdot \tfrac{1}{2}\;  du 
```

````

````{tabbed} Step 3
This gives us a basic integral, which can be solved by multiplying out the integrand and then using power rule:

```{math}
\begin{split}
\dfrac{1}{4}\int_{x=0}^{x=4} u^{-1/2} \cdot (u-1)\;  du  &= \dfrac{1}{4} \cdot \int_{x=0}^{x=4} u^{1/2}-u^{-1/2} \; du \\
& = \dfrac{1}{4}\cdot \left( \dfrac{2}{3}u^{3/2}-2u^{1/2}\right)\biggr\rvert_{x=0}^{x=4}
\end{split}
```

````

````{tabbed} Step 4
Convert the antiderivative back to $x$


```{math} 
\dfrac{1}{6}u^{3/2}-\dfrac{1}{2}u^{1/2}\biggr\rvert_{x=0}^{x=4} = \dfrac{1}{6}\cdot (2x+1)^{3/2}-\dfrac{1}{2}\cdot (2x+1)^{1/2}\biggr\rvert_{x=0}^{x=4}
```
````

````{tabbed} Step 5
And then evaluate!


```{math} 
\begin{split}
\tfrac{1}{6}\cdot (2x+1)^{3/2} &-\tfrac{1}{2}\cdot (2x+1)^{1/2}\biggr\rvert_{x=0}^{x=4} \\
& = \bigg(\tfrac{1}{6}\cdot 9^{3/2}-\tfrac{1}{2}\cdot 9^{1/2}\bigg)- \bigg(\tfrac{1}{6}\cdot 1^{3/2}-\tfrac{1}{2}\cdot 1^{1/2}\bigg)
\end{split}
```

Simplify as desired!
````
