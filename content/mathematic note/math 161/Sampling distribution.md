The mean and standard deviation of x̅
$$
\bar{x}=\frac{1}{n}(X_{1}+X_{2}+\dots +Xn)
$$
If the population has mean μ, then μ is the mean of the distribution of each observation $X_{i}$. Why? assume we have 60 data 
The $\mu$ is the sum of the data divide by 60. What if we take sample with size 5. Since they are equal likely to be choose so, there are 12 group of data(random variable) that have the same probability, Thus, we add the group data and then divide by 12 and then add together divide by 5 is exactly the same as the $\mu$

Thus,
$$
\begin{align}
\mu_{\bar{x}}&=\frac{1}{n}(\mu+\mu+\dots+\mu) \\
&=\mu
\end{align}
$$

Imagine you have a bag with 60 slips of paper, each with a number on it. You reach in and pull out **one** slip ($X_1$).

- Before you look at it, what do you expect it to be?
    
- It could be any of the 60 numbers, each with a probability of $1/60$.
    
- The "average" result of this single draw is:
    
    $$E[X_1] = (x_1 \cdot \frac{1}{60}) + (x_2 \cdot \frac{1}{60}) + \dots + (x_{60} \cdot \frac{1}{60})$$
    
- Factor out the $1/60$:
    
    $$E[X_1] = \frac{1}{60} \sum x_i = \mu$$


How about the variance?
It is the same way
$$E[X_1] = (x_1 \cdot \frac{1}{60}) + (x_2 \cdot \frac{1}{60}) + \dots + (x_{60} \cdot \frac{1}{60})$$
Imagine the data is shrinking to $\frac{1}{n}$ size, so the variance must shrink to $\frac{1}{n^{2}}$ size. Thus,

$$
\begin{align}
\sigma_{x}^{2}&=\left( \frac{1}{n^{2}} \right)(\sigma^{2}+\sigma^{2}+\dots+\sigma^{2}) \\
&=\frac{\sigma^{2}}{n}
\end{align}
$$
### The Central Limit Theorem

Suppose $X_{1},X_{2},\dots,X_{n}$ are independent random variable that having a common distribution. When $n$ increase the distribution resembles normal distribution.

In real world, Without replacement, thus $n$ must be large enough.??

Thus, by this theorem we can use standard normal distribution to compute the probability about the sample mean when $n> 30$.

### Standard Error of the mean
$\sigma_{\bar{X}}= \frac{\sigma}{\sqrt{ n }}$ describe the degree to which the sample statistic differ from one another.

### Sampling Distribution of Sample Proportions, pˆ


$\mu_{\hat{p}}=p$

$\sigma^{2}_{\hat{p}}=\frac{pq}{n}$

For cases where n is sufficiently large (so that $np>5$ and $nq>5$), the normal approximation on the binomial distribution may be used to find probabilities about pˆ.