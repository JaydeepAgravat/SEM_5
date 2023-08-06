# Probability Distribution

## Random Variable

What are Algebraic Variables?

- In Algebra a variable, like x, is an unknown value.
- x + 5 = 7, x=2

What are Random Variables in Stats and Probability?

- A Random Variable is a set of possible values from a random experiment.
- X = {1,0} <= sample space, coin a toss

Types of Random Variables

1. Discrete Random Variables
2. Continuous Random Variables

## Probability Distributions

What are Probability Distributions?

- A probability distribution is a list of all of the possible outcomes of a random variable
along with their corresponding probability values.

| coin a toss | p(H) | p(T) |
|-------------|------|------|
| probability | 1/2  | 1/2  |

Problem with Distribution?

- In many scenarios, the number of outcomes can be much larger and hence a table would
be tedious to write down.
- Worse still, the number of possible outcomes could be infinite, in which case, good luck writing a table for that.
- Example: Height of people

Solution - Function?

- What if we use a mathematical function to model the relationship between outcome of a  random experiment and probability?
- y = f(x)

Note

- A lot of time Probability Distribution and Probability Distribution Functions are
used interchangeably.

Types of Probability Distributions

1. Discrete
2. Continuous

Famous Probability Distributions

- Bernoulli Distribution
- Binomial Distribution
- Poisson Distribution
- Normal (Gaussian) Distribution
- Exponential Distribution
- Uniform Distribution
- Gamma Distribution
- Chi-Square Distribution
- Student's t-Distribution
- Beta Distribution
- Weibull Distribution
- Logistic Distribution
- Pareto Distribution
- Geometric Distribution
- Negative Binomial Distribution

Why are Probability Distributions important?

- Gives an idea about the shape/distribution of the data.
- If our data follows a famous distribution then we automatically know a lot about the
data.

A note on Parameters

- Parameters in probability distributions are numerical values that determine the shape,
location, and scale of the distribution.
- Different probability distributions have different sets of parameters that determine their shape and characteristics, and understanding these parameters is essential in statistical analysis and inference.

## Probability Distribution Function

- A Probability Distribution Function  is a function that describes the probability of each possible outcome in a random variable.
- It maps the values of the random variable to their respective probabilities.

Types of Probability Distribution Function

1. Probability Mass Function (PMF):
   - Symbol: f(x) or P(X = x)

2. Probability Density Function (PDF):
   - Symbol: f(x) or P(X = x)

## Cumulative Distribution Function (CDF)

- The cumulative distribution function (CDF) F(x) describes the probability that a
random variable X with a given probability distribution will be found at a value less
than or equal to x.
- Symbol: F(x) or P(X ≤ x)

## Probability Mass Function (PMF)

- A Probability Mass Function (PMF) is a function that gives the probability of a discrete random variable taking on a specific value.
- It provides a way to map the values of the random variable to their respective probabilities of occurrence.
- In other words, the PMF tells us how likely each possible outcome is in a discrete distribution.
- The probabilities assigned by the PMF must satisfy two conditions:

1. The probability assigned to each value must be non-negative (i.e., greater
than or equal to zero).
2. The sum of the probabilities assigned to all possible values must equal 1.

Example

| x   | 2    | 3    | 4    | 5    | 6    | 7    | 8    | 9    | 10   | 11   | 12   |
|-----|------|------|------|------|------|------|------|------|------|------|------|
| P(X=x)| 1/36 | 2/36 | 3/36 | 4/36 | 5/36 | 6/36 | 5/36 | 4/36 | 3/36 | 2/36 | 1/36 |

```math
P(X = x) = Number of ways to get x / Total possible outcomes
```

Here is the list of discrete probability distributions:

1. Bernoulli Distribution
2. Binomial Distribution
3. Poisson Distribution
4. Geometric Distribution
5. Negative Binomial Distribution
6. Hypergeometric Distribution
7. Multinomial Distribution
8. Uniform Distribution

## Probability Density Function (PDF)

- PDF is a function used for continuous random variables.
- PDF describes the relative likelihood of the variable taking on different values, the area under the curve gives us the cumulative probability of the variable being within a given interval.
- PDF is a tool for understanding the relative likelihood of different outcomes and for performing probability calculations over intervals.

Calculate Probability

```math
P(a ≤ X ≤ b) = ∫[from a to b] f(x) dx
Where:

P(a ≤ X ≤ b) represents the probability that the continuous random variable X falls within the interval [a, b].
f(x) is the Probability Density Function (PDF) of the continuous random variable X.
```

1. Why Probability Density and why not Probability?
    - Because the number of possible outcomes is infinite (e.g., height, weight, time, etc.).
