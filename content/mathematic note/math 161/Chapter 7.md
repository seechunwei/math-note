
# A Comprehensive Guide to Inferential Statistics: Estimation
## 1.0 The Foundation of Inferential Statistics

Inferential statistics is the branch of statistics that uses information gathered from a sample to make decisions and draw conclusions about the characteristics of an entire population. While the study of probability distributions provides the theoretical framework, inferential statistics is the practical application of these concepts. It helps us move from observing a small, manageable subset of data to making informed judgments about the larger group from which the data was drawn.

A critical first step in this process is understanding the distinction between measures calculated for a population and those calculated for a sample.

|                                                                                                    |                                                                                   |
| -------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------- |
| Population Parameter                                                                               | Sample Statistic                                                                  |
| A **population parameter** is a constant numerical summary measure calculated for population data. | A **sample statistic** is a random variable calculated from sample data.          |
| _Examples:_ Population Mean (μ), Population Variance (σ²), Population Standard Deviation (σ)       | _Examples:_ Sample Mean (x̄), Sample Variance (s²), Sample Standard Deviation (s) |

Because a sample statistic is a random variable, it has a probability distribution. This specific distribution is called a **sampling distribution**, and it is the conceptual bedrock upon which all of inferential statistics is built. By understanding the behavior of a sample statistic's distribution, we can begin to make reliable inferences about the unknown population parameter it represents. These foundational concepts pave the way for the two primary methods used to make statistical inferences.

## 2.0 The Core Methods of Inference: Estimation and Hypothesis Testing

The main objective of inferential statistics is to gain knowledge about unknown population parameters by analyzing the information contained in sample data. When the true value of a population parameter is already known, there is no need for inference. However, in most real-world scenarios, these values are unknown, and we must rely on samples to learn about them.

There are two primary methods for making inferences about a population:

1. **Estimation**: This is the process of estimating the value of a population parameter. This can be done by providing a single value, known as a **point estimate**, or by constructing a range of plausible values, known as an **interval estimate**.
2. **Hypothesis Testing**: This is the process of evaluating claims or theories about a population parameter to determine their validity.

This document will focus exclusively on the first of these methods: the procedures and concepts behind **Estimation**. We will begin by exploring the simplest form of estimation, the point estimate.

## 3.0 Point Estimation: Using a Single Value to Estimate a Parameter

A **point estimate** is the simplest form of statistical inference. It is a single value, calculated from a sample statistic, that is used to estimate an unknown population parameter. The sample statistic used to generate this estimate is referred to as an **estimator**.

The table below shows the common population parameters and their corresponding point estimators.

|                           |                        |
| ------------------------- | ---------------------- |
| Parameter                 | Estimator              |
| Population Mean (μ)       | Sample Mean (x̄)       |
| Population Proportion (p) | Sample Proportion (p̂) |
| Population Variance (σ²)  | Sample Variance (s²)   |

For an estimator to be considered effective, it should possess certain desirable properties. The three key properties of a good estimator are:

- **Unbiased:** An estimator is unbiased if its expected value is equal to the population parameter it is intended to estimate. This means that, on average, the estimator will hit the true target value.
- **Less variable:** The variability of an estimator is measured by the standard deviation of its sampling distribution. Between two unbiased estimators, the one with the smaller standard deviation is considered better because its values are more tightly clustered around the true parameter.
- **Consistent:** A consistent estimator is one whose value tends to get closer to the true value of the population parameter as the sample size increases.

While a point estimate provides a straightforward and useful "best guess," its primary limitation is that it does not convey any information about the certainty or precision of the estimate. To address this, we turn to interval estimation.

## 4.0 Interval Estimation: Constructing a Range of Plausible Values

An **interval estimate**, more commonly known as a **confidence interval**, provides a more complete picture than a point estimate. Instead of a single value, it offers a range of values that likely contains the true population parameter. Crucially, this range is accompanied by a specified level of confidence, giving us a measure of the estimate's reliability.

The following terms are essential for understanding and constructing confidence intervals:

