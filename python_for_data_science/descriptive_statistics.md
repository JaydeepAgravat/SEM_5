# Statistics

## What is Statistics ?

- Statistics is a branch of mathematics and a field of study that deals with collecting, organizing, analyzing, interpreting, and presenting data.
- Its primary goal is to gain insights and make smart decisions using data.
- Statistics plays a crucial role in various disciplines, including data science, economics, social sciences, medicine, engineering, and more.
- By using statistical techniques effectively, data scientists can extract meaningful insights from data, draw reliable conclusions, and communicate their findings in a clear and informative manner.

## Statistics Applications

1. Medical Research: Statistics is used to analyze clinical trial data to determine the effectiveness of new drugs or treatments. It helps researchers understand the impact of a treatment on patients and draw conclusions about its safety and efficacy.

2. Market Research: Companies use statistics to analyze consumer data, conduct surveys, and gather feedback to make informed decisions about product development, pricing strategies, and marketing campaigns.

3. Economics: Economists use statistics to analyze economic data, such as GDP, inflation rates, and unemployment rates, to understand the overall health of the economy and identify trends.

4. Quality Control in Manufacturing: Statistics is used to monitor and control the quality of products in manufacturing processes. It helps identify defects and variations, ensuring products meet quality standards.

5. Finance and Investment: Statistical models are used in finance to analyze stock market trends, portfolio performance, and risk assessment. It helps investors make informed decisions about their investments.

6. Education: In education, statistics is used to analyze student performance data, evaluate the effectiveness of teaching methods, and identify areas for improvement.

7. Environmental Science: Statistics is used to analyze environmental data, such as air and water quality measurements, to understand the impact of pollution and climate change.

8. Sports Analytics: Statistics is widely used in sports to analyze player performance, team strategies, and game outcomes. It helps coaches and teams make data-driven decisions.

9. Social Sciences: Researchers in psychology, sociology, and other social sciences use statistics to analyze survey data, conduct experiments, and draw conclusions about human behavior and social trends.

10. Public Health: Epidemiologists use statistics to study disease outbreaks, track the spread of infections, and assess the effectiveness of public health interventions.

## Types of Statistics

1. Descriptive Statistics

    - Descriptive statistics involve methods used to summarize and describe data through measures such as mean, median, mode, standard deviation, and graphs like histograms or scatter plots.

    - These techniques help us understand the main features of the data, identify patterns, and gain initial insights.

    - Suppose we have the heights (in centimeters) of ten students in a class:

    - [170, 165, 172, 175, 160, 168, 180, 158, 162, 167]

    - Using descriptive statistics, we can calculate the following measures:

    - Mean: (170 + 165 + 172 + 175 + 160 + 168 + 180 + 158 + 162 + 167) / 10 = 167.7 cm

    - Standard Deviation: Approximately 7.5 cm

    - Median: 167 cm

    - Mode: There is no mode as all values are unique.

    - These descriptive statistics summarize the central tendency (mean, median), spread (standard deviation), and frequency (mode) of the heights in the class.

2. Inferential Statistics

    - Inferential statistics deals with drawing conclusions or making predictions about a larger population based on a smaller sample of data.

    - This involves using probability theory to quantify the uncertainty associated with our estimates.

    - Hypothesis testing is a crucial part of inferential statistics, where we assess the validity of assumptions and make decisions based on the evidence from sample data.

    - Suppose we want to know the average height of all students in the school based on the heights of the ten students we measured.

    - We can use inferential statistics to estimate this population parameter.

    - We can perform a hypothesis test or construct a confidence interval using the sample data to make inferences about the population.

    - Hypothesis Testing: We can test the hypothesis that the average height of all students in the school is 170 cm (a common value).

    - Confidence Interval: We can calculate a 95% confidence interval for the average height, e.g., (162 cm, 173 cm).

    - These inferential statistics allow us to make educated guesses or draw conclusions about the larger population based on the information from the sample data.

## Population vs Sample

Population:

- In statistics, a population refers to the entire group of individuals, objects, or observations of interest that share a common characteristic.

- It is the complete set from which data is collected, and it represents the entire target group about which we want to make inferences or draw conclusions.

- For example, if we are interested in studying the average income of all adults in a country, the population would consist of every adult (i.e., all individuals aged 18 and above) in that country.

Sample:

- A sample, on the other hand, is a subset of the population that is selected for data collection and analysis.

- It is used to make inferences and draw conclusions about the larger population.

- The process of selecting a sample from the population is known as sampling.

- In the previous example, instead of collecting income data from every adult in the country, we might choose a smaller group, say 1000 individuals, as our sample to represent the entire adult population.

- By analyzing the sample, we can estimate and make predictions about the average income of the entire population with a certain level of confidence.