2. What does the area of this graph represents?
    - P(a ≤ X ≤ b) = ∫[from a to b] f(x) dx
    - By integrating the PDF over a specific interval, we find the probability of the variable falling within that range.
    - The area under the entire curve (i.e., the total area under the entire range of the variable) is always equal to 1, as the sum of all probabilities for all possible outcomes must be 1 for any probability distribution.

Here is a list of continuous probability distributions:

1. Normal Distribution (Gaussian Distribution)
2. Uniform Distribution
3. Exponential Distribution
4. Gamma Distribution
5. Beta Distribution
6. Cauchy Distribution
7. Weibull Distribution
8. Log-Normal Distribution
9. Pareto Distribution
10. Chi-Square Distribution
11. Student's t-Distribution
12. F-Distribution

## Density Estimation

- Density estimation is a statistical technique used to estimate the probability
density function (PDF) of a random variable based on a set of observations or data.
- In simpler terms, it involves estimating the underlying distribution of a set of data
points.
- Density estimation can be used for a variety of purposes, such as hypothesis
testing, data analysis, and data visualization.
- It is particularly useful in areas such
as machine learning, where it is often used to estimate the probability distribution
of input data or to model the likelihood of certain events or outcomes.

Density estimation techniques can be broadly categorized into two main types: parametric and non-parametric approaches.

- Both parametric and non-parametric density estimation approaches have their strengths and weaknesses, and the choice of method depends on the specific characteristics of the data and the goals of the analysis.
- In practice, it's common to use a combination of both approaches to leverage the advantages of each in different parts of the data analysis process.

## Parametric Density Estimation

- Parametric methods assume that the data follows a specific probability distribution with a known functional form, which is characterized by a finite number of parameters.
- The goal is to estimate the parameters of the assumed distribution from the data to construct the PDF.
- Examples of parametric density estimation methods include Maximum Likelihood Estimation (MLE), Method of Moments, and Bayesian estimation.

Advantages:

- If the assumed distribution accurately represents the data, parametric methods can provide efficient and precise density estimates with fewer data points.
- They are computationally less demanding compared to non-parametric methods.

Disadvantages:

- If the data deviates significantly from the assumed distribution, parametric methods can lead to biased density estimates.
- They may not be suitable when the underlying distribution is complex or unknown.

## Non-Parametric Density Estimation

- Non-parametric methods do not assume any specific form for the underlying distribution.
- They aim to estimate the PDF directly from the data without making strong assumptions about the data's distributional form.
- Non-parametric methods are more flexible and can handle a wide range of data distributions.
- Examples of non-parametric density estimation methods include:

1. Kernel Density Estimation (KDE)
2. Histograms
3. K-Nearest Neighbors (KNN)
4. Parzen Windows
5. Local Regression (LOESS)

Advantages:

- Non-parametric methods are more robust and can adapt to various data distributions.
- They can provide accurate density estimates even when the underlying distribution is unknown or complex.

Disadvantages:

- Non-parametric methods may require a larger sample size to provide accurate density estimates, especially in regions with sparse data.
- They can be computationally more demanding, especially for large datasets.

## Kernel Density Estimation (KDE)

Kernel Density Estimation (KDE) is a popular non-parametric method used to estimate the probability density function (PDF) of a continuous random variable based on a set of data points.

It provides a smooth, continuous estimate of the underlying distribution, even when the true form of the distribution is unknown or complex.

Here's a step-by-step explanation of Kernel Density Estimation (KDE):

1. Start with Data:
   - Begin with a set of data points representing the observations of a continuous random variable. Let's call this data set {x₁, x₂, ..., xₙ}.

2. Choose a Kernel:
   - A "kernel" is a smooth, symmetric, and usually bell-shaped function. Common choices include the Gaussian (Normal) kernel or the Epanechnikov kernel.
   - The kernel represents the shape of the probability distribution for each data point.

3. Place a Kernel at Each Data Point:
   - For each data point xᵢ, the kernel is centered at that point.
   - The kernel's bandwidth determines the width of the kernel, influencing the smoothness of the estimated PDF.

4. Sum the Kernels:
   - The next step is to sum up all the individual kernels placed at each data point. This creates a smooth curve that represents the estimated PDF.

5. Choose a Bandwidth:
   - The "bandwidth" parameter controls the width of the kernels and, in turn, the smoothness of the estimated PDF.
   - A larger bandwidth leads to a smoother PDF, while a smaller bandwidth can capture more detailed features in the data but may be noisier.

6. Normalize the Curve:
   - To obtain a valid PDF, the curve needs to be normalized so that the area under the curve equals 1.
   - The normalization ensures that the estimated PDF integrates to 1 over the entire range of the data.

The KDE provides a flexible and non-parametric approach to estimate the probability density function.

It allows us to visualize the data distribution, identify modes and outliers, and approximate the underlying PDF when the true distribution is unknown or difficult to model explicitly.

One of the main advantages of KDE is its ability to smooth out the noise and provide a continuous representation of the data's underlying distribution.

