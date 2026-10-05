## Multinomial experiment

It is same with binomial experiment but each trial we have $k$ outcome where $k> 2$.

Results from a multinomial experiment can be categorized under one attribute in a one-way table

![[Pasted image 20260130162839.png]]


## A goodness-of-fit test

It is a test that concern about if the outcome in a multinomial experiment equally likely to be choose. (Close to theoretical probability)

It concern about the frequency distribution.

$df=k-1$
## Two-way Table

When data is categorized under two attributes and tabulated, the result is a two-way table(or also known as a contingency table or cross-tabulation).


![[Pasted image 20260130163302.png]]


The frequencies obtained from the experiment are called the observed frequencies and are denoted as 𝑂.
The expected frequencies, denoted by 𝐸, are the frequencies that we expect to obtain if the null hypothesis is true.
$E=np$

where $n$ is the sample size and $p$ is the probability if the null hypothesis is true.

==Hypothesis==
$H_{0}$: The probabilities for each cell are $p_{1},p_{2},\dots,p_{k}$
$H_{1}$: The probabilities for each cell are not $p_{1},p_{2},\dots,p_{k}$

==Test Statistics==
$$
X^{2}=\sum \frac{(O-E)^{2}}{E}
$$
df=k-1
The number of column - 1


Thus, a chi-square goodness-of-fit test is always a RTT.

The sample size should be large enough so that the expected frequency for each cell is at least 5.
## An independence test
Question:
Are the two attributes in the contingency table related (dependent) or not related (independent)?

![[Pasted image 20260130171123.png]]

We need to find test statistic for each cell and sum up together , and the expected frequency is $E$ using the given formula.

Like a goodness-of-fit test, a test of independence is always right-tailed, and the sample size should be large enough so that the expected frequency for each cell is at least 5.

==Hypothesis==
$H_{0}$: The row factor is independent of (not related to) the column factor
$H_{1}$: The row factor is dependent of (related to)the column factor

The logic behind this formula comes directly from the probability rule for **independent events**.

In a Chi-Square Test of Independence, the "Expected Count" ($E$) is a hypothetical number. It answers the question: _"If the two variables were completely unrelated (independent), how many observations would we expect to see in this specific cell?"_

Here is the step-by-step derivation of why that specific formula works.

---

### 1. The Probability of Independence

In probability theory, two events ($A$ and $B$) are defined as **independent** if the probability of both happening at the same time is equal to the product of their individual probabilities:

$$P(A \text{ and } B) = P(A) \times P(B)$$

### 2. Translating to a Contingency Table

Imagine you have a table of data with a total sample size of $N$. You want to find the expected count for a specific cell that sits at the intersection of a specific **Row** and a specific **Column**.

First, we calculate the individual probabilities based on the totals:

- **Probability of being in this Row:**
    
    $$P(\text{Row}) = \frac{\text{Row Total}}{N}$$
    
- **Probability of being in this Column:**
    
    $$P(\text{Column}) = \frac{\text{Column Total}}{N}$$
    

### 3. Applying the Independence Rule

If the Null Hypothesis is true (meaning the variables are independent), then the probability of a data point falling into that specific cell (intersection of the Row and Column) is:

$$P(\text{Cell}) = P(\text{Row}) \times P(\text{Column})$$

$$P(\text{Cell}) = \frac{\text{Row Total}}{N} \times \frac{\text{Column Total}}{N}$$

### 4. Converting Probability to a Count

The formula above gives us a _percentage_ (or probability). To get the actual **Expected Count** ($E$), we must multiply that percentage by the total number of people in the sample ($N$):

$$E = P(\text{Cell}) \times N$$

Substitute the probabilities we found in Step 3:

$$E = \left( \frac{\text{Row Total}}{N} \times \frac{\text{Column Total}}{N} \right) \times N$$

### 5. Simplifying the Algebra

Now, we just simplify the equation. One of the $N$s in the denominator cancels out the $N$ in the numerator:

$$E = \frac{\text{Row Total} \times \text{Column Total}}{N \times \bcancel{N}} \times \bcancel{N}$$

**Leaving you with the final formula:**

## A homogeneity test
Question:
Are the proportions of elements with certain characteristics in two or more populations the same?

==Hypothesis==
$H_{0}$: The distribution proportion within (row) is the same for all column 
$H_{1}$: .... are not same

The test procedure for independence and homogeneity tests are the same, except for the hypotheses and conclusion.


| **Feature**  | **Test of Independence**                                                                                 | **Test of Homogeneity**                                                                            |
| ------------ | -------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------- |
| **Sampling** | **One single sample** is taken from one large population. You then categorize everyone by two variables. | **Separate samples** are taken from different populations (e.g., 100 people from NY, 100 from LA). |
| **Goal**     | To see if two variables are related (associated).                                                        | To see if different populations possess the same traits.                                           |
| **Example**  | Survey 500 people and ask: "Do you smoke?" and "Do you have asthma?"                                     | Survey 200 Smokers and 200 Non-Smokers and ask both groups: "Do you have asthma?"                  |
| **Math**     | Uses the same $\frac{Row \times Column}{Total}$ formula.                                                 | Uses the same $\frac{Row \times Column}{Total}$ formula.                                           |

The **Test of Homogeneity** is a Chi-Square test used to determine if two or more distinct populations share the same distribution of a single categorical variable