- The key idea is that a sample is a smaller, manageable representation of the population, and by studying the sample, we can make informed inferences about the population without having to collect data from every single individual in the population.

- The quality and representativeness of the sample are crucial factors in the accuracy of the inferences made about the population.

- Here is a list of factors to consider while sampling:

    1. Randomness
    2. Sample size
    3. Sampling method
    4. Representation
    5. Resource constraints

## Types of Data

1. Numerical Data:
    - Numerical data includes both continuous and discrete data.
    - It represents quantitative measurements and can be further divided into continuous and discrete data.
    1. Continuous Data:
        - Continuous data is numerical data that can take any value within a specific range.
        - It has an infinite number of possible values and can be measured with great precision. Examples include height, weight, temperature, and time.
    2. Discrete Data:
        - Discrete data is numerical data that can only take specific, separate values and cannot be measured with the same level of precision as continuous data.
        - Examples include the number of siblings, the number of cars in a parking lot, and the number of students in a class.

2. Categorical Data:
    - Categorical data represents qualitative characteristics or attributes and can be further divided into ordinal and nominal data.
    1. Ordinal Data:
        - Ordinal data represents categories with a meaningful order or ranking between them but without precise numerical differences.
        - Examples include educational levels (elementary/middle/high school), movie ratings (1 star to 5 stars), and customer satisfaction levels (poor/fair/good/excellent).
    2. Nominal Data:
        - Nominal data represents categories with no inherent order or ranking.
        - It includes qualitative data that can be classified into distinct groups without quantitative meaning.
        - Examples include gender (male/female), colors (red/blue/green), and types of fruit (apple/orange/banana).

Understanding the type of data is important because it guides the selection of appropriate statistical methods and techniques for data analysis. Different data types require different approaches for summarizing, visualizing, and analyzing the data effectively.

## Measure of Central Tendancy

- Measure of Central Tendency, also known as measures of central location, is a statistical concept used to describe the center or average of a dataset.
- These measures help to identify a typical or representative value around which the data tends to cluster.
- The three main measures of central tendency are the mean, median, and mode.

1. Mean:
   - The mean, often referred to as the "average," is the most common measure of central tendency.
   - To calculate the mean, sum all the values in the dataset and then divide by the total number of observations.
   - The formula for the mean (μ) of a dataset with n observations (x1, x2, ..., xn) is: μ = (x1 + x2 + ... + xn) / n.
   - The mean is sensitive to outliers since extreme values can significantly affect its value.

2. Median:
   - The median is the middle value of an ordered dataset when arranged in ascending or descending order.
   - If the dataset has an odd number of observations, the median is the middle value.
   - If the dataset has an even number of observations, the median is the average of the two middle values.
   - The median is less sensitive to outliers compared to the mean, making it more suitable for datasets with extreme values.

3. Mode:
   - The mode is the value that occurs most frequently in the dataset.
   - A dataset can have one mode (unimodal), two modes (bimodal), or more (multimodal).
   - In some cases, a dataset may not have any mode if all values occur with the same frequency.

- Each measure of central tendency has its strengths and weaknesses, and the choice of which measure to use depends on the characteristics of the data and the objectives of the analysis.

Use Cases:

- The mean is commonly used when dealing with continuous data that is normally distributed, as it takes into account all values in the dataset.
- The median is often preferred when the dataset contains extreme values or is skewed, as it is not affected by outliers.
- The mode is useful for categorical data or discrete datasets, where the most frequent value is of interest.

- It is essential to consider the properties and distribution of the data when choosing the appropriate measure of central tendency. In some cases, using a combination of measures can provide a more comprehensive understanding of the data's central behavior.

Weighted Mean:

- The weighted mean is a type of average that takes into account the importance or weight of each data point when calculating the mean.
- In other words, instead of giving each value an equal contribution to the average, certain values are given more weight or importance based on their significance.
- Weighted Mean = (w1 *x1 + w2* x2 + ... + wn * xn) / (w1 + w2 + ... + wn)

Use Case of Weighted Mean:

- Weighted means are commonly used when different observations have different levels of importance or when data from different sources need to be combined.

Trimmed Mean:

- The trimmed mean is a measure of central tendency that involves removing a certain percentage of extreme values from both ends of the dataset before calculating the mean.
- The idea behind the trimmed mean is to reduce the impact of outliers or extreme values that can distort the average.
- For example, a 10% trimmed mean involves removing the lowest 5% and highest 5% of the data (totaling 10% of the dataset) and then calculating the mean from the remaining 90% of the data.

Use Case of Trimmed Mean:

- Trimmed means are useful when dealing with datasets that contain outliers or extreme values that can significantly affect the traditional mean.

- By trimming the dataset and calculating the mean from the central portion, the trimmed mean provides a more robust estimate of the center of the data.