However, choosing an appropriate bandwidth is crucial, as an overly wide or narrow bandwidth can lead to over-smoothing or under-smoothing of the estimated PDF, respectively.

As with any density estimation method, the quality of the estimate depends on the size and quality of the data set used for estimation.

## How to use PDF

- Interpreting the Probability Density Function (PDF) involves understanding the information it provides about the distribution of a continuous random variable.
- The PDF describes the likelihood of the random variable taking on various values within its range.
- Here's how to interpret the PDF:

1. Probability at a specific point:
   - The value of the PDF at a specific point does not give the probability of the random variable being exactly equal to that value, as the probability of a single point in a continuous distribution is zero.
   - Instead, the PDF provides the probability density at that point. The higher the value of the PDF at a particular point, the higher the probability density, indicating that values near that point are more likely to occur.

2. Area under the curve:
   - The total area under the PDF curve represents the total probability of all possible outcomes.
   - For a continuous random variable, the probability of it falling within a particular range is given by the area under the PDF curve over that range.

3. Relative likelihood:
   - Comparing the heights of the PDF at different points allows you to determine which values are more or less likely to occur.
   - Higher peaks indicate higher likelihood, while lower regions indicate lower likelihood.

4. Shape of the distribution:
   - The shape of the PDF curve gives insights into the distribution of the data.
   - Common shapes include symmetric (e.g., normal distribution), skewed (positively or negatively), and uniform.

5. Range of the random variable:
   - The PDF is only defined over the range of the random variable.
   - Outside this range, the probability is zero.

6. Integration for probability calculations:
   - To find the probability of the random variable lying within a specific range, you need to integrate the PDF over that range.
   - The integral of the PDF over an interval gives the probability of the random variable falling within that interval.

7. Expected value:
   - The expected value (mean) of the continuous random variable can be calculated using the PDF.
   - The expected value is the center of mass or the balance point of the distribution.

8. Variance and Standard deviation:
   - The variance and standard deviation of the continuous random variable can also be determined from the PDF.
   - They represent the spread or dispersion of the data around the mean.

Remember, the PDF itself doesn't provide individual probabilities for specific points but gives a continuous representation of the distribution's characteristics.

It's crucial to understand that the PDF is a tool for understanding the relative likelihood of different outcomes and for performing probability calculations over intervals.

## How to use CDF

- Interpreting the Cumulative Distribution Function (CDF) for a continuous random variable involves understanding how it provides information about the probabilities of the random variable taking on values up to a specific point.
- The CDF gives a cumulative view of the distribution and allows you to make probability calculations for continuous random variables.
- Here's how to interpret the CDF:

1. Probability at a specific point:
   - The CDF at a specific point gives the probability that the random variable is less than or equal to that point.
   - In other words, for a continuous random variable X and a given value x, CDF(x) represents P(X ≤ x).

2. Monotonicity:
   - The CDF is a non-decreasing function, meaning it either increases or remains constant as you move along the range of the random variable.
   - It starts at 0 and approaches 1 as the value of the random variable approaches positive infinity.

3. Probability over an interval:
   - To find the probability that the random variable falls within a specific range [a, b], you can calculate the difference between the CDF values at b and a.
   - That is, P(a ≤ X ≤ b) = CDF(b) - CDF(a).

4. Probability density:
   - The derivative of the CDF with respect to the random variable provides the Probability Density Function (PDF).
   - For a continuous random variable, the CDF is a continuous function, and its derivative exists everywhere except at isolated points.

5. Quantiles and percentiles:
   - The CDF is useful for finding quantiles and percentiles of the distribution.
   - For instance, the 50th percentile (also known as the median) is the value at which the CDF equals 0.5.

6. Range of the random variable:
   - The CDF is defined for all real numbers, and its values are within the range [0, 1].
   - CDF(x) = 0 means that the probability of the random variable being less than or equal to x is 0, and CDF(x) = 1 means that the probability is 1.

7. Complementary CDF:
   - The complementary CDF (CCDF) is 1 minus the CDF.
   - It gives the probability that the random variable is greater than a specific value.

The CDF provides a comprehensive view of the distribution and allows you to determine probabilities for individual values as well as for intervals.

It also serves as a foundation for other statistical concepts like hypothesis testing, confidence intervals, and survival analysis. Understanding the CDF is crucial for conducting various analyses and making informed decisions based on continuous random variables.

## 2D Density Plots

- A 2D density plot is a data visualization technique used to display the distribution of data points in a two-dimensional space.
- It represents the density of data points as a color map, contour plot, or heat map, allowing us to observe the concentration of data and identify patterns or trends.
- 2D density plots are particularly useful when visualizing large datasets with overlapping points, enabling better insights into the underlying data distribution and relationships between variables.
- Darker areas or higher contours indicate regions with more data points, while lighter areas or lower contours show sparser regions.