- **Confidence Level:** This is the specified certainty that the procedure used to create the interval will produce a range containing the true population parameter. It is typically expressed as a percentage, with 90%, 95%, and 99% being the most common levels.
- **Confidence Coefficient (1 − α):** This is the confidence level expressed as a probability. It represents the probability that a randomly selected sample will yield an interval that successfully includes the parameter being estimated. For a 95% confidence level, the confidence coefficient is 0.95.

It is vital to interpret a confidence interval correctly. Once a specific interval is calculated from a sample, the true population parameter either is or is not within that interval. Therefore, the probability of it containing the parameter is technically either 1 or 0. The confidence level applies to the _method_ of constructing the interval, not to any single result. The correct phrasing is, for example: **"We are 95% confident that the interval contains the true population parameter."** This means that under repeated sampling, 95% of the intervals constructed using this method would contain the true parameter.

Now, we can apply these concepts to estimate specific population parameters, beginning with the most common: the population mean.

## 5.0 Estimating a Population Mean (μ)

Estimating the average value of a population, such as the mean weight of a product or the average test score of applicants, is a common statistical task. The confidence interval for a population mean (μ) is constructed around the sample mean (x̄) and takes the general form:

`(point estimate − margin of error, point estimate + margin of error)`

The procedure for constructing this interval depends on whether the population variance (σ²) is known or unknown.

### 5.1 Case 1: Population Variance (σ²) is Known

A confidence interval for the population mean can be constructed using the standard normal (Z) distribution under the following conditions:

- The population from which the sample is drawn is normally distributed.
- The sample size is large (n ≥ 30), which allows us to invoke the Central Limit Theorem, meaning the sampling distribution of the sample mean is approximately normal regardless of the population's distribution.

The formula for a (1 − α)100% confidence interval for the population mean (μ) when σ² is known is:

`x̄ ± zα/2 * (σ / √n)`

The components of this formula are:

- `x̄`: The **point estimate** (the sample mean).
- `zα/2`: The **critical value** from the standard normal distribution corresponding to the chosen confidence level.
- `σ/√n`: The **standard error** of the mean, which is the standard deviation of the sampling distribution of x̄.
- `zα/2 * (σ / √n)`: The entire second term is the **Margin of Error (E)**, which is half the width of the confidence interval.

### 5.2 Case 2: Population Variance (σ²) is Unknown

In most real-world problems, if the population mean is unknown, the population variance is almost always unknown as well. In this more common scenario, we must estimate the standard error of the mean by using the sample standard deviation (`s`) in place of the population standard deviation (`σ`). This gives us an estimated standard error of `s/√n`.

When the population is normally distributed but σ is unknown, we use the **Student's t-distribution** instead of the standard normal distribution.

The t-distribution has the following key properties:

- It is bell-shaped and symmetric around a mean of 0.
- It has a lower height and a wider spread (i.e., is more variable) than the standard normal distribution.
- Its shape depends on a parameter called **degrees of freedom (df)**, which for this application is calculated as `df = n - 1`.
- As the degrees of freedom increase (i.e., as the sample size grows), the t-distribution approaches the standard normal distribution.

The formula for a (1 − α)100% confidence interval for the population mean (μ) when σ² is unknown is:

`x̄ ± t(n-1),α/2 * (s / √n)`

For large samples (n ≥ 30), there are two options: use the `t` value from the last row (infinity) of the t-distribution table, or use the standard normal (Z) distribution as an approximation.

Having covered the estimation of means, we now turn our attention to estimating population proportions.

## 6.0 Estimating a Population Proportion (p)

In many situations, the parameter of interest is not a mean value but a proportion or percentage. For example, a manufacturer may want to estimate the proportion of defective items produced, or a company may wish to determine the percentage of customers satisfied with a service.

The point estimate for the population proportion (p) is the **sample proportion**, which is calculated as: `p̂ = x/n`, where `x` is the number of successes in the sample and `n` is the sample size.

For a sufficiently large sample, the sampling distribution of p̂ is approximately normal. The conditions required to use this normal approximation are: `np ≥ 5` and `nq ≥ 5`, where `q = 1 - p`.

The formula for a (1 − α)100% confidence interval for the population proportion (p) is:

`p̂ ± zα/2 * √(p̂q̂ / n)`

In this formula, `s_p̂ = √(p̂q̂ / n)` represents the estimated standard error for the proportion.

Next, we will explore the methods for estimating the variability within a population.

