# Non-Gaussian Probability Distributions

## Kurtosis

- Kurtosis is the 4th statistical moment. In probability theory and statistics, kurtosis
(meaning "curved, arching") is a measure of the "tailedness" of the probability
distribution of a real-valued random variable.
- Like skewness, kurtosis describes a
particular aspect of a probability distribution.
- A higher kurtosis indicates fatter tails in the distribution, meaning there is a greater probability of extreme values, both positive and negative.
- A negative kurtosis suggests a flatter distribution, meaning there is a fewer extreme values, both positive and negative.

Excess kurtosis, also known as "kurtosis excess" or simply "excess," refers to the kurtosis value minus 3.

There are three main types of Excess Kurtosis:

1. Mesokurtic:
    - If the kurtosis value is zero, the distribution is considered mesokurtic.
    - This means the distribution has a shape similar to a normal distribution, and the tails are neither too heavy nor too light.

2. Leptokurtic:
    - When the kurtosis value is positive, the distribution is leptokurtic.
    - This indicates that the distribution has fatter tails and is more peaked around the mean than a normal distribution.
    - In other words, it has a higher probability of extreme values, making it riskier.

3. Platykurtic:
    - A negative kurtosis value indicates a platykurtic distribution.
    - This means the distribution has lighter tails and is flatter around the mean compared to a normal distribution.
    - It is less risky and has fewer extreme values.

## QQ Plot

- A QQ plot (quantile-quantile plot) is a graphical tool used to assess the similarity of the distribution of two sets of data.
- It is useful for determining whether a set of data follows  a particular theoretical distribution.
- In a QQ plot, the quantiles of the two sets of data are plotted against each other. The
quantiles of one set of data are plotted on the x-axis, while the quantiles of the other
set of data are plotted on the y-axis. If the two sets of data have the same distribution, the points on the QQ plot will fall on a straight line. If the two sets of
data do not have the same distribution, the points will deviate from the straight line.

## Uniform Distribution

- A uniform distribution is a type of probability distribution where every possible outcome within a specific range has an equal probability of occurring.
- It is a continuous probability distribution, meaning that the random variable can take on any value within a given interval with equal likelihood.

Key characteristics of the uniform distribution:

1. Probability density function (pdf):

    - The probability density function of a uniform distribution is defined as:

    $$
    f(x) = \begin{cases}
    \frac{1}{b - a}, & \text{for } a \leq x \leq b \\
    0, & \text{otherwise}
    \end{cases}
    $$

    - a: The minimum value of the range (lower bound).
    - b: The maximum value of the range (upper bound).

2. Cumulative distribution function (cdf):

    - The cumulative distribution function for the uniform distribution is a linear function:

    $$
    F(x) = \begin{cases}
    0, & \text{for } x < a \\
    \frac{x - a}{b - a}, & \text{for } a \leq x \leq b \\
    1, & \text{for } x > b
    \end{cases}
    $$

3. Mean and variance:

    - The mean (expected value) of a uniform distribution is the average of the lower and upper bounds:

    $$
    Mean = (a + b) / 2
    $$

    - The variance of the uniform distribution is given by:

    $$
    Variance = (b - a)^2 / 12
    $$

4. Support:

    - The support of the uniform distribution is the interval [a, b], which represents the range of possible outcomes.

5. Equal probability density:

    - In a uniform distribution, all points within the range have an equal probability density, which means that the probability of an outcome falling within any subinterval of the range is proportional to the length of that subinterval.

6. Rectangular probability density function:

    - The probability density function of a uniform distribution is represented graphically as a rectangle with a constant height (1 / (b - a)) over the interval [a, b]. The area under the rectangle is equal to 1, representing the total probability of all possible outcomes.

Applications of the uniform distribution:

- Generating random numbers for simulations and Monte Carlo methods.
- In statistical sampling techniques when a random sample is needed.
- Modeling situations where each outcome in a given range is equally likely, such as selecting a random day of the week, rolling a fair dice, or selecting a random point within a given area.

The uniform distribution is straightforward and has many practical applications, especially in situations where there is an equal chance of any value within a specific range occurring.

## Log Normal Distribution

- The log-normal distribution is a continuous probability distribution used to model positive-valued random variables that have skewed, right-skewed, or positively skewed distributions.
- It is often used to model data that is expected to be multiplicative, where the logarithm of the data follows a normal distribution.
- The log-normal distribution is widely used in various fields, including finance, economics, biology, and engineering.

Key characteristics of the log-normal distribution:

