# (AI-3) Partial Fractions

In this lesson we are going to see how to use the technique of partial fractions to split a rational function up into simpler functions (which are ultimately easier to integrate). For example:

$$
\dfrac{2x+5}{(x-1)(3x+4)}=\dfrac{1}{x-1}-\dfrac{1}{3x+4}
$$

## Partial Fraction Decomposition

We start by factoring the denominator of our rational function and classifying the resulting factors. It is these factors in the denominator that tell us how to write out the form of our partial fraction decomposition.

| Term in Denominator | Description | Partial Fraction Decomposition |
|------------------|-----|------|----------------|
| $(ax+b)$ | linear term with multiplicity&nbsp;$1$   | $\dfrac{A}{ax+b}$ |
| $(ax+b)^n$ | linear term with multiplicity&nbsp;$n$ | $\dfrac{A_1}{ax+b}+\dfrac{A_2}{(ax+b)^2}+\cdots + \dfrac{A_n}{(ax+b)^n}$ |
| $(ax^2+bx+c)$ | irreducible quadratic with multiplicity&nbsp;$1$   | $\dfrac{Ax+B}{ax^2+bx+c}$ |
| $(ax^2+bx+c)^n$  | irreducible quadratic with multiplicity&nbsp;$n$  | $\dfrac{A_1x+B_1}{ax^2+bx+c}+\dfrac{A_2x+B_2}{(ax^2+bx+c)^2}+\cdots + \dfrac{A_nx+B_n}{(ax^2+bx+c)^n}$ |



## Example 1

For each function write out the **form of the partial fraction decomposition.** Do not determine the numerical values of the coefficients.

```{dropdown} $\dfrac{2x+5}{(x-1)(3x+4)}$
$$
\dfrac{A}{x-1}+\dfrac{B}{3x+4}
$$

```

```{dropdown} $\dfrac{3x^2}{(2x+1)(x+1)^3}$
$$
\dfrac{A}{2x+1}+\dfrac{B}{x+1}+\dfrac{C}{(x+1)^2}+\dfrac{D}{(x+1)^3}
$$

```

```{dropdown} $\dfrac{4x^3+5}{x^2(x^2+1)}$
$$
\dfrac{A}{x}+\dfrac{B}{x^2}+\dfrac{Cx+D}{x^2+1}
$$

```

```{dropdown} $\dfrac{x^2+12x+4}{(x-2)(4+x^2)^2}$


$$
\dfrac{A}{x-2}+\dfrac{Bx+C}{4+x^2}+\dfrac{Dx+E}{(4+x^2)^2}
$$

```

## Example 2
Show that:

$$
\dfrac{2x+5}{(x-1)(3x+4)}=\dfrac{1}{x-1}-\dfrac{1}{3x+4}
$$

``````{dropdown} Solution (Click to see the steps.)

`````{tabbed} Step 1
We start by writing down the partial fraction decomposition:

$$
\dfrac{2x+5}{(x-1)(3x+4)}=\dfrac{A}{x-1}+\dfrac{B}{3x+4}
$$
 
Where $A$ and $B$ are constants that we need to find.


`````

`````{tabbed} Step 2
Multiply both sides of the equation by the denominator on the left side and simplify:

$$
\dfrac{2x+5}{(x-1)(3x+4)}&=\dfrac{A}{x-1}+\dfrac{B}{3x+4}\\[10pt]
(x-1)(3x+4)\cdot \dfrac{2x+5}{(x-1)(3x+4)}&=\left(\dfrac{A}{x-1}+\dfrac{B}{3x+4}\right)\cdot (x-1)(3x+4)\\[10pt]
2x+5&=A(3x+4)+{B}(x-1)\\
$$
`````

