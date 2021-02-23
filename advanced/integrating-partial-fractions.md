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
