Example of Weighted Mean:

- Suppose you want to calculate the weighted mean of students' exam scores, where the weights represent the importance of each exam. The dataset is as follows:

| Exam Score (x) | Weight (w) |
|--------------|---------|
| 85           | 0.2     |
| 90           | 0.3     |
| 78           | 0.1     |
| 95           | 0.4     |

- To calculate the weighted mean, we use the formula:

Weighted Mean = 89.8

Example of Trimmed Mean:

- Suppose you have a dataset representing the time (in seconds) taken by athletes to complete a race:

[10, 11, 9, 12, 15, 8, 18, 7, 14, 22, 25]

To calculate the 20% trimmed mean, we remove the lowest 10% and highest 10% of the data (2 values from each end):

Trimmed Mean ≈ 13.875

The 20% trimmed mean of the race completion times is approximately 13.875 seconds.

- In these examples, the weighted mean accounts for different exam weights, and the trimmed mean excludes extreme values to provide a more robust estimate of the center of the data.
- Both methods are used to handle specific scenarios where traditional arithmetic mean might not be the best representation of the data.

## Measure of Dispersion

- Measure of Dispersion, also known as measures of variability or spread, is a set of statistical concepts used to quantify the extent of variation or spread in a dataset.
- These measures provide valuable insights into how much the individual data points differ from the central tendency, such as the mean or median.
- Measures of dispersion are essential in understanding the distribution of data points and assessing the consistency or variability of the data.

1. Range:
   - The range is the simplest measure of dispersion and represents the difference between the largest and smallest values in the dataset.
   - Range = Maximum Value - Minimum Value
   - While easy to calculate, the range is sensitive to outliers and may not provide a comprehensive view of data spread.

2. Interquartile Range (IQR):
   - The interquartile range is a more robust measure that accounts for outliers. It is the difference between the third quartile (Q3) and the first quartile (Q1).
   - IQR = Q3 - Q1
   - The IQR is useful for summarizing the middle 50% of the data, excluding the extreme values.

3. Variance:
   - Variance measures the average of the squared differences between each data point and the mean. It measures the spread of data points around the mean.
   - Variance = Σ[(x - μ)²] / N
   - where x is each data point, μ is the mean, and N is the total number of observations.
   - Variance is influenced by both small and large differences from the mean, making it sensitive to outliers.

4. Standard Deviation:
   - The standard deviation is the square root of the variance. It is the most commonly used measure of dispersion due to its interpretability and convenient units.
   - Standard Deviation = √(Variance)
   - Like variance, the standard deviation measures the spread of data around the mean.

5. Coefficient of Variation (CV):
   - The coefficient of variation expresses the standard deviation as a percentage of the mean.
   - It is useful for comparing the relative variability between datasets with different means and units.
   - Coefficient of Variation = (Standard Deviation / Mean) * 100

6. Mean Absolute Deviation (MAD):
   - The mean absolute deviation is the average of the absolute differences between each data point and the mean. It provides a measure of average deviation without squaring the differences.
   - MAD = Σ| x - μ | / N
   - MAD is less sensitive to extreme values compared to variance and standard deviation.

Use Cases:

- Range is straightforward to calculate and provides a quick idea of the dataset's spread but is not suitable for handling outliers.
- IQR is robust to outliers and is useful when the dataset contains extreme values.
- Variance and standard deviation are commonly used for normally distributed datasets to understand the variability around the mean.
- Coefficient of Variation is useful when comparing datasets with different means and units.
- MAD is used when a measure of average deviation without squaring the differences is preferred.
- In summary, measures of dispersion are critical for understanding the spread and variability of data. Selecting the appropriate measure depends on the characteristics of the data and the objectives of the analysis.

## Quantiles

- Quantiles are statistical measures used to divide a set of numerical data into equal-sized groups, with each group containing an equal number of observations.
- Quantiles are important measures of variability and can be used to:

   1. understand distribution of data
   2. summarize and compare different datasets
   3. identify outliers

- There are several types of quantiles used in statistical analysis, including:

1. Quartiles: Divide the data into four equal parts, Q1 (25th percentile), Q2 (50th percentile or median), and Q3 (75th percentile).
2. Deciles: Divide the data into ten equal parts, D1 (10th percentile), D2 (20th percentile), ..., D9 (90th percentile).
3. Percentiles: Divide the data into 100 equal parts, P1 (1st percentile), P2 (2nd percentile), ..., P99 (99th percentile).
4. Quintiles: Divides the data into 5 equal parts

- Things to remember while calculating these measures:
   1. Data should be sorted from low to high
   2. You are basically finding the location of an observation
   3. They are not actual values in the data
   4. All other tiles can be easily derived from Percentiles

