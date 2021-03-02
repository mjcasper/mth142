# (AI-6) Improper Integrals (p-forms)

In this lesson we are going to investigate the convergence and divergence of a specific class of improper integrals: the $p$-forms. We will be using these pretty extenstively when we talk about sequences and series.

By the end of this lesson, you will be able to determine whether a $p$-form improper integral is convergent or divergent, and if convergent, be able to evaluate the integral. 


---




## Convergence and Divergence


```{admonition} Improper Integrals ($p$-forms)
The convergence of the $p$-form improper integral depends on the value of $p$: 

$$
\int_1^{\infty} \dfrac{1}{x^p}\, dx
$$

Specifically, this improper integral is:
- convergent when $p>1$
- divergent when $p\leq 1$

```

### Antiderivative

The function in these integrals

$$
f(x)=\dfrac{1}{x^p}
$$ 

is a power function and in general there are two separate cases when we integrate a power function:

````{panels}
Case: $p=1$
^^^
Here the function can be written as:

$$
f(x)=\dfrac{1}{x}
$$ 

and the antiderivative is:

$$
F(x)=\ln |x|
$$

(where we *cannot* use power rule)

---

Case: $p\neq 1$
^^^
Here the function can be written as:

$$
f(x)=\dfrac{1}{x^p}=x^{-p}
$$ 

and the antiderivative is:

$$
F(x)=\tfrac{1}{-p+1}\cdot x^{-p+1}
$$

(where we use power rule)


````



### Proof 

We break the proof of this result into 3 cases:





``````{dropdown} **Case $p=1\qquad$** (Click to see the steps.)



`````{tabbed} Step 1
Since this is an improper integral over an infinite interval we begin by rewriting this integral as a limit:


$$
\int_1^{\infty} \dfrac{1}{x}\, dx = \lim_{b\to\infty} \int_1^{b}  \dfrac{1}{x}\, dx 
$$



`````

`````{tabbed} Step 2
Next we work on calculating the resulting definite integral:

$$
  & \lim_{b\to\infty} \int_1^{b}  \dfrac{1}{x}\, dx  \\[10pt]
= & \lim_{b\to\infty} \ln |x| \biggr|_{x=1}^{x=b} \\[10pt]
= & \lim_{b\to\infty} \bigg(\ln |b| -  \ln |1|\bigg)  \\[10pt]
= & \lim_{b\to\infty} \ln |b|   \\[10pt]
$$


`````

`````{tabbed} Step 3
Finally, we calculate the limit at infinity:

$$
\lim_{b\to\infty} \ln |b| =  \infty
$$

Why? This is one of our [important limits at infinity](improper-integrals.html#infinite-limits) that we should remember.



`````


`````{tabbed} Conclusion
We have shown that the improper integral

$$
\int_1^{\infty} \dfrac{1}{x}\, dx = \infty
$$

and is therefore **divergent.**

`````






``````







``````{dropdown} **Case $p>1\qquad$** (Click to see the steps.)



`````{tabbed} Step 1
Since this is an improper integral over an infinite interval we begin by rewriting this integral as a limit:


$$
\int_1^{\infty} \dfrac{1}{x^p}\, dx = \lim_{b\to\infty} \int_1^{b}  \dfrac{1}{x^p}\, dx 
$$



`````

`````{tabbed} Step 2
Next we work on calculating the resulting definite integral:

$$
  & \lim_{b\to\infty} \int_1^{b}  \dfrac{1}{x^p}\, dx  \\[10pt]
= & \lim_{b\to\infty} \tfrac{1}{-p+1}\cdot x^{-p+1} \biggr|_{x=1}^{x=b} \\[10pt]
= & \lim_{b\to\infty} \bigg(\tfrac{1}{-p+1}\cdot b^{-p+1}-\tfrac{1}{-p+1}\cdot 1^{-p+1}\bigg)  \\[10pt]
= & \lim_{b\to\infty} \tfrac{1}{-p+1}\left(b^{-p+1}-1\right)   \\[10pt]
$$


`````