`````{tabbed} Step 3
At this point, we need to solve for $A$ and $B$ in the equation:

$$
2x+5=A(3x+4)+{B}(x-1)
$$

We see two linear terms on the right. Let's find the $x$-values that correspond with these terms:

$$
(x-1) \quad \longrightarrow \quad x=1
$$

$$
(3x+4) \quad \longrightarrow \quad x=-\tfrac{4}{3}
$$


If we plug these $x$-values into our equation, it will greatly simplify it down to a point where we can solve for $A$ and $B$.

$$
&x=1 &\quad \longrightarrow \quad 2(1)+5=A(3(1)+4)+{B}(1-1) \\[10pt]
& & \quad \longrightarrow \quad 7=7A \\[10pt]
& &\quad \longrightarrow \quad A=1\\[20pt]
& x=-\tfrac{4}{3} &\quad \longrightarrow \quad  2\left(-\tfrac{4}{3}\right)+5=A\left(3\left(-\tfrac{4}{3}\right)+4\right)+{B}\left(-\tfrac{4}{3}-1\right) \\[10pt]
& & \quad \longrightarrow \quad \tfrac{7}{3}=-\tfrac{7}{3}B \\[10pt]
& & \quad \longrightarrow \quad B=-1
$$




`````

`````{tabbed} Step 4

And finally we plug our values $A=1$ and $B=-1$ into the form of the partial fractions decomposition.

$$
\dfrac{2x+5}{(x-1)(3x+4)}&=\dfrac{A}{x-1}+\dfrac{B}{3x+4}\\[10pt]
&=\dfrac{1}{x-1}-\dfrac{1}{3x+4}
$$
`````

``````


## Example 3
Find the partial fraction decomposition of the function

$$
\dfrac{1}{x^2-25}
$$

``````{dropdown} Solution (Click to see the steps.)

`````{tabbed} Step 1
We start by factoring the denominator and writing down the partial fraction decomposition:

$$
\dfrac{1}{x^2-25} &= \dfrac{1}{(x-5)(x+5)}\\[10pt]
&=\dfrac{A}{x-5}+\dfrac{B}{x+5}
$$
 
Where $A$ and $B$ are constants that we need to find.


`````

`````{tabbed} Step 2
Multiply both sides of the equation by the denominator on the left side and simplify:

$$
\dfrac{1}{(x-5)(x+5)}&=\dfrac{A}{x-5}+\dfrac{B}{x+5}\\[10pt]
(x-5)(x+5)\cdot \dfrac{1}{(x-5)(x+5)}&=\left(\dfrac{A}{x-5}+\dfrac{B}{x+5}\right)\cdot (x-5)(x+5)\\[10pt]
1&=A(x+5)+{B}(x-5)\\
$$
`````

`````{tabbed} Step 3
At this point, we need to solve for $A$ and $B$ in the equation:

$$
1=A(x+5)+{B}(x-5)
$$

We see two linear terms on the right. Let's find the $x$-values that correspond with these terms:

$$
(x+5) \quad \longrightarrow \quad x=-5
$$

$$
(x-5) \quad \longrightarrow \quad x=5
$$


If we plug these $x$-values into our equation, it will greatly simplify it down to a point where we can solve for $A$ and $B$.

$$
&x=-5 &\quad \longrightarrow \quad 1=A(-5+5)+{B}(-5-5) \\[10pt]
& & \quad \longrightarrow \quad 1=-10B \\[10pt]
& &\quad \longrightarrow \quad B=-\tfrac{1}{10}\\[20pt]
&x=5 &\quad \longrightarrow \quad 1=A(5+5)+{B}(5-5) \\[10pt]
& & \quad \longrightarrow \quad 1=10A \\[10pt]
& &\quad \longrightarrow \quad A=\tfrac{1}{10}
$$




`````

`````{tabbed} Step 4

And finally we plug our values $A=\tfrac{1}{10}$ and $B=-\tfrac{1}{10}$ into the form of the partial fraction decomposition to get our answer.

$$
\dfrac{1}{x^2-25} &=\dfrac{A}{x-5}+\dfrac{B}{x+5}\\[10pt]
&=\dfrac{\tfrac{1}{10}}{x-5}-\dfrac{\tfrac{1}{10}}{x+5}
$$
`````

