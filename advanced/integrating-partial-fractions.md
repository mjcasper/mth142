# (AI-4) Integrating with Partial Fractions

In this lesson we are going to see how partial fraction decompositions can help us integrate rational functions.



## Important Integrals

After going through the partial fraction decomposition process, we are going to frequently end up with the four types of integrals listed below. (All of these can be proved with a $u$-substitution.)

$$
&\int \dfrac{1}{kx+d} \, dx &= \tfrac{1}{k}\ln \left|kx+d\right| +C\\[10pt]
&\int \dfrac{1}{(kx+d)^n}\, dx \; &= \tfrac{1}{k}\left(\tfrac{1}{-n+1}(kx+d)^{-n+1} \right)+C \\[10pt]
&\int \dfrac{x}{x^2+a^2}\, dx &= \tfrac{1}{2}\ln \left|x^2+a^2\right| +C\\[10pt]
&\int \dfrac{1}{x^2+a^2}\, dx &= \tfrac{1}{a}\tan^{-1}\left(\dfrac{x}{a}\right) +C\\[10pt]
$$


## Example 1
Calculate the integral

$$
\int \dfrac{2x+5}{(x-1)(3x+4)}\, dx 
$$

``````{dropdown} Solution (Click to see the steps.)

Recall that we did the partial fraction decomposition of this rational function back in [AI-3 Example 2.](partial-fractions.html#example-2)

$$
\int \dfrac{2x+5}{(x-1)(3x+4)}\, dx &=\int \left(\dfrac{1}{x-1}-\dfrac{1}{3x+4}\right) \, dx\\[10pt]
&=\ln\left|x-1\right|-\tfrac{1}{3}\ln\left|3x+4\right| +C
$$


``````


## Example 2
Calculate the integral

$$
\int \dfrac{1}{x^2-25}\, dx 
$$

``````{dropdown} Solution (Click to see the steps.)

Recall that we did the partial fraction decomposition of this rational function back in [AI-3 Example 3.](partial-fractions.html#example-3)

$$
\int \dfrac{1}{x^2-25}\, dx &=\int \left(\dfrac{\tfrac{1}{10}}{x-5}-\dfrac{\tfrac{1}{10}}{x+5}\right) \, dx\\[10pt]
&=\tfrac{1}{10}\ln\left|x-5\right|-\tfrac{1}{10}\ln\left|x+5\right| +C
$$


``````


## Example 3
Calculate the integral

$$
\int \dfrac{2x^2-x+4}{x^3+4x}\, dx 
$$

``````{dropdown} Solution (Click to see the steps.)

Recall that we did the partial fraction decomposition of this rational function back in [AI-3 Example 4.](partial-fractions.html#example-4)

$$
\int \dfrac{2x^2-x+4}{x^3+4x}\, dx &=\int \left(\dfrac{1}{x}+\dfrac{x-1}{x^2+4}\right) \, dx\\[10pt]
&=\int \left(\dfrac{1}{x}+\dfrac{x}{x^2+4}-\dfrac{1}{x^2+4}\right) \, dx\\[10pt]
&=\ln\left|x\right|+\tfrac{1}{2}\ln\left|x^2+4\right| -\tfrac{1}{2}\tan^{-1}\left(\dfrac{x}{2}\right)+C
$$


Note that $\dfrac{1}{x^2+4}=\dfrac{1}{x^2+2^2}

``````



## Example 4
Calculate the integral

$$
\int \dfrac{x^4-2x^2+4x+1}{x^3-x^2-x+1}\, dx 
$$

``````{dropdown} Solution (Click to see the steps.)

Recall that we did the polynomial long division and partial fraction decomposition of this rational function back in [AI-3 Example 5.](partial-fractions.html#example-5)

$$
&=\int \left(x+ 1+ \dfrac{1}{x-1}+\dfrac{2}{(x-1)^2}-\dfrac{1}{x+1}\right) \, dx\\[10pt]
&=\tfrac{1}{2}x^2+x+\ln\left|x-1\right|+2\left(\tfrac{1}{-1}(x-1)^{-1}\right)-\ln\left|x+1\right| +C\\[10pt]
&=\tfrac{1}{2}x^2+x+\ln\left|x-1\right|-\dfrac{2}{x-1}-\ln\left|x+1\right| +C
$$


``````
## Irreducible Quadratics

We know how to integrate fractions involving irreducible quadratics of the form $(x^2+a^2)$ from our two important integrals:

$$
&\int \dfrac{x}{x^2+a^2}\, dx &= \tfrac{1}{2}\ln \left|x^2+a^2\right| +C\\[10pt]
&\int \dfrac{1}{x^2+a^2}\, dx &= \tfrac{1}{a}\tan^{-1}\left(\dfrac{x}{a}\right) +C\\[10pt]
$$

But how do we integrate an irreducible quadratic of the form $(ax^2+bx+c)$? **Completing the square!**

## Example 5

Calculate the integral

$$
\int \dfrac{x+3}{x^2+4x+13}\, dx 
$$


``````{dropdown} Solution (Click to see the steps.)



`````{tabbed} Step 1
We see that this is a rational function, so partial fractions might be one of our first thoughts. But if we were to try factoring the denominator we would see that the polynomial $(x^2+4x+13)$ is an irreducible quadratic (use the quadratic formula to check this).

This means the function as written is already in its partial fraction decomposition. So to integrate, we need to make the denominator look more like our usual irreducible quadratic form: $(x^2+a^2)$. And completing the square will help us  with this: 

$$
x^2+4x& &+13\\[10pt]
x^2+4x&+4-4 &+13\\[10pt]
(x^2+4x&+4)-4 &+13\\[10pt]
(x+&2)^2 &+9\\[10pt]
$$
 
This gives us the integral:

$$
\int \dfrac{x+3}{(x+2)^2 +9}\, dx 
$$



`````

`````{tabbed} Step 2
So far we have:

$$
\int \dfrac{x+3}{(x+2)^2 +9}\, dx 
$$


We still need to make our denominator look more like our usual irreducible quadratic form: $(x^2+a^2)$. We're getting closer, but still not quite there. If we do a $u$-substitution with:

$$
u&=x+2\\[10pt]
du&=dx\\[10pt]
$$ 

and noting that $u+1=x+3$, we get:


$$
\int \dfrac{u+1}{u^2 +9}\, du 
$$

This looks good! This is something we know how to integrate.

`````

`````{tabbed} Step 3
We can split this fraction up into 2 separate fractions and then integrate each fraction separately:

$$
\int \dfrac{u+1}{u^2 +9}\, du &= \int \left(\dfrac{u}{u^2 +9}+\dfrac{1}{u^2 +9}\right)\, du\\[10pt]
&= \tfrac{1}{2}\ln \left|u^2+9\right| + \tfrac{1}{3}\tan^{1}\left(\dfrac{u}{3}\right) +C \\[10pt]
$$

And finally convert back to our original variable $x$ with $u=x+2$.

$$
= \tfrac{1}{2}\ln \left|(x+2)^2+9\right| + \tfrac{1}{3}\tan^{1}\left(\dfrac{x+2}{3}\right) +C 
$$



`````


``````




## Rationalizing Substitutions

Integrating something with a root function? Try doing a $u$-substitution by letting $u$ equal the entire root function.

Sometimes this will rationalize the function enough where our partial fraction techniques becomes helpful!

## Example 6 
Calculate the integral

$$
\int \dfrac{1}{(4x-5)\sqrt{x-1}}\, dx 
$$




``````{dropdown} Solution (Click to see the steps.)



`````{tabbed} Step 1
We see that we have a root function that does not fit our usual trig substitution form: $\sqrt{x^2-a^2}$ (note that our function just has an $x$ but the trig sub format has an $x^2$.

We're going to try a rationalizing substitution by letting: 

$$
u=\sqrt{x-1}
$$

Now instead of calculating $du$ immediately, we're first going to try solving our $u$-equation for $x$

$$
u=\sqrt{x-1}\quad \longrightarrow\quad u^2=x-1 \quad \longrightarrow\quad x=u^2+1
$$

And then from here we calculate the differential $dx$ to get:

$$
dx = 2u\cdot du
$$

Now we can plug these 3 results into our integral to get: 


$$
\int \dfrac{1}{(4(u^2+1)-5)u}\cdot 2 u \, du 
$$



`````

`````{tabbed} Step 2
Simplifying we see that we now have a rational function to integrate:

$$
\int \dfrac{1}{(4(u^2+1)-5)u}\cdot 2 u \, du = \int \dfrac{2}{4u^2-1}\, du
$$


And the denominator does factor, so partial fractions will be applicable. So let's factor and write out the form of the partial fraction decomposition:

$$
\dfrac{2}{4u^2-1} =  \dfrac{2}{(2u-1)(2u+1)} = \dfrac{A}{2u-1}+\dfrac{B}{2u+1}
$$


`````

`````{tabbed} Step 3
Multiply both sides of the equation by the denominator on the left side and simplify:

$$
\dfrac{2}{(2u-1)(2u+1)} &= \dfrac{A}{2u-1}+\dfrac{B}{2u+1}\\[10pt]
2 &= \left(\dfrac{A}{2u-1}+\dfrac{B}{2u+1}\right)\cdot (2u-1)(2u+1)\\[10pt]
2 &= A (2u+1) + B (2u-1)\\[10pt]
$$



`````


`````{tabbed} Step 4
At this point, we need to solve for $A$ and $B$ in the equation:

$$
2 = A (2u+1) + B (2u-1)
$$


We see two linear terms on the right. Let's find the $u$-values that correspond with these terms:

$$
(2u+1) \quad \longrightarrow \quad u=-\tfrac{1}{2}
$$

$$
(2u-1) \quad \longrightarrow \quad u=\tfrac{1}{2}
$$


If we plug these $u$-values into our equation, it will greatly simplify it down to a point where we can solve for $A$ and $B$.

$$
&u=-\tfrac{1}{2} &\quad \longrightarrow \quad 2=A(-1+1)+{B}(-1-1) \\[10pt]
& & \quad \longrightarrow \quad 2=-2B \\[10pt]
& &\quad \longrightarrow \quad B=-1\\[20pt]
&u=\tfrac{1}{2} &\quad \longrightarrow \quad 2=A(1+1)+{B}(1-1) \\[10pt]
& & \quad \longrightarrow \quad 2=2A \\[10pt]
& &\quad \longrightarrow \quad A=1\\[20pt]
$$


`````


`````{tabbed} Step 5

We plug our values $A=1$ and $B=-1$ into the form of the partial fraction decomposition:

$$
\dfrac{A}{2u-1}+\dfrac{B}{2u+1} = \dfrac{1}{2u-1}-\dfrac{1}{2u+1}
$$

Using this result in our integral, gives us two $k$-form integrals:

$$
\int \dfrac{2}{4u^2-1}\, du &= \int \left( \dfrac{1}{2u-1}-\dfrac{1}{2u+1} \right)\, du\\[10pt]
&= \tfrac{1}{2} \ln \left|2u-1\right| - \tfrac{1}{2} \ln \left|2u+1\right| \\[10pt]
$$

And then finally, we started with $x$, we need to get back to $x$. Let's plug back in our original substitution $u=\sqrt{x-1}$.

$$
=\tfrac{1}{2} \ln \left|2\sqrt{x-1}-1\right| - \tfrac{1}{2} \ln \left|2\sqrt{x-1}+1\right| 
$$

`````


``````