## 7.0 Estimating a Population Variance (σ²)

Controlling and estimating the variance (or standard deviation) of a population is critical in many fields, particularly in quality control and manufacturing. For instance, a machine that fills biscuit packages must be consistent. If the variance of the fill weights is too large, some packages will be significantly underfilled while others are overfilled, both of which are undesirable. Unlike the z and t distributions used for means, which are symmetric, estimating variance requires a distribution that is non-negative and skewed, as variance itself cannot be negative. This is the role of the **Chi-square (χ²)** distribution.

Assuming the underlying population is approximately normally distributed, the Chi-square distribution has the following key properties:

- Its values are always non-negative (greater than or equal to 0).
- It is a family of curves, with the specific shape determined by the degrees of freedom.
- The distributions are positively skewed.

The formula for a (1 − α)100% confidence interval for the population variance (σ²) is given by:

`(n - 1)s² / χ²α/2 ≤ σ² ≤ (n - 1)s² / χ²1-α/2`

(Note that because the chi-square distribution is not symmetric, the lower and upper critical values, `χ²1-α/2` and `χ²α/2`, are not simply ± values like with the z or t distributions).

Here, `χ²α/2` and `χ²1-α/2` are critical values from the chi-square distribution with `n - 1` degrees of freedom. As a final note, a confidence interval for the population standard deviation (σ) can be easily found by taking the positive square root of the lower and upper limits of the interval for the variance.

## 8.0 Practical Application: Determining the Required Sample Size

The difference between a point estimate and the true value of the parameter is called the **error of estimation**, or **margin of error (E)**. A crucial step in the planning phase of any study is to determine the sample size needed to achieve a desired level of precision. By calculating the required sample size _before_ collecting data, a researcher can ensure that the final estimate will be sufficiently close to the true population value with a specified level of confidence.

The formulas for determining sample size vary depending on the parameter being estimated.

#### Estimating a Population Mean (μ)

To find the sample size needed to estimate μ within a specified margin of error `E`:

`n = (zα/2 * σ / E)²`

#### Estimating a Population Proportion (p)

To find the sample size needed to estimate p within a specified margin of error `E`:

- If a preliminary estimate of the sample proportion (`p̂`) is available: `n = z²α/2 * p̂q̂ / E²`
- If `p̂` is unknown (the conservative approach): `n = 0.25 * z²α/2 / E²` This formula uses `p̂ = 0.5`, which yields the maximum possible sample size and thus guarantees the desired margin of error regardless of the true proportion.

When using these formulas, it is critical to follow one rule: **always round the calculated value of** `**n**` **up to the next whole number** to ensure the sample size is sufficient.

## 9.0 Key Terms and Final Takeaway

### Key Term Definitions

- **Inferential Statistics**: The use of sample results to make decisions and draw conclusions about the population from which the sample is drawn.
- **Population Parameter**: A constant numerical summary measure calculated for population data.
- **Sample Statistic**: A random variable calculated from sample data, used to estimate a population parameter.
- **Sampling Distribution**: The probability distribution of a sample statistic.
- **Point Estimate**: The value of a sample statistic that is used to estimate a population parameter.
- **Interval Estimate (Confidence Interval)**: An interval estimate of an unknown population parameter, constructed with a specified level of confidence.
- **Confidence Level**: The specified certainty (e.g., 95%) that the procedure used to generate a confidence interval will produce an interval containing the true population parameter.
- **Margin of Error**: The maximum error of estimation; it specifies how close the estimate is to the true population value and is one-half the width of the confidence interval.
- **Student's t-distribution**: A probability distribution used for making inferences about a population mean when the population is normally distributed and the population variance is unknown.
- **Chi-square (χ²) distribution**: A probability distribution used to construct a confidence interval for a population variance.

### Core Takeaway

Estimation provides a structured, probabilistic framework for making informed judgments about an entire population based on limited sample data. A point estimate provides a single "best guess," but the probability that it is exactly correct is essentially zero. In contrast, a confidence interval provides a more complete and meaningful result. By furnishing a range of plausible values along with a measure of probabilistic confidence, interval estimation offers a crucial assessment of an estimate's reliability, empowering us to draw sound conclusions from data in the face of uncertainty.