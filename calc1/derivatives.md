Differentiation
============================


## Elementary Forms

### Trigonometric Functions

```{math}
 &\dfrac{d}{dx}\big[\sin x\big] = \cos x &  & \dfrac{d}{dx}\big[\cos x\big] = -\sin x \\ 
 &\dfrac{d}{dx}\big[\sec x\big] = \sec x \tan x \qquad &  & \dfrac{d}{dx}\big[\csc x\big] = -\csc x \cot x\\ 
 &\dfrac{d}{dx}\big[\tan x\big] = \sec^2 x &  & \dfrac{d}{dx}\big[\cot x\big] = -\csc^2 x \\  
```

---

### Inverse Trigonometric Functions
```{math}
 &\dfrac{d}{dx}\big[\sin^{-1} x\big] = \dfrac{1}{\sqrt{1-x^2}} \qquad &  & \dfrac{d}{dx}\big[\cos^{-1} x\big] = -\dfrac{1}{\sqrt{1-x^2}} \\ 
 &\dfrac{d}{dx}\big[\tan^{-1} x\big] = \dfrac{1}{1+x^2} &  &  \\  
```

---
### Exponential and Logarithmic Functions

```{math}
 &\dfrac{d}{dx}\big[e^x\big] = e^x &  & \dfrac{d}{dx}\big[\ln x\big] = \dfrac{1}{x} \\ 
 &\dfrac{d}{dx}\big[b^x\big] = b^x \ln b \qquad &  & \dfrac{d}{dx}\big[\ln \lvert x\rvert \big] = \dfrac{1}{x} \\ 
 & &  & \dfrac{d}{dx}\big[\log_b x\big] = \dfrac{1}{x\ln b} \\  
```

---

## Power Rule

````{admonition} Power Rule
For real number $n$
```{math}
\dfrac{d}{dx}\big[ x^n \big] = n x^{n-1}
```
````

## Algebraic Rules

$$
\dfrac{d}{dx}\big[f(x)+g(x)\big] = f'(x)+g'(x)
$$ 

$$
\dfrac{d}{dx}\big[f(x)-g(x)\big] = f'(x)-g'(x)
$$ 

$$
\dfrac{d}{dx}\big[c\cdot f(x)\big] = c\cdot f'(x)
$$ 


## Product Rule

$$
\dfrac{d}{dx}\big[f(x)\cdot g(x)\big] = \big[f(x)\big]' \cdot g(x) + f(x)\cdot \big[g(x)\big]'
$$ 

## Quotient Rule

$$
\dfrac{d}{dx}\left[\dfrac{f(x)}{g(x)}\right] = \dfrac{\big[f(x)\big]' \cdot g(x) - f(x)\cdot \big[g(x)\big]'}{(g(x))^2}
$$ 

## Chain Rule
$$
\dfrac{d}{dx}\bigg[f(g(x))\bigg] = f'(g(x))\cdot g'(x)
$$