``````








## Finding Coefficients

We have two main techniques for finding the partial fraction coefficients like $A$,&nbsp;$B$,&nbsp;$C$:

1. **Plug-in various $x$-values.** This especially works well when we have distinct linear terms, but can also be effective for the other cases. The idea is that you pick $x$-values which: 
    - correspond to the linear terms or are
    - just nice and easy like $x=1$, $x=0$, $x=-1$.
1. **Compare coefficients** of the various powers of $x$ in your simplified equation.
    - Identify terms like $x^0$, $x^1$, $x^2$ that show up in the equation.
    - Set the coefficients from the left side equal to the coefficients from the right.


And of course, you can use a **combination of these two strategies.**


```{admonition} Finding coefficients

1. Plug-in various $x$-values. 
1. Compare coefficients of the powers of $x$
```

In the next example, we're going to see how to compare coefficients.



## Example 4
Find the partial fraction decomposition of the function

$$
\dfrac{2x^2-x+4}{x^3+4x}
$$


``````{dropdown} Solution (Click to see the steps.)

`````{tabbed} Step 1
We start by factoring the denominator and writing down the partial fraction decomposition:

$$
\dfrac{2x^2-x+4}{x^3+4x} &= \dfrac{2x^2-x+4}{x(x^2+4)}\\[10pt]
&=\dfrac{A}{x}+\dfrac{Bx+C}{x^2+4}
$$
 
Where $(x^2+4)$ is an irreducible quadratic and $A$, $B$, $C$ are constants that we need to find.


`````

`````{tabbed} Step 2
Multiply both sides of the equation by the denominator on the left side and simplify:

$$
\dfrac{2x^2-x+4}{x(x^2+4)}&=\dfrac{A}{x}+\dfrac{Bx+C}{x^2+4}\\[10pt]
x(x^2+4)\cdot \dfrac{2x^2-x+4}{x(x^2+4)}&=\left(\dfrac{A}{x}+\dfrac{Bx+C}{x^2+4}\right)\cdot x(x^2+4)\\[10pt]
2x^2-x+4&=A(x^2+4)+(Bx+C)x
$$
`````

`````{tabbed} Step 3
At this point, we need to solve for $A$, $B$, and $C$ in the equation:

$$
2x^2-x+4=A(x^2+4)+(Bx+C)x
$$

We could use the technique of plugging in various $x$-values, but in this example we're going to compare the coefficients of the powers of $x$. To do this, let's multiply everything out:

$$
2x^2-x+4=Ax^2+4A+Bx^2+Cx
$$

And combine like terms to get:

$$
2x^2-x+4=(A+B)x^2+Cx+4A
$$

Now we compare coefficients between the powers of $x$ on the left side of this equation and those on the right. (If two polynomails with variable $x$ are equal then their coefficients must also be equal.)

```{panels}
$x^2$ terms
^^^

$$
2=A+B
$$

---
$x^1$ terms
^^^

$$
-1=C
$$

---

$x^0$ terms
^^^

$$
4=4A
$$

```

We can solve that last equation for $A$ to get: $A=1$. Then we can plug this into the first equation: $2=A+B$ to find that $B=1$

This gives us: $A=1$, $B=1$, $C=-1$


`````

`````{tabbed} Step 4

And finally we plug our values $A=1$, $B=1$, and $C=-1$ into the form of the partial fraction decomposition to get our answer.

$$
\dfrac{2x^2-x+4}{x^3+4x} &=\dfrac{A}{x}+\dfrac{Bx+C}{x^2+4}\\[10pt]
&=\dfrac{1}{x}+\dfrac{x-1}{x^2+4}
$$
`````

``````


## Factoring

So what makes all this work? Why factoring of course! The **Fundamental Theorem of Algebra** asserts that every polynomial with real number coefficients can be factored into either linear or irreducible quadratic terms of the form:

