Probability density function(pdf)- a function used to defined the probability of continuous random variable.

The probability of a continuous random variable which is a interval $(a,b)$ are the area below the function at given interval.

$$P(x_{1}<X<x_{2})=\int ^{x_{2}}_{x_{1}} f(x)\, dx$$
#### Properties of a (Continuous) Probability Density Function

1) The probability that X lies between two points, $x_{1}$ and $x_{2}$, is a number between 0 and 1.

$$0<P(x_{1}<X<x_{2})<1$$

The total probability of $X$ over all defined intervals in 1. If $X$ is defined on the whole real line, then 
$$
\int^{\infty}_{-\infty}f(x) \, dx=1 
$$

#### Mean and Variance of a Continuous Random Variables
$$
E(X)=\int^{}_{x}xf(x)\,dx 
$$

$$
\begin{align}
Var(X)&=\left[ \int^{}_{x}x^{2}f(x)\,dx  \right]-\mu^{2} \\
&=E(X^{2})-\mu^{2}
\end{align}
$$


### Some Special Continuous Probability Distributions

#### The Continuous Uniform Distribution

$X\sim Uni(a,b)$, then $f(x)=\dfrac{1}{b-a},\,a\leq x\leq b$

$\frac{1}{b-a}$ is height while $b-a$ is width 

#### Mean and variance of a Uniform Variable

$$
\begin{align}
E(X)=\frac{b+a}{2} 
\end{align}
$$

$$
Var(X)=\frac{b^{2}+ab+a^{2}}{3}-\frac{(b+a)^{2}}{4}=\frac{(b-a)^{2}}{12}
$$


### The Normal Distribution

We will use standard normal distribution table to find the probability $P(Z\leq z)$ . A continuous random variable with normal distribution denoted by $X\sim N(\mu,\sigma^{2})$ where $\mu$ and $\sigma^{2}$ are parameter.

The shape of normal distribution defined by these 2 parameter. $\mu$ determine the center while $\sigma^{2}$ determine the dispersion of data (the spread of data).

Standard normal distribution
$$
X\sim Z(0,1)
$$

How to find the probability of a non-standard normal variable?

We need to standardize the normal distribution 
$$
\begin{align}
P(x_{1}\leq X\leq x_{2})=P\left( \frac{x_{1}-\mu}{\sigma}\leq Z\leq \frac{x_{2}-\mu}{\sigma} \right)
\end{align}
$$

Because $Z=\frac{X-\mu}{\sigma}$

#### Approximation 
Notice that we can use standard normal distribution to approximate the binomial distribution. 

When $np> 5$ and $n(1-p)> 5$. then $\mu=np$ and $\sigma^{2}=np(1-p)$

But we need to perform continuity correction step.

$P(X=a)\implies P(a-0.05\leq X\leq a+0.05)$

==Poisson Approximation==

Suppose $X\sim Po(\mu)$. If $\mu>10$, then $X$ can be approximated with a normal distribution with mean $\mu$ and variance $\sigma^{2}=\mu$.
