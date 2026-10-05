Chapter 4 study about event where each sample point have same probability.  Or we say that the element of the event is one of the outcome in experiment. Thus, what if group the outcome that satisfy certain condition? 

For example Let $Y$ be set of number of times we get 6 form tossing 1 dice for 3 times. Notice the different $S=\{ \{ 1,1,1 \},\{ 1,2,3 \},\dots,\{ 6,6,6 \} \}$
Each element in sample space have same probability but how about $Y$?
$Y=\{ 0,1,2,3 \}$
Each element have different probability , we say $Y$ is a random variable because it is a characteristic of interest of experiment that its value is determined by the outcome of experiment. Thus, we will study about the probability distribution.

- **Formal Definition:** A random variable is a function that maps a sample space to real numbers ($S \rightarrow \mathbb{R}$).
- **The Set $\{0, 1, 2, 3\}$:** This is called the **Support** or the **Range** of the random variable (the possible values it can take).

A random variable can either be discrete or continuous.

### Probability Distributions: Discrete Random Variables
Properties:
1) The probability assigned to each value of random variable is between 0 and 1
$$
0\leq P(x)\leq 1
$$
2) The sum of the probability assigned to all values of the random variable must equal to one 
$$
\sum P(x)=1
$$
Thus, we need to group all the sample point under certain condition.

#### Mean and Variance of a Discrete Probability Distribution

Mean
Mean is average , we multiply each data with frequency and divide by $n$. Thus, in random variable, we use relative frequency and $n =1$. Thus,
$$
\mu=\sum \frac{xP(x)}{1}=\sum xP(x)
$$
$P(x)$ is relative frequency 

Variance
$$
\sum x^{2}P(x)-\mu^{2}
$$

#### Some Special Discrete Probability Distributions
##### The Binomial Distribution

Binomial Probability Experiment
A binomial experiment is made up of repeated trials that has the following properties:
1) There are $n$ repeated, independent trials
2) Each trial has two possible outcomes (success or failure)
3) The binomial random variable X, is the count of the number of successful trials that occur; X may take on any integer value from zero to n.

The parameter of a binomial random variable is $n$ and $p$.

$P(X=x)=P(x)=\binom{n}{x}p^{x}q^{n-x}$


We can use **Binomial Probability Table**, but notice that the table give us the value of $P(X\leq x)$ for $p\leq0.5$. Thus, for $p>0.5$ , $q\leq 0.5$ , we use $q$ to find the probability

$X \sim B(n, p)$
$Y\sim B(n,q)$, with $p+q=1$ , $X+Y=n$

$$
\begin{align}
P(X=r)&=P(n-Y=r) \\
&=P(Y=n-r)
\end{align}
$$
$$
\begin{align}
P(X\leq r)&=P(n-Y\leq r) \\
&=P(Y\geq n-r)
\end{align}
$$
##### Mean & Standard Deviation of the Binomial Distribution

mean:$\mu=np$
$\sigma=\sqrt{ npq }$

#### The Poison Distribution

- counts occurrences over a continuous interval of time or space.

- It can be used to approximate binomial probabilities when the probability of a success is small ($p\leq 0.05$) and the number of trials is large ($n\geq 20$).

Note that the number of possible occurrences is countable but there is no fixed upper limit.

Property of Poison random variable
1) The probability that an event will occur in a short interval of time or space is proportional to the size of the interval.
2) In a very small interval, the probability that two events will occur is close to zero.
3) Independent

##### Poison Probability Density Function
If a random variable X has a Poisson distribution with parameter $\mu$, then its probability density function is given by:
$$
P(X=x)=\frac{e^{-\mu}\mu^{x}}{x!}
$$
 $X\sim Po(\mu)$
##### The Mean and Variance
$E(X)=\mu$ 
$Var(X)=\mu$

Poisson distribution can be used to approximate the binomial distribution if
$n\geq 100$, $p<0.1$ so that $np<10$

#### The Hypergeometric Distribution
- is useful for determining the probability of a number of occurrences when sampling is done **without replacement**.
- counts the number of successes (x) in n selections from a population of N elements, k of which are successes and (N-k) of which are failures.

We are given a population with constant $p$ as the probability of success, the question is if we draw a sample from the population, what is the probability of success?

$P(X=x)=\dfrac{\binom{k}{x}\binom{N-k}{n-x}}{\binom{N}{n}}$
