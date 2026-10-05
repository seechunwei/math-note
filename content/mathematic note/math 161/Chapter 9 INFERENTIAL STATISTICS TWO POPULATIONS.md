
We may want to make a confidence interval for the difference between the mean prices of houses in Penang and in Kedah

We want to study about the difference of two population parameters

The two samples used to make inference about two populations can be independent or dependent samples. The dependence or independence is determined by the source of the data

| **Component**                | **Dependent Samples(σd​ Unknown)**                 | **Independent Samples(σx​,σy​ Known)**                                                                     | **Independent Samples(σx​,σy​ Unknown)Equal Variances**                                                                                                                                         | **Independent Samples(σx​,σy​ Unknown)Unequal Variances**                                                                                                                                     |
| ---------------------------- | -------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Distribution**             | **t-distribution**<br><br>  <br><br>$df = n_d - 1$ | **Z-distribution**<br><br>  <br><br>(Standard Normal)<br><br>  <br><br>$N(0,1)$                            | **t-distribution**<br><br>  <br><br>$df = n_x + n_y - 2$                                                                                                                                        | **t-distribution**<br><br>  <br><br>$df \approx \frac{(s_x^2/n_x + s_y^2/n_y)^2}{\frac{(s_x^2/n_x)^2}{n_x-1} + \frac{(s_y^2/n_y)^2}{n_y-1}}$<br><br>  <br><br>(Satterthwaite's approximation) |
| **Variance Estimator**       | $s_{\bar{d}}^2 = \frac{s_d^2}{n_d}$                | $\sigma_{\bar{x}-\bar{y}}^2 = \frac{\sigma_x^2}{n_x} + \frac{\sigma_y^2}{n_y}$                             | $s_{\bar{x}-\bar{y}}^2 = s_p^2(\frac{1}{n_x} + \frac{1}{n_y})$<br><br>  <br>  <br><br>_Pooled Variance ($s_p^2$):_<br><br>  <br><br>$s_p^2 = \frac{(n_x-1)s_x^2 + (n_y-1)s_y^2}{n_x + n_y - 2}$ | $s_{\bar{x}-\bar{y}}^2 = \frac{s_x^2}{n_x} + \frac{s_y^2}{n_y}$                                                                                                                               |
| **Confidence Interval (CI)** | $\bar{d} \pm t_{\alpha/2} \frac{s_d}{\sqrt{n_d}}$  | $(\bar{x} - \bar{y}) \pm z_{\alpha/2} \sqrt{\frac{\sigma_x^2}{n_x} + \frac{\sigma_y^2}{n_y}}$              | $(\bar{x} - \bar{y}) \pm t_{\alpha/2} s_p \sqrt{\frac{1}{n_x} + \frac{1}{n_y}}$                                                                                                                 | $(\bar{x} - \bar{y}) \pm t_{df, \alpha/2} \sqrt{\frac{s_x^2}{n_x} + \frac{s_y^2}{n_y}}$                                                                                                       |
| **Test Statistic (TS)**      | $T = \frac{\bar{d} - \mu_d}{s_d / \sqrt{n_d}}$     | $Z = \frac{(\bar{x} - \bar{y}) - (\mu_x - \mu_y)}{\sqrt{\frac{\sigma_x^2}{n_x} + \frac{\sigma_y^2}{n_y}}}$ | $T = \frac{(\bar{x} - \bar{y}) - (\mu_x - \mu_y)}{s_p \sqrt{\frac{1}{n_x} + \frac{1}{n_y}}}$                                                                                                    | $T = \frac{(\bar{x} - \bar{y}) - (\mu_x - \mu_y)}{\sqrt{\frac{s_x^2}{n_x} + \frac{s_y^2}{n_y}}}$                                                                                              |

## Inferences about the Difference between Two Population Proportions

consider their difference, $p_{1}-p_{2}$

### Sampling Distribution

$\mu_{\hat{p}_{1}-\hat{p}_{2}}=p_{1}-p_{2}$ 

$\sigma_{\hat{p}_{1}-\hat{p}_{2}}=\sqrt{ \frac{p_{1}q_{1}}{n_{1}}+\frac{p_{2}q_{2}}{n_{2}} }$

We need to check if the sample size is large by $n_{1}p_{1},n_{1}q_{1},n_{2}p_{2},n_{2}q_{2}\geq 5$

Since we don't know $p_{1}q_{1}$ and $p_{2}q_{2}$ . Thus, we will use $\hat{p}_{1}-\hat{p}_{2}$ to estimate.

![[Pasted image 20260130160505.png]]

### Hypothesis Test about the Two Population Variances

When comparing two variances;!"and ;"", the common statistical procedure considers their ratio. If the variances are nearlyequal, then the ratio will be close to one.

the ratio of $X_{2}$" distributions is an $F$-distribution,

Test statistic
$$
F=\frac{s ^{2}_{1}}{s_{2}^{2}}
$$
Since we don't know about the ratio $\frac{\sigma_{1}^{2}}{\sigma_{2}^{2}}$ . Thus we will use $\frac{s_{1}^{2}}{s_{2}^{2}}$. 

$F-distribution$ determined by 2 degree of freedom which is $n_{1}-1$ and $n_{2}-1$.


$F_{1-\alpha,df_{N},df_{D}}=\dfrac{1}{F_{\alpha,df_{N},df_{D}}}$

$F_{1-\alpha}$ is at left tail and $F_{\alpha}$ is at right tail consider $\alpha$ is the probability more than the critical value.