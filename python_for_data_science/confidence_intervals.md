# Confidence Intervals

## Parameter vs. Statistic

Parameter and statistic are two important concepts in statistics that are used to describe and summarize data.
They are both numerical values, but they have different meanings and roles depending on the context.

Parameter:

1. Definition:
    - A parameter is a numerical value that describes a characteristic of a population.
    - A population refers to the entire group of individuals or items that are of interest in a study. Parameters are often fixed and unknown, representing the true characteristics of the entire population.
2. Notation:
    - Parameters are usually represented by Greek letters (e.g., μ for population mean, σ for population standard deviation, p for population proportion).
3. Estimation:
    - Estimating population parameters often requires data from a sample, and statistical methods are used to infer or estimate these values with a certain level of confidence.

Statistic:

1. Definition:
    - A statistic is a numerical value that describes a characteristic of a sample. A sample is a subset of the population that is selected for study.
    - Statistics are calculated from sample data and are used to make inferences about population parameters.
2. Notation:
    - Statistics are typically represented by Latin letters (e.g., x̄ for sample mean, s for sample standard deviation, ̂p for sample proportion).
3. Role:
    - Statistics serve as estimates or approximations of population parameters. They provide information about the characteristics of the sample and can be used to draw conclusions or make predictions about the population.

In summary, parameters are numerical values that describe characteristics of a population, while statistics are numerical values that describe characteristics of a sample.

Parameters are usually unknown and require estimation, whereas statistics are calculated from sample data and used to make inferences about the population.

## Point Estimate

- Point estimate is a single numerical value that is used to approximate an unknown population parameter based on sample data.
- It is a specific value that provides an estimate of the true parameter value, such as the sample mean used to estimate the population mean or the sample proportion used to estimate the population proportion.
- Point estimates are used to make inferences and draw conclusions about the population based on the information obtained from the sample.
- However, they are not exact and may differ from the true parameter value due to the inherent variability in sampling.

## Confidence Interval

- A confidence interval is a range of values that is constructed around a point estimate (like the sample mean or proportion) to provide a measure of the uncertainty or variability associated with the estimate.
- It is a way to quantify the precision of the estimate and express the level of confidence we have in capturing the true population parameter within that interval.
- A confidence interval is typically defined by two values: an upper limit and a lower limit.
- The interval represents a range of values within which we believe the true population parameter lies with a certain degree of confidence.

For example, if we have a 95% confidence interval for the population mean weight of all apples in a region, it might look like this: [150 grams, 200 grams].

- This means that we are 95% confident that the true population mean weight of apples falls between 150 and 200 grams.

## Confidence Level

- The confidence level is a measure of the long-term frequency of confidence intervals constructed from random samples that will contain the true population parameter.
- A 95% confidence level means that if we take 100 different samples and make confidence intervals for each: The true parameter will be inside the confidence interval 95 out of those 100 times
- It is often expressed as a percentage and represents the long-term frequency with which the constructed confidence intervals would contain the true population parameter if we were to take many samples and calculate many intervals.
- Choosing the confidence level is a trade-off between precision and certainty. Higher confidence levels, such as 95% or 99%, provide wider intervals and more certainty that the true parameter lies within the interval.
- Conversely, lower confidence levels, like 90%, provide narrower intervals but with a reduced level of confidence.
- It is important to note that the confidence level does not refer to the probability of the true parameter being within a particular interval for a specific sample; rather, it relates to the long-term behavior of confidence intervals based on repeated sampling.

In summary, a confidence interval is a range of values around a point estimate that quantifies the uncertainty associated with the estimate, while the confidence level represents the probability that the true population parameter lies within the constructed interval, based on repeated sampling.

The choice of the confidence level depends on the desired level of certainty and the precision required for a particular analysis or study.

## Calculate Confidence Interval

Calculating a confidence interval involves several steps.

The process may vary depending on whether you are estimating the confidence interval for the population mean or population proportion.

Here are the formulas for confidence intervals:

Confidence Interval for Population Mean (σ known):

$$\text{Confidence Interval} = \bar{x} \pm Z \left( \frac{\sigma}{\sqrt{n}} \right)$$

Confidence Interval for Population Mean (σ unknown):

$$\text{Confidence Interval} = \bar{x} \pm t \left( \frac{s}{\sqrt{n}} \right)$$

Confidence Interval for Population Proportion:

$$\text{Confidence Interval} = \hat{p} \pm Z \sqrt{\frac{\hat{p}(1-\hat{p})}{n}}$$

In these formulas:

