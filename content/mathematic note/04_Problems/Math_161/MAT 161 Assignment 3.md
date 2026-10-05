Group member:
1) LEONG WEN XUAN 24303049
2) LIN XING WEI 24302816
3) SEE CHUN WEI 24302351

Q1
a) 
Let X represent the random variable of the mean soil pH
Let D represent the random variable of change in the soil pH

$d=x_{\text{after}}-x_{\text{before}}$

| $x_{\text{after}}$ | $x_{\text{before}}$ | $d$   | $d^{2}$ |
| ------------------ | ------------------- | ----- | ------- |
| 10.21              | 10.02               | 0.19  | 0.0361  |
| 10.16              | 10.16               | 0     | 0       |
| 10.11              | 9.96                | 0.15  | 0.0225  |
| 10.1               | 10.01               | 0.09  | 0.0081  |
| 10.07              | 9.87                | 0.2   | 0.04    |
| 10.13              | 10.05               | 0.08  | 0.0064  |
| 10.08              | 10.07               | 0.01  | 1E-04   |
| 10.3               | 10.08               | 0.22  | 0.0484  |
| 10.17              | 10.05               | 0.12  | 0.0144  |
| 10.1               | 10.04               | 0.06  | 0.0036  |
| 10.06              | 10.09               | -0.03 | 0.0009  |
| 10.37              | 10.09               | 0.28  | 0.0784  |
$\sum d^{2}=0.2589$
$\sum d=1.37$
$\bar{d}=0.1142$

$$
\begin{align}
s_{d}&=\sqrt{ \frac{\sum d^{2}-\frac{\left( \sum x \right)^{2}}{n}}{n-1} } \\
&=\sqrt{ \frac{0.2589-\frac{(1.37)^{2}}{12}}{11} } \\
&=0.09653
\end{align}
$$

Select the distribution to use:
$\sigma$ is unknown, Population distribution: Unknown and $n<30$. Thus, we assume that $D$ is approximately normal distributed. Thus, we use t-distribution.

$df=12-1$
$1-\alpha=0.99$
$\alpha=0.01$
$\dfrac{\alpha}{2}=0.005$

99% Confidence interval: 
$$
\begin{align}
\bar{d} \pm t_{ \alpha  / 2,n-1}\left( \frac{s_{d}}{\sqrt{ n }} \right)&=0.1142  \pm 3.106\left( \frac{0.09653}{\sqrt{ 12 }} \right) \\
&= (0.02765,0.20075)
\end{align}
$$

$\therefore$ We are 99% confident that the true mean change in soil pH is between **0.0277** and **0.2008**.

---



b) 
- $H_0: \mu_d \le 0$ (The mean soil pH did not increase)
- $H_1: \mu_d > 0$ (The mean soil pH increased significantly)


$\sigma$ is unknown, Population distribution: Unknown and $n<30$. Thus, we assume that $D$ is approximately normal distributed. Thus, we use t-distribution.

Test Statistic:

$$t_{0} = \frac{\bar{d} - \mu_0}{s_d / \sqrt{n}} = \frac{0.1142 - 0}{0.0965 / \sqrt{12}} = \frac{0.1142}{0.0279} = 4.099$$
For RTT:
$\alpha=0.01$
$df=12-1=11$
P-value=$P(T>4.099)$
$0.0005<P(T>4.099)<0.001$ (From table 10)

Since, P-value<$\alpha$ (Reject $H_{0}$)

$\therefore$ There is sufficient evidence at the 1% significance level to conclude that the mean soil pH has significantly increased after reclamation. **Therefore, the mining company will be fined.**

---


Q2
a) 
$H_0: \mu = 12.1$ 
$H_1: \mu < 12.1$ 

$\sigma$ is unknown, Population distribution: Unknown, but $n>42$, by CLT- Standard normal distribution

Let the confidence level=95%. Thus, $\alpha=0.05$ ,$n = 42$, $\bar{x}=11.4$, $s=1.9$

Test Statistic:

$$t_{0} = \frac{\bar{x} - \mu}{s / \sqrt{n}} = \frac{11.4 - 12.1}{1.9 / \sqrt{42}} = \frac{-0.7}{0.2932} = -2.3876$$
For LTT, Critical value:
$t_{41,0.05}=1.684$
RR: $T\leq-1.684$

![[Pasted image 20251220124621.png]]

Since the observed value $-2.3876\leq-1.684$ (In RR). Thus, we reject $H_{0}$.

There is sufficient evidence to reject Teslow's claim. The mean fuel consumption is statistically specifically lower than 12.1 km/ litre .

---

b)
 $H_0: \sigma \le 0.8$ (Standard deviation is within limits)
 $H_1: \sigma > 0.8$ (Standard deviation is higher than claimed)
Test Statistic:

$$\chi^2 = \frac{(n-1)s^2}{\sigma_0^2} = \frac{(41)(1.9)^2}{(0.8)^2} = \frac{148.01}{0.64} = 231.266$$

For RTT, Critical value:
$df=41$
$X^2_{0.05, 41} \approx X^2_{0.05, 40}=55.76$.
RR: $X^{2}\geq 55.76$

![[Pasted image 20251220123839.png]]

Since the observed value $231.266 \geq{5}5.76$ (In RR). Thus, we reject $H_{0}$.

$\therefore$ There is overwhelming evidence that the variability in fuel consumption is significantly higher than Teslow's claim of 0.8 km/litre.

---

c)
From finding in (a), we know that the Car X does not  achieve 12.1 km/litre on average. The real performance is less than what they are claiming for. Thus, Tesla must accurate the fuel efficiency to avoid false advertising claims.

From finding in (b), since we reject $H_{0}$ ,the hypothesis test showed that the fuel consumption of the Car X varies significantly. It means that the difference of fuel consumption of car X is huge. Thus, Tesla should increase its quality control to reduce this high variability.