1. Probability density function (pdf):

    - The probability density function of the log-normal distribution is defined as:

    $$
    f(x) = \frac{1}{x \sigma \sqrt{2\pi}} \cdot \exp\left(-\frac{(\ln(x) - \mu)^2}{2\sigma^2}\right)
    $$

    - x: The random variable (x > 0).
    - μ: The mean of the natural logarithm of the data (location parameter).
    - σ: The standard deviation of the natural logarithm of the data (scale parameter).

2. Cumulative distribution function (cdf):

    - The cumulative distribution function of the log-normal distribution does not have a closed-form expression, but it can be calculated numerically.

3. Log-Normal vs. Normal distribution:

    - The log-normal distribution is related to the normal distribution, but it is not the same.
    - While the normal distribution is symmetric and centered around its mean, the log-normal distribution is right-skewed due to the exponential transformation.

4. Transforming back to the original scale:

    - If a random variable Y follows a log-normal distribution with parameters μ and σ, then the variable X, which is the exponential of Y (X = exp(Y)), follows a normal distribution with mean and standard deviation given by:

    $$
    Mean = \exp\left(\mu + \frac{\sigma^2}{2}\right)
    $$

    $$
    Variance = \left(\exp(\sigma^2) - 1\right) \cdot \exp\left(2\mu + \sigma^2\right)
    $$

5. Interpretation of parameters:
   - μ (mean of the logarithm): It determines the location of the peak of the distribution on the logarithmic scale.
   - σ (standard deviation of the logarithm): It controls the spread or width of the distribution on the logarithmic scale. Larger values of σ result in broader, more dispersed distributions.

6. Logarithmic scale:
    - The name "log-normal" comes from the fact that taking the natural logarithm of the data transforms it into a normal distribution.
    - This transformation is essential in many statistical analyses and applications.

Applications of the log-normal distribution:

- The log-normal distribution is commonly used in finance to model asset returns, stock prices, and interest rates, as these quantities are often multiplicative in nature.
- It is also used in biology to model the size of biological organisms or populations, in hydrology for modeling flood flows, in engineering for modeling time to failure of components, and in other fields where the underlying data is expected to be positively skewed.

The log-normal distribution is a useful and flexible distribution that provides a good fit for many real-world datasets with positive skewness. However, like any statistical model, it should be applied with caution, and the appropriateness of the log-normal assumption should be verified through statistical tests and data analysis.

## Pareto Distribution

- The Pareto distribution is a continuous probability distribution used to model heavy-tailed phenomena, where a small number of extreme values have a disproportionate impact on the overall distribution.

Key characteristics of the Pareto distribution:

1. Probability density function (pdf):

    - The probability density function of the Pareto distribution is defined as:

    $$
    f(x) = \frac{\alpha \cdot x_m^\alpha}{x^{\alpha + 1}}
    $$

    - x: The random variable (x > x_m).
    - x_m: The minimum value of the distribution, also known as the scale parameter or lower bound.
    - α: The shape parameter, which controls the tail behavior of the distribution. α > 0.

2. Cumulative distribution function (cdf):

    - The cumulative distribution function of the Pareto distribution is given by:

    $$
    F(x) = 1 - \left(\frac{x_m}{x}\right)^\alpha
    $$

3. Power-law relationship:

    - The Pareto distribution follows a power-law relationship, meaning that the tail of the distribution decreases according to a power function.
    - The power-law tail is what gives the distribution its heavy-tailed characteristic.

4. Scale-free property:

    - The Pareto distribution is scale-free, which means it does not have a fixed scale or characteristic size.
    - It has infinite variance for α ≤ 2 and finite variance for α > 2.

5. Relationship to Pareto Principle (80-20 Rule):
    - The Pareto distribution is related to the Pareto Principle or the 80-20 rule, which states that roughly 80% of the effects come from 20% of the causes.
    - While the Pareto Principle is an observation about real-world phenomena, the Pareto distribution can be used to model situations that exhibit this kind of unequal distribution.

6. Tail behavior:

    - High values of α:

        - When α is large, the distribution has a relatively lighter tail.
        - This means that extreme events occur less frequently, and the distribution decays more rapidly as x increases.

    - Low values of α:
        - When α is small, the distribution has a heavier tail, and extreme events occur more frequently.
        - The distribution decays slowly as x increases, resulting in a higher probability of observing extreme values.

Application:

- The Pareto distribution is used in various fields to model phenomena with extreme events or heavy-tailed behavior.
- It finds applications in economics (income distribution, wealth distribution), finance (extreme value analysis, insurance claims), network science (degree distribution in complex networks), and other areas where a small number of extreme events dominate the overall behavior.

