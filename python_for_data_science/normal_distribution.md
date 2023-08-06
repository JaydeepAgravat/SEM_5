# Normal Distribution

What is normal distribution?

- Normal distribution, also known as Gaussian distribution, is a probability distribution that is commonly used in statistical analysis.
- It is a continuous probability distribution that is symmetrical around the mean, with a bell-shaped curve.
- Asymptotic in nature.
- Lots of points near the mean and very few far away.
- The normal distribution is characterized by two parameters: the mean (μ) and the
standard deviation (σ).
- The mean represents the centre of the distribution, while the standard deviation represents the spread of the distribution.
- Denoted as: X ~ N(μ,σ)

Why is it so important?

- Commonality in Nature: Many natural phenomena follow a normal distribution, such as the heights of people, the weights of objects, the IQ scores of a population, and many more.
- Thus, the normal distribution provides a convenient way to model and analyse such
data.

PDF Equation of Normal Distribution:

    ```python
    f(x; μ, σ) = (1 / (σ * √(2π))) * e^(-((x - μ)^2 / (2 * σ^2)))

    Equation Detail: y=e^(-x^2)
    ```

Parameters in Normal Distribution:

- If the mean increases, the whole distribution shifts to the right, and vice versa for a decrease in the mean.
- If the standard deviation increases, the distribution becomes more spread out, and vice versa for a decrease in the standard deviation.
- The mean influences the center and symmetry of the normal distribution, while the standard deviation impacts its spread and shape.

## Standard Normal distribution

- A Standard Normal distribution is a standardized form of the normal distribution with mean = 0 and standard deviation = 1.
- Standardizing a normal distribution allows us to compare different distributions with each other, and to calculate probabilities using standardized tables or software.

Equation:

    ```python
    f(z) = (1 / √(2π)) * e^(-z^2 / 2)
    ```

- To transform a normal distribution to Standard Normal distribution we use
Standard Normal Variate [Z = (x-μ/σ)].
- The Standard Normal Variate, also known as the Z-score.

Suppose the heights of adult males in a certain population follow a normal distribution with a mean of 68 inches and a standard deviation of 3 inches. What is the probability that a randomly selected adult male from this population is taller than 72 inches?

    ```python
    We need to calculate P(X > 72).

    First, we standardize the value 72 using the Z-score formula:

    Z = (X - μ) / σ

    where X = 72, μ = 68, and σ = 3.

    Z = (72 - 68) / 3 = 4 / 3 ≈ 1.3333

    P(Z > 1.3333) ≈ 0.0912
    ```

What are Z-tables

- A z-table tells you the area underneath a normal distribution curve, to the left of the z-score.

## Properties of Normal Distribution

1. Symmetricity
    - The normal distribution is symmetric about its mean, which means that the probability of observing a value above the mean is the same as the probability of observing a value below the mean.
    - The bell-shaped curve of the normal distribution reflects this symmetry.

2. Measures of Central Tendencies are equal

3. Empirical Rule
    - The normal distribution has a well-known empirical rule, also called the 68-95-99.7 rule,
    - which states that approximately 68% of the data falls within one standard deviation of the mean, about 95% of the data falls within two standard deviations of the mean, and about 99.7% of the data falls within three standard deviations of the mean.

4. The area under the curve is 1.

## Skewness

- Skewness is a measure of the asymmetry of a probability distribution.
- It is a statistical measure that describes the degree to which a dataset deviates from the normal distribution.
- In a symmetrical distribution, the mean, median, and mode are all equal.
- In contrast, in a skewed distribution, the mean, median, and mode are not equal, and the distribution tends to have a longer tail on one side than the other.
- Skewness can be positive, negative, or zero.
- A positive skewness means that the tail of
the distribution is longer on the right side, while a negative skewness means that the tail
is longer on the left side.
- A zero skewness indicates a perfectly symmetrical distribution.
- The greater the skew the greater the distance between mode, median and mode.

How skewness is calculated?

    ```python
    Sample Skewness = [(∑(xi - x̄)^3) / (n * s^3)]
    Population Skewness = [(∑(xi - μ)^3) / (N * σ^3)]
    ```

## CDF of Normal Distribution

- The Cumulative Distribution Function (CDF) of the normal distribution produces an S-shaped curve.
- The CDF of the normal distribution is an essential tool for calculating probabilities associated with a specific range of values or for finding percentiles of the distribution.
- It allows us to assess the likelihood of observing values up to a certain point in the normal distribution.
- Increasing μ shifts the entire CDF to the right.
- Increasing the standard deviation results in a broader CDF curve that covers a wider range of values, as the data becomes more spread out & and a higher likelihood of observing extreme values.the probability of observing values close to the mean decreases.
- Decreasing the standard deviation in a normal distribution implies a narrower spread of data points and a higher likelihood of observing values close to the mean. The probability of observing extreme values decreases.

Use of Normal Distribution in Data Science:

- Outlier detection
- Assumptions on data for ML algorithms (Linear Regression and GMM)
- Hypothesis Testing
- Central Limit Theorem