| multiplicity | linear | irreducible quadratic |
|:-:|--------|-----------------------|
| $1$ | $ax+b$ | $(ax^2+bx+c)$         |
| repeated | $(ax+b)^n$ | $(ax^2+bx+c)^n$   |

(where $a$, $b$, and $c$ are real numbers)


### Irreducible Quadratics

There are quadratic expressions like $(x^2+4)$ or $(3x^2+x+2)$ that cannot be factored any further into products of linear terms (factored with real number coefficients). 

Why is this? Unfortunately, the real numbers are just not "enough." We need more. We need complex numbers. But this is a calculus course and we're only working with real numbers. So irreducible quadratics it is!

### Checking Irreducibility 

How do we know if a quadratic is irreducible? Try setting it equal to&nbsp;$0$ and solving for $x$. Is there a solution? Can it ever equal&nbsp;0?

```{dropdown} Why is $(x^2+4)$ irreducible?

Does $(x^2+4)$ factor any further? If it could, then we would be able to write it in the form $(x+a)(x+b)$, which means that it has at least one real root. 

But $x^2+4$ is always greater than $0$, which means it **cannot equal** $0$, and therefore does not have any real roots. So no, $(x^2+4)$ cannot be factored any further and is therefore irreducible.

```

```{dropdown} Show that $(3x^2+x+2)$ is irreducible using the **quadratic formula**.
Once we apply the quadratic fomula, the **negative under the square root** means the quadratic polynomial is irreducible:

$$
x=\dfrac{-b\pm \sqrt{b^2-4ac}}{2a}\quad \longrightarrow \quad x&=\dfrac{-1\pm \sqrt{1^2-4(3)(2)}}{2(3)}\\[10pt]
&=\dfrac{-1\pm \sqrt{-23}}{6}
$$
```


## Rational Functions


One technical point that we haven't mentioned so far, is that partial fraction decompositions do not immediately work for all rational functions. So to address this we make a few definitions:

````{admonition} Rational Functions

A rational function is a function of the form: 
```{math}
\dfrac{P(x)}{Q(x)}
```

where $P$ and $Q$ are polynomials with real number coefficients.

````




### Degrees

We then go on to define the degree of a polynomial:

```{admonition} Degree of a polynomial
The degree of a polynomial is the largest power of $x$.
```

The reason for this definition is that partial fraction decompositions only work if the degree of the polynomial in the numerator is less than the degree of the polynomial in the denominator. 


```{warning}
Partial Fraction Decompositions only work for rational functions where $\text{deg}(P)<\text{deg}(Q)$
```

### Polynomial Long-Division

If $\text{deg}(P)\geq \text{deg}(Q)$, that is the degree of the numerator is greater than or equal to the degree in the denominator, then we need to use polynomial long-division first.


```{dropdown} Use polynomial long-division to rewrite: $\dfrac{x^4-2x^2+4x+1}{x^3-x^2-x+1}$ 


```





## Example 5
Find the partial fraction decomposition of the function

$$
\dfrac{x^4-2x^2+4x+1}{x^3-x^2-x+1}
$$


``````{dropdown} Solution (Click to see the steps.)

`````{tabbed} Step 0
We start by doing polynomial long-division in order to get the degree of the numerator **less than** the degree of the denominator. We repeat our above result here:

$$
\dfrac{x4-2x^2+4x+1}{x^3-x^2-x+1} = x+1+\dfrac{4x}{x^3-x^2-x+1}
$$
 



`````



`````{tabbed} Step 1
Now we can focus on the remainder term of our rational function and work on its partial fraction decomposition. This means factor the denominator and write down the form of the  decomposition:

$$
\dfrac{4x}{x^3-x^2-x+1} &= \dfrac{4x}{(x-1)^2(x+1)}\\[10pt]
&=\dfrac{A}{x-1}+\dfrac{B}{(x-1)^2}+\dfrac{C}{x+1}
$$
 
Where $A$, $B$, and $C$ are constants that we need to find.


`````