It's important to note that the Pareto distribution is only valid for positive values of x, and it has a heavy tail that stretches out to infinity, making it a useful tool for analyzing extreme events or outliers in data. The shape parameter α determines the degree of heaviness in the tail: higher values of α lead to lighter tails, while lower values indicate more extreme events.

## Bernoulli distribution

- The Bernoulli distribution is one of the simplest and most fundamental discrete probability distributions.
- It models a random experiment with only two possible outcomes: success and failure.

Key characteristics of the Bernoulli distribution:

1. Probability mass function (pmf):

    - The probability mass function of the Bernoulli distribution is defined as:

    $$
    P(X = x) = p^x * (1 - p)^(1-x)
    $$

    - X: The random variable representing the outcome of the experiment (0 for failure, 1 for success).
    - p: The probability of success, where 0 ≤ p ≤ 1.

2. Mean and variance:
    - The mean (expected value) of the Bernoulli distribution is given by:
    $$
    Mean(X) = p
    $$
    - The variance of the Bernoulli distribution is given by:
    $$
    Variance(X) = p * (1 - p)
    $$

3. Support:
    - The support of the Bernoulli distribution is {0, 1}, representing the two possible outcomes: failure (0) and success (1).

4. Relationship to the Binomial distribution:
    - The Bernoulli distribution is a special case of the Binomial distribution with n=1 (a single trial).
    - If we repeat the Bernoulli experiment multiple times (n trials), the Binomial distribution arises to model the number of successes in those n trials.

5. Independence assumption:
    - For a sequence of Bernoulli trials (success/failure experiments), the trials are assumed to be independent of each other.
    - This means that the outcome of one trial does not affect the outcome of the others.

Application:

- The Bernoulli distribution is commonly used to model binary events or experiments with two possible outcomes.
- Examples include coin flips (heads or tails), success or failure in a single trial, yes/no questions, and many other situations where there are only two mutually exclusive possibilities.

The Bernoulli distribution is a fundamental building block for more complex distributions, such as the Binomial, Geometric, and Negative Binomial distributions. It serves as the foundation for understanding the behavior of random experiments with binary outcomes.

## Binomial Distribution

- The Binomial distribution is a discrete probability distribution that models the number of successes in a fixed number of independent Bernoulli trials.
- Each trial can have only two possible outcomes: success with probability "p" or failure with probability "q" (where q = 1 - p).
- The Binomial distribution is widely used in various fields, such as statistics, genetics, finance, and quality control.

Key characteristics of the Binomial distribution:

1. Probability mass function (pmf):
    - The probability mass function of the Binomial distribution is defined as:

    $$
    P(X = k) = C(n, k) * p^k * (1 - p)^(n - k)
    $$

    - X: The random variable representing the number of successes in "n" trials.
    - k: The number of successes (0, 1, 2, ..., n).
    - n: The total number of trials.
    - p: The probability of success in each individual trial.

2. Mean and variance:
    - The mean (expected value) of the Binomial distribution is given by:

    $$
    Mean(X) = n * p
    $$

    - The variance of the Binomial distribution is given by:

    $$
    Variance(X) = n * p * (1 - p)
    $$

3. Support:
    - The support of the Binomial distribution is {0, 1, 2, ..., n}, representing the possible number of successes in "n" trials.

4. Independence assumption:
    - The Binomial distribution assumes that each trial is independent of the others.
    - This means that the outcome of one trial does not affect the outcome of the others.

5. Relationship to the Bernoulli distribution:

    - The Binomial distribution is a generalization of the Bernoulli distribution.
    - If we conduct a single trial (n=1) and count the number of successes, we get a Bernoulli distribution.
    - The Binomial distribution with n=1 is equivalent to a Bernoulli distribution.

6. Approximation:
    - The Binomial distribution can be approximated by the Normal distribution when "n" is large, and both "np" and "n(1-p)" are sufficiently large.
    - This is known as the Normal approximation to the Binomial distribution.

Application:

- The Binomial distribution is commonly used to model situations where there are a fixed number of independent trials, and each trial has two possible outcomes. Examples include:
- The number of successes in a fixed number of coin flips (heads or tails).
- The number of defective items in a fixed number of sampled items during quality control.
- The number of individuals with a specific genetic trait in a fixed-size population.

The Binomial distribution is a fundamental and versatile distribution used in statistical inference, hypothesis testing, and many real-world applications. It provides a simple yet powerful model for understanding the behavior of discrete random experiments with binary outcomes.