- x̄ represents the sample mean.
- σ is the known population standard deviation.
- s is the sample standard deviation.
- Z is the Z-score critical value associated with the desired confidence level.
- t is the t-score critical value associated with the desired confidence level/
- p represents the sample proportion for the population proportion confidence interval.
- n is the sample size.

### 1. Confidence Interval for Population Mean (σ known)

When the population standard deviation (σ) is known and you want to estimate the confidence interval for the population mean (μ):

1. Collect Sample Data
    - Obtain a random sample from the population.
    - The sample should be representative of the population of interest.

2. Calculate the Sample Mean (x̄)
    - Compute the mean of the sample data, which is denoted by x̄.

3. Determine the Z-Score
    - Find the Z-score corresponding to the desired confidence level.
    - For example, if you want a 95% confidence interval, the Z-score is approximately 1.96 (for a standard normal distribution).

4. Calculate the Margin of Error
    - The margin of error (E) is given by the formula: E = Z * (σ / √n), where Z is the Z-score, σ is the known population standard deviation, and n is the sample size.

5. Compute the Confidence Interval
    - The confidence interval is given by: (x̄ - E, x̄ + E).
    - This interval represents the range within which we are confident that the true population mean lies with the specified confidence level.

### 2. Confidence Interval for Population Mean (σ unknown)

When the population standard deviation (σ) is unknown and you want to estimate the confidence interval for the population mean (μ):

1. Collect Sample Data
    - Obtain a random sample from the population.
    - The sample should be representative of the population of interest.

2. Calculate the Sample Mean (x̄)
    - Compute the mean of the sample data, which is denoted by x̄.

3. Determine the T-Score
    - Find the T-score corresponding to the desired confidence level and degrees of freedom (df = n - 1), where n is the sample size.
    - The T-score is obtained from the Student's t-distribution table or using statistical software.

4. Calculate the Standard Error
    - The standard error (SE) is given by the formula: SE = (s / √n), where s is the sample standard deviation.

5. Calculate the Margin of Error
    - The margin of error (E) is given by: E = T * SE, where T is the T-score.

6. Compute the Confidence Interval
    - The confidence interval is given by: (x̄ - E, x̄ + E).
    - This interval represents the range within which we are confident that the true population mean lies with the specified confidence level.

### 3. Confidence Interval for Population Proportion

When you want to estimate the confidence interval for a population proportion (p):

1. Collect Sample Data
    - Obtain a random sample from the population. The sample should be representative of the population of interest.

2. Calculate the Sample Proportion (p̂)
    - Compute the proportion of successes in the sample, which is denoted by p̂.

3. Determine the Z-Score
    - Find the Z-score corresponding to the desired confidence level.
    - For example, if you want a 95% confidence interval, the Z-score is approximately 1.96 (for a standard normal distribution).

4. Calculate the Standard Error
    - The standard error (SE) for a population proportion is given by: SE = √(p̂ * (1 - p̂) / n), where n is the sample size.

5. Calculate the Margin of Error
    - The margin of error (E) is given by: E = Z * SE, where Z is the Z-score.

6. Compute the Confidence Interval
    - The confidence interval is given by: (p̂ - E, p̂ + E).
    - This interval represents the range within which we are confident that the true population proportion lies with the specified confidence level.

The higher the confidence level, the wider the confidence interval will be, capturing more uncertainty and providing greater confidence in the estimate.

### Condition For σ Known

Condition:

To construct a confidence interval for the population mean (μ) when the population standard deviation (σ) is known, you need to meet the following conditions:

1. Simple Random Sample:
    - The data should be collected using a simple random sampling method, where each individual in the population has an equal chance of being selected.

2. Normality:
    - The sampling distribution of the sample mean (x̄) should be approximately normally distributed. This condition is satisfied if the sample size is large enough (typically, n ≥ 30) due to the central limit theorem, even if the underlying population distribution is not exactly normal.

3. Known Population Standard Deviation (σ):
    - The population standard deviation (σ) must be known and provided as part of the problem or data. If it is not known, you cannot use this method, and you need to use the confidence interval for the population mean with σ unknown.

### Condition For σ Unknown

Condition:

To construct a confidence interval for the population mean (μ) when the population standard deviation (σ) is unknown, you need to meet the following conditions:

1. Simple Random Sample:
    - The data should be collected using a simple random sampling method, where each individual in the population has an equal chance of being selected.

2. Normality or Sufficient Sample Size:
    - The sampling distribution of the sample mean (x̄) should be approximately normally distributed, which is true when the sample size is large (typically, n ≥ 30) due to the central limit theorem.
    - If the sample size is small and the population is not approximately normally distributed, you should use other methods, such as bootstrapping or non-parametric approaches.

