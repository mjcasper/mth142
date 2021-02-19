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

<!--

## Example 3
Find the partial fraction decomposition of the function

$$
\dfrac{x^2+3x-5}{3x^3+5x^2-2x}
$$


## Rational Functions

A rational function is a function of the form: 

$$
\dfrac{P(x)}{Q(x)}
$$

where $P$ and $Q$ are polynomials with variable $x$ and real number coefficients.


## Factoring

Get ready for some factoring! The **Fundamental Theorem of Algebra** asserts that every polynomial with real number coefficients can be factored into terms of the form:

| multiplicity | linear | irreducible quadratic |
|:-:|--------|-----------------------|
| $1$ | $ax+b$ | $(ax^2+bx+c)$         |
| repeated | $(ax+b)^n$ | $(ax^2+bx+c)^n$   |

(where $a$, $b$, and $c$ are real numbers)


### Irreducible Quadratics

There are quadratic expressions like $(x^2+4)$ or $(x^2+x+1)$ that cannot be factored any further into products of linear terms (factored with real number coefficients). 

Why is this? Unfortunately, the real numbers are just not "enough." We need more. We need complex numbers. But this is a calculus course and we're only working with real numbers. So irreducible quadratics it is!

### Checking Irreducibility 

How do we know if a quadratic is irreducible? Try setting it equal to&nbsp;$0$ and solving for $x$. Is there a solution? Can it ever equal&nbsp;0?

Let's try using the **quadratic formula** to check if $3x^2+x+2$ is irreducible.

$$
x=\dfrac{-b\pm \sqrt{b^2-4ac}}{2a}\quad \longrightarrow \quad x&=\dfrac{-1\pm \sqrt{1^2-4(3)(2)}}{2(3)}\\[10pt]
&=\dfrac{-1\pm \sqrt{-23}}{6}
$$

**The negative under the square root means the quadratic polynomial is irreducible.**




## Trig Substitutions

We identify which trigonometric substitution to use, based on the square root term that shows up in our integral. There are generally three cases we consider:

| Term in Denominator | Choice for $x$ | Partial Fraction Decomposition |
|------------------|-----|------|----------------|
| $(ax+b)$ | linear term with multiplicity&nbsp;$1$   | $\dfrac{A}{ax+b}$ |
| $(ax+b)^n$ | linear term with multiplicity&nbsp;$n$ | $\dfrac{A_1}{ax+b}+\dfrac{A_2}{(ax+b)^2}+\cdots + \dfrac{A_n}{(ax+b)^n}$ |
| $(ax^2+bx+c)$ | irreducible quadratic with multiplicity&nbsp;$1$   | $\dfrac{Ax+B}{ax^2+bx+c}$ |
| $(ax^2+bx+c)^n$  | irreducible quadratic with multiplicity&nbsp;$n$  | $\dfrac{A_1x+B_1}{ax^2+bx+c}+\dfrac{A_2x+B_2}{(ax^2+bx+c)^2}+\cdots + \dfrac{A_nx+B_n}{(ax^2+bx+c)^n}$ |




-->
