### Step-by-Step Derivation


1. The Initial Inequality

The derivation begins with the standard normal distribution (Z-distribution) inequality. We assume the sample mean follows a normal distribution, so the standardized score (z-score) lies between two critical values, $-z_{\alpha/2}$ and $z_{\alpha/2}$:

$$-z_{\alpha/2} < \frac{\bar{x} - \mu}{\frac{\sigma}{\sqrt{n}}} < z_{\alpha/2}$$

- **$\bar{x}$**: Sample mean.
    
- **$\mu$**: Population mean (the value we want to estimate).
    
- **$\sigma / \sqrt{n}$**: Standard error of the mean.
    

2. Isolate the Middle Term (Multiply by Standard Error)

To start isolating $\mu$, multiply all parts of the inequality by the denominator, $\frac{\sigma}{\sqrt{n}}$:

$$-z_{\alpha/2} \left( \frac{\sigma}{\sqrt{n}} \right) < \bar{x} - \mu < z_{\alpha/2} \left( \frac{\sigma}{\sqrt{n}} \right)$$

3. Subtract the Sample Mean ($\bar{x}$)

Subtract $\bar{x}$ from all three parts of the inequality to move it away from the center:

$$-\bar{x} - z_{\alpha/2} \left( \frac{\sigma}{\sqrt{n}} \right) < -\mu < -\bar{x} + z_{\alpha/2} \left( \frac{\sigma}{\sqrt{n}} \right)$$

4. Multiply by $-1$ (Flip the Inequality)

To solve for a positive $\mu$, multiply the entire inequality by $-1$. Crucially, multiplying an inequality by a negative number flips the direction of the signs:

$$\bar{x} + z_{\alpha/2} \left( \frac{\sigma}{\sqrt{n}} \right) > \mu > \bar{x} - z_{\alpha/2} \left( \frac{\sigma}{\sqrt{n}} \right)$$

5. Rearrange into Standard Form

Finally, rewrite the inequality in ascending order (from smallest to largest) to arrive at the final confidence interval formula:

$$\bar{x} - z_{\alpha/2} \left( \frac{\sigma}{\sqrt{n}} \right) < \mu < \bar{x} + z_{\alpha/2} \left( \frac{\sigma}{\sqrt{n}} \right)$$
In sapling distribution we learn about the relationship between then population parameter and the mean and standard deviation of sample statistic.

We are given the population parameter to infer about the sampling distribution. For example, we are given the population mean and $\sigma$ , we are asked to find the probability of taking size $n$ sample that the mean more than...... 
Since we can find the mean and standard deviation of sample statistic, thus we can find the probability by using the standard normal distribution
 

In chapter 7 we learn about the point estimate and interval estimate. We need to infer the population parameter using the sample statistic and its sampling distribution. We are given the $\sigma$ or $s$ and $\bar{x}$ , notice that this $\bar{x}$ is not always reveal the true value of $\mu$ because in real life it is impossible to take all the sample. Notice that the $s$ and $\sigma$ here is not the standard deviation of sample statistic, it is for sample or population itself.

Thus, we take $\bar{x}$ from one random sample and we use the $\sigma$ or $s$ to find the $\sigma_{\bar{x}}$ and also the confidence level to determine the $z_{\frac{\alpha}{2}}$ . And we construct the confidence interval. Notice that the confidence level is not the probability because the real parameter is either in the interval or outside the interval so it probability is either 0 or 1.

Notice that the $\bar{x}$ is differ from sample and cannot reveal the true value of $\mu$, thus different sample will give us different interval. The 90% of confidence level represent if we take many sample to construct the interval, the true $\mu$ will fall between 90% of these interval.


Hypothesis test 
The value of alpha and beta


The most important thing to understand is that **$\alpha$ and $\beta$ have an inverse relationship.**

Imagine you are adjusting the sensitivity of a **car alarm**:

- **Scenario A: Super Sensitive (High $\alpha$, Low $\beta$)**
    
    - You set the alarm to go off if a leaf falls on the car.
        
    - **Result:** You will definitely catch every thief (**Low $\beta$**), BUT the alarm will go off constantly when no one is there (**High $\alpha$**).
        