3. Unknown Population Standard Deviation (σ):
    - In this case, the population standard deviation (σ) is not known and needs to be estimated from the sample data.

### Condition For Population Proportion

Condition:

To construct a confidence interval for the population proportion (p), you need to meet the following condition:

1. Random Sample:
    - The data should be collected using a random sampling method, where each individual in the population has an equal chance of being selected.

2. Binary Outcome:
    - The variable of interest should be binary or categorical with two possible outcomes, such as success/failure, yes/no, or present/absent.

3. Independence:
    - The individual observations in the sample should be independent of each other. If the sampling process is done without replacement, the sample size should be small relative to the population size (usually considered satisfied if n ≤ 0.05N, where N is the population size).

4. Sufficient Successes and Failures:
    - The sample should have sufficient successes and failures to satisfy the requirements of using normal approximation methods. In practice, this is often achieved when both np and n(1-p) are greater than 5, where n is the sample size, and p is the sample proportion.

## Imp Topic For σ known

$$\text{Confidence Interval} = \bar{x} \pm Z \left( \frac{\sigma}{\sqrt{n}} \right)$$

Effect on Confidence Interval:

- When the sample mean (x̄) increases, the upper bound of the confidence interval increases, and the lower bound increases as well. This leads to a wider confidence interval.
- As the confidence level increases (e.g., from 90% to 95% or 99%), the Z-score increases. A higher Z-score leads to a wider confidence interval because it includes a larger proportion of the area under the normal distribution curve.
- As the sample size (n) increases, the standard error (σ/√n) decreases. A larger sample size reduces the uncertainty associated with the sample mean (x̄) and leads to a narrower confidence interval.

## Imp Topic For σ Unknown

$$\text{Confidence Interval} = \bar{x} \pm t \left( \frac{s}{\sqrt{n}} \right)$$

- When the sample mean (x̄) increases, the upper bound of the confidence interval increases, and the lower bound increases as well. This leads to a wider confidence interval.
- As the confidence level increases (e.g., from 90% to 95% or 99%), the t-score increases. A higher t-score leads to a wider confidence interval because it includes a larger proportion of the t-distribution's area.
- A larger sample standard deviation leads to a wider confidence interval because it increases the uncertainty associated with the sample mean (x̄).
- As the sample size (n) increases, the standard error (s/√n) decreases. A larger sample size reduces the uncertainty associated with the sample mean (x̄) and leads to a narrower confidence interval.

## Student's T-Distribution

- The Student's t-distribution, often referred to simply as the t-distribution, is a probability distribution used in statistics for making inferences about the population mean when the sample size is small or when the population standard deviation is unknown.

Key characteristics of the Student's t-distribution:

1. Shape:

    - The t-distribution is similar in shape to the standard normal (Z) distribution but has heavier tails.
    - As the sample size increases, the t-distribution approaches the standard normal distribution.

2. Symmetry and Centering:

    - The t-distribution is symmetric about the mean of 0 (centered at 0).
    - It has a mean of 0 and a median of 0.

3. Degrees of Freedom:

    - The shape of the t-distribution is determined by a parameter called degrees of freedom (df).
    - The degrees of freedom depend on the sample size (n) and play a crucial role in the distribution's properties.
    - The greater the degrees of freedom, the closer the t-distribution resembles the standard normal distribution.

4. Probability density function (pdf):

    $$
    f(t) = \frac{\Gamma\left(\frac{df+1}{2}\right)}{\sqrt{df\pi} \cdot \Gamma\left(\frac{df}{2}\right)} \left(1 + \frac{t^2}{df}\right)^{-\frac{df+1}{2}}
    $$

    - t: The random variable representing the t-score.
    - df: Degrees of freedom.
    - Γ: The gamma function.

5. Use in Hypothesis Testing and Confidence Intervals:

    - The t-distribution is widely used in hypothesis testing and constructing confidence intervals for population mean when the sample size is small (typically n < 30) or when the population standard deviation is unknown.
    - It accounts for the additional uncertainty introduced by estimating the population standard deviation from the sample data.

6. Relationship with the Z-Distribution:

    - When the sample size is large (n ≥ 30) and the population standard deviation is known, the t-distribution approaches the standard normal (Z) distribution.
    - For large sample sizes, using the t-distribution and the Z-distribution yield similar results.

7. Critical Values:

    - Critical values from the t-distribution are commonly used to determine the rejection regions in t-tests, which are used to test hypotheses about the population mean.

The Student's t-distribution plays a crucial role in inferential statistics when dealing with small sample sizes and uncertainty in population parameters.

It provides a robust framework for making inferences about the population mean, particularly when the assumptions of normality and known population standard deviation are not met.