`````{tabbed} Step 2
Multiply both sides of the equation by the denominator on the left side and simplify:

$$
\dfrac{4x}{(x-1)^2(x+1)}&=\dfrac{A}{x-1}+\dfrac{B}{(x-1)^2}+\dfrac{C}{x+1}\\[10pt]
(x-1)^2(x+1)\cdot \dfrac{4x}{(x-1)^2(x+1)}&=\left(\dfrac{A}{x-1}+\dfrac{B}{(x-1)^2}+\dfrac{C}{x+1}\right)\cdot (x-1)^2(x+1)\\[10pt]
4x &=A(x-1)(x+1)+B(x+1)+C(x-1)^2
$$
`````

`````{tabbed} Step 3
At this point, we need to solve for $A$, $B$, and $C$ in the equation:

$$
4x =A(x-1)(x+1)+B(x+1)+C(x-1)^2
$$

Here we're going to use a combination of our two techniques. 

**Plug-in:** Let's start by plugging in $x=1$ and $x=-1$, since these correspond to our two linear terms $(x-1)$ and $(x+1)$, respectively.


$$
&x= 1 &\quad \longrightarrow \quad 4(1)=A(0)(2)+{B}(2)+C(0)^2 \\[10pt]
& & \quad \longrightarrow \quad 4=2B \\[10pt]
& &\quad \longrightarrow \quad B=2\\[20pt]
&x=-1 &\quad \longrightarrow \quad 4(-1)=A(-2)(0)+{B}(0)+C(-2)^2 \\[10pt]
& & \quad \longrightarrow \quad -4=4C \\[10pt]
& &\quad \longrightarrow \quad C=-1
$$

**Compare coefficients:** We could keep going and plug in another $x$-value (something easy like $x=0$). But instead let's try comparing coefficients, and in particular the coefficients of all $x^2$ terms:

$$
4x =A(x-1)(x+1)+B(x+1)+C(x-1)^2
$$

- There is no $x^2$ term on the left side, so this means the coefficient is $0$.
- On the right side, we're only going to get an $x^2$ when we multiply out the $A(x-1)(x+1)$ and the $C(x-1)^2$. This means the coefficient of $x^2$ on the right is $A+C$

Putting these together gives us:

$$
0=A+C
$$

And since we already know $C=-1$, we get $A=1$. Therefore, we have: $A=1$, $B=2$, $C=-1$



`````

`````{tabbed} Step 4

We plug our values $A=1$, $B=2$, and $C=-1$ into the form of the partial fraction decomposition.

$$
\dfrac{4x}{x^3-x^2-x+1} &= \dfrac{A}{x-1}+\dfrac{B}{(x-1)^2}+\dfrac{C}{x+1}\\[10pt]
&=\dfrac{1}{x-1}+\dfrac{2}{(x-1)^2}-\dfrac{1}{x+1}
$$

And then finally we put this together with our result from the polynomial long-division:


$$
\dfrac{x^4-2x^2+4x+1}{x^3-x^2-x+1} = x+ 1+ \dfrac{1}{x-1}+\dfrac{2}{(x-1)^2}-\dfrac{1}{x+1}
$$


`````

``````

## Summary

We end by summarizing the steps needed to complete the partial fraction decomposition of a rational function.

```{admonition} Partial Fraction Decomposition
1. Use polynomial long division if necessary. We need $\text{deg}(P)<\text{deg}(Q)$.
2. Factor the denominator $Q(x)$.
3. Break the fraction apart based on the multiplicity of the linear and irreducible quadratic terms in the denominator.
4. Solve for the coefficients $A$, $B$, $C$, ...
```

The hardest part of all of this in general is factoring the denominator. A few extra tips:
- The **quadratic formula** can be used to help determine factors. If $x=2$ is a solution, then $(x-2)$ is a factor.
- Look for **"easy solutions"** like $x=1$, $x=0$, $x=-1$, and then use polynomial long-division to find the remainder.