- **Scenario B: Not Sensitive (Low $\alpha$, High $\beta$)**
    
    - You set the alarm to go off only if the window is smashed.
        
    - **Result:** You will almost never have a false alarm (**Low $\alpha$**), BUT a thief could quietly pick the lock and steal the car without you knowing (**High $\beta$**).


Let me clarify the difference between the **General Rule** (Science/Law) and the **Exception** (Safety/Screening).

Why we always set alpha to be very low? Because we are protecting the H0.

Notice that If we interchange the H0 and H1 the value of alpha and beta will interchange.


Derivation of confidence interval for variance

This derivation is very similar to the one for the population mean, but with one major "twist": **The Chi-Square ($\chi^2$) distribution is not symmetric.** This is why the formula looks different on the left and right sides (you divide by different numbers instead of just adding/subtracting a margin of error).

Here is the step-by-step derivation for the Confidence Interval of the Population Variance ($\sigma^2$).

### 1. The Foundation: The "Pivot" Variable

We start with a known statistical fact: If samples come from a Normal distribution, the relationship between the sample variance ($s^2$) and the population variance ($\sigma^2$) follows a **Chi-Square distribution** with $n-1$ degrees of freedom:

$$\chi^2 = \frac{(n-1)s^2}{\sigma^2}$$

### 2. The Probability Statement

We want to capture the middle $(1-\alpha)\%$ of this distribution. Because the curve is skewed (lopsided), we cannot just use $\pm$ a single number. We need two distinct cutoffs:

- **Right Tail Cutoff ($\chi^2_{\alpha/2}$):** Leaves $\alpha/2$ area to the right (a large number).
    
- **Left Tail Cutoff ($\chi^2_{1-\alpha/2}$):** Leaves $\alpha/2$ area to the left (a small number).
    

We write the probability statement:

$$P\left( \chi^2_{1-\alpha/2} \le \frac{(n-1)s^2}{\sigma^2} \le \chi^2_{\alpha/2} \right) = 1 - \alpha$$

### 3. The Algebra (Isolating $\sigma^2$)

Our goal is to get $\sigma^2$ alone in the middle.

Step A: Invert everything

We flip the fractions upside down. Crucial Rule: When you flip inequalities ($1/x$), the direction of the signs must reverse (e.g., $2 < 5$, but $1/2 > 1/5$).

$$\frac{1}{\chi^2_{1-\alpha/2}} \ge \frac{\sigma^2}{(n-1)s^2} \ge \frac{1}{\chi^2_{\alpha/2}}$$

Step B: Multiply by the numerator $(n-1)s^2$

Multiply all sides by $(n-1)s^2$ to clear the denominator in the middle. Since variance is always positive, the signs stay the same.

$$\frac{(n-1)s^2}{\chi^2_{1-\alpha/2}} \ge \sigma^2 \ge \frac{(n-1)s^2}{\chi^2_{\alpha/2}}$$

Step C: Rearrange to Standard Order

We usually write intervals from smallest to largest ($Lower < Middle < Upper$).

- The term with the **larger denominator** ($\chi^2_{\alpha/2}$) is the **smaller number** (Lower Bound).
    
- The term with the **smaller denominator** ($\chi^2_{1-\alpha/2}$) is the **larger number** (Upper Bound).
    

$$\frac{(n-1)s^2}{\chi^2_{\alpha/2}} \le \sigma^2 \le \frac{(n-1)s^2}{\chi^2_{1-\alpha/2}}$$

### Summary of the Logic

1. **Start** with the ratio $\frac{(n-1)s^2}{\sigma^2}$.
    
2. **Bound it** between two Chi-Square critical values.
    
3. **Flip it** to solve for $\sigma^2$ (which reverses the inequalities).
    
4. **Result:** The Lower Bound uses the _Right_ critical value (because dividing by a big number gives a small result), and the Upper Bound uses the _Left_ critical value.


Confidence interval we set certain confidence level and then we use sample statistic to infer population parameter. While hypothesis testing, we use sample statistic and population parameter to see whether it fall within the non-rejection region. Both are 1 side of a coin.