`````{tabbed} Step 3
Finally, we need to calculate the limit at infinity:

$$
\lim_{b\to\infty} \tfrac{1}{-p+1}\left(b^{-p+1}-1\right)
$$

But before we do, we note that since $p>1$ for this case, we have :

$$
& 1 <p\\[10pt]
\longrightarrow\quad -p+& 1<0\\[10pt]
$$

So $-p+1$ is a negative number. To simplify some of the notation, let's rename this and say: $-p+1=-n$ where $n$ is some positive number. This would make:

$$
\lim_{b\to\infty} b^{-p+1} = \lim_{b\to\infty} b^{-n} = \lim_{b\to\infty} \dfrac{1}{b^n} = 0
$$

Using this result we get:

$$
\lim_{b\to\infty} \tfrac{1}{-p+1}\left(b^{-p+1}-1\right)= \tfrac{1}{-p+1}\left(0-1\right)= \tfrac{-1}{-p+1} = \tfrac{1}{p-1}\\[10pt]
$$


`````


`````{tabbed} Conclusion
We have shown that when $p>1$ the improper integral

$$
\int_1^{\infty} \dfrac{1}{x^p}\, dx = \tfrac{1}{p-1}
$$

and is therefore **convergent.**

`````






``````







``````{dropdown} **Case $p<1\qquad$** (Click to see the steps.)



`````{tabbed} Step 1
Same as step 1 for the case where $p>1$.



`````

`````{tabbed} Step 2
Same as step 2 for the case where $p>1$.


`````

`````{tabbed} Step 3
Finally, we need to calculate the limit at infinity:

$$
\lim_{b\to\infty} \tfrac{1}{-p+1}\left(b^{-p+1}-1\right)
$$

This is where things start to get different. Since $p<1$ for this case, we have :

$$
p<1 \quad \longrightarrow\quad 0<-p+1
$$

So $-p+1$ is a **positive number** in this case. To simplify some of the notation, let's rename this and say, $-p+1=m$ where $m$ is some positive number. This would make:

$$
\lim_{b\to\infty} b^{-p+1} = \lim_{b\to\infty} b^{m} = \infty
$$

Using this result we get:

$$
\lim_{b\to\infty} \tfrac{1}{-p+1}\left(b^{-p+1}-1\right)=\infty
$$


`````


`````{tabbed} Conclusion
We have shown that when $p<1$ the improper integral

$$
\int_1^{\infty} \dfrac{1}{x^p}\, dx = \infty
$$

and is therefore **divergent.**

`````






``````




















## Example 1
Determine if the following improper integral is convergent or divergent. 

$$
\int_1^{\infty} \dfrac{1}{x^2}\, dx 
$$





``````{dropdown} Solution (Click to see the steps.)

This is a $p$-form improper integral with $p=2$ which is greater than 1. 

This integral is therefore **convergent.**



``````



## Example 2
Determine if the following improper integral is convergent or divergent. 

$$
\int_1^{\infty} \dfrac{1}{\sqrt{x}}\, dx 
$$





``````{dropdown} Solution (Click to see the steps.)

This is a $p$-form improper integral with $p=\tfrac{1}{2}$ which is less than 1. 

This integral is therefore **divergent.**



``````


```{note}
We can relax the starting point of our integration and the general result is still true. For any number $a>0$, the improper integral

$$
\int_a^{\infty} \dfrac{1}{x^p}\, dx 
$$

is convergent when $p>1$ and divergent when $p\leq 1$.
```


## Example 3
Determine if the following improper integral is convergent or divergent. 

$$
\int_5^{\infty} \dfrac{1}{x}\, dx 
$$





``````{dropdown} Solution (Click to see the steps.)

This is a $p$-form improper integral with $p=1$. 

This integral is therefore **divergent.**



``````