## Percentiles

- A percentile is a statistical measure that represents the percentage of observations in a dataset that fall below a particular value.
- For example, the 75th percentile is the value below
which 75% of the observations in the dataset fall.
- Formula to calculate the percentile value:

```math
PL = p(N+1)/100

• PL = the desired percentile value location
• N = the total number of observations in the dataset
• p = the percentile rank (expressed as a percentage)
```

## 5 number summary

- The five-number summary is a descriptive statistic that provides a summary of a dataset.
- It consists of five values that divide the dataset into four equal parts, also known as quartiles.
- The five-number summary includes the following values:

1. Minimum value: The smallest value in the dataset (excluding outliers).

2. First quartile (Q1): The value that separates the lowest 25% of the data from the rest of the dataset.

3. Median (Q2): The value that separates the lowest 50% from the highest 50% of the data.

4. Third quartile (Q3): The value that separates the lowest 75% of the data from the highest 25% of the data.

5. Maximum value: The largest value in the dataset (excluding outliers).

- The five-number summary is often represented visually using a box plot, which displays the range of the dataset, the median, and the quartiles.
- The five-number summary is a useful way to quickly summarize the central tendency, variability, and distribution of a dataset.

## Boxplots

- A box plot, also known as a box-and-whisker plot, is a graphical representation of a dataset that shows the distribution of the data.
- The box plot displays a summary of the data, including the minimum and maximum values, the first quartile (Q1), the median (Q2), and the third quartile (Q3).

Benefits of a Boxplot:

- Easy way to see the distribution of data
- Tells about skewness of data
- Can identify outliers
- Compare 2 categories of data (Side by side boxplot)

## Scatterplot

- A scatter plot is a type of graphical representation that displays the relationship between two numerical variables.
- It is used to visualize the correlation or association between the variables and is especially helpful in identifying patterns, trends, and potential outliers in the data.
- In a scatter plot, each data point is represented by a dot, and the position of the dot corresponds to the values of the two variables being plotted.

## Covariance

- Covariance is a statistical measure that describes the degree to which two variables are linearly related.
- It measures how much two variables change together, such that when one variable increases, does the other variable also increase, or does it decrease?
- If the covariance between two variables is positive, it means that the variables tend tomove together in the same direction.
- If the covariance is negative, it means that the
variables tend to move in opposite directions.
- A covariance of zero indicates that the
variables are not linearly related.
- One limitation of covariance is that it does not tell us about the strength of the relationship between two variables, since the magnitude of covariance is affected by the scale of the variables.
- Covariance of a variable with itself is a variance.

## Correlation

- Correlation refers to a statistical relationship between two or more variables.
- Specifically, it measures the degree to which two variables are related and how they tend to change together.
- Correlation is often measured using a statistical tool called the correlation coefficient, which ranges from -1 to 1.
- A correlation coefficient of -1 indicates a perfect negative correlation, a correlation coefficient of 0 indicates no correlation, and a correlation coefficient of 1 indicates a perfect positive correlation.
- A correlation between two variables does not necessarily imply that one variable is the reason for the other variable's behaviour.
- Correlations can provide valuable insights into how different variables are related, they cannot be used to establish causality.
- Establishing causality often requires additional evidence such as experiments, randomized controlled trials, or well-designed observational studies.

## Formula

```
Sample Mean = (x1 + x2 + ... + xn) / n
Population Mean = (x1 + x2 + ... + xn) / n

Median = (n + 1) / 2 
Median = (n / 2) + ((n / 2) + 1) / 2

Mode = highest frequency

Weighted Mean = (w1 * x1 + w2 * x2 + ... + wn * xn) / (w1 + w2 + ... + wn)

Trimmed Mean = Mean of the remaining (n - p*n) observations

Range = Maximum Value - Minimum Value

Population Variance = Σ[(x - μ)²] / N
Sample Variance = Σ[(x - x̄)²] / (n - 1)

Population Standard Deviation = √(Population Variance)
Sample Standard Deviation = √(Sample Variance)

Coefficient of Variation = (Standard Deviation / Mean) * 100

percentile value location PL = p(N+1)/100

IQR = Q3 - Q1
min =  Q1 - 1.5 * IQR
max =  Q3 + 1.5 * IQR

sample = Sxy = Cov(X, Y) = Σ [ (Xᵢ - X̄) * (Yᵢ - Ȳ) ] / (n - 1)
population σxy = Cov(X, Y) = Σ [ (Xᵢ - X̄) * (Yᵢ - Ȳ) ] / n

population ρ(X, Y) = Cov(X, Y) / (σ(X) * σ(Y))
sample r(X, Y) = Cov(X, Y) / (s(X) * s(Y))



```

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

```
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

Calculate Probability

```
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

