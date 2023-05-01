# Statistics

## Introduction

- Statistics is the discipline that concerns the collection, organization, analysis, interpretation, and presentation of data.
- In applying statistics to a scientific, industrial, or social problem, it is conventional to begin with a statistical population or a statistical model to be studied.
- Populations can be diverse groups of people or objects such as "all people living in a country" or "every atom composing a crystal".
- Statistics deals with every aspect of data, including the planning of data collection in terms of the design of surveys and experiments.

## Samples, Population Experiments

- When census data cannot be collected, statisticians collect data by developing specific experiment designs and survey samples.
- Representative sampling assures that inferences and conclusions can reasonably extend from the sample to the population as a whole.
- An experimental study involves taking measurements of the system under study, manipulating the system, and then taking additional measurements using the same procedure to determine if the manipulation has modified the values of the measurements.
- In contrast, an observational study does not involve experimental manipulation.

## Statistics Types

- Two main statistical methods are used in data analysis: descriptive statistics, which summarize data from a sample using indexes such as the mean or standard deviation, and inferential statistics, which draw conclusions from data that are subject to random variation (e.g., observational errors, sampling variation).
- Descriptive statistics are most often concerned with two sets of properties of a distribution (sample or population): central tendency (or location) seeks to characterize the distribution's central or typical value, while dispersion (or variability) characterizes the extent to which members of the distribution depart from its center and each other.
- Inferences on mathematical statistics are made under the framework of probability theory, which deals with the analysis of random phenomena.

## Statistical Procedure

- A standard statistical procedure involves the collection of data leading to a test of the relationship between two statistical data sets, or a data set and synthetic data drawn from an idealized model.
- A hypothesis is proposed for the statistical relationship between the two data sets, and this is compared as an alternative to an idealized null hypothesis of no relationship between two data sets.
- Rejecting or disproving the null hypothesis is done using statistical tests that quantify the sense in which the null can be proven false, given the data that are used in the test.
- Working from a null hypothesis, two basic forms of error are recognized: Type I errors (null hypothesis is falsely rejected giving a "false positive") and Type II errors (null hypothesis fails to be rejected and an actual relationship between populations is missed giving a "false negative").
- Multiple problems have come to be associated with this framework, ranging from obtaining a sufficient sample size to specifying an adequate null hypothesis.

## Errors in Statistics

- Measurement processes that generate statistical data are also subject to error.
- Many of these errors are classified as random (noise) or systematic (bias), but other types of errors (e.g., blunder, such as when an analyst reports incorrect units) can also occur.
- The presence of missing data or censoring may result in biased estimates and specific techniques have been developed to address these problems.

## Resources

- <https://en.wikipedia.org/wiki/Statistics>
- <https://www.investopedia.com/terms/s/statistics.asp>

## Descriptive Statistics

### Central Tendency

- Mean, every event is equally likely

$$
\bar{x} = \frac{\sum x_i}{\sum f_i} = \sum x_i * \frac{1}{f_i}
$$

- Expected Value

$$
E(x) = \sum x_i P(x_i)
$$

- Median - median of a data means, half of the items are above median and half are below, so median is much representative and not affected by large values

For Sample,

$$
\mathrm {median} (x) = \begin{cases}
& x_{(n+1)/2} && \text{if } n \text{ is odd} \\
& (x_{(n/2)}+x_{((n/2)+1)})/2 && \text{if } n \text{ is even}
\end{cases}
$$

- <https://en.wikipedia.org/wiki/Median>

- Mode - item which occurs most frequently

> Note: your dataset may not be unimodal, it can have multiple mode (multimodal)

- Quartile, not related to central tendency
    - This divides data into four equal parts, as median divides data into four equal parts
    - $Q_1$ lower quartile
    - $Q_2$ median
    - $Q_3$ upper quartile

### Dispersion

- Inter Quartile Range, IQR - $Q_3 - Q_1$

- Variance, we can do sum of the absolute difference from mean,
    but it is not much useful, a much better metric is square of that difference,
    this cause far value to add more weight to variance

$$
\sigma^2 = \frac{\sum(x_i - \bar{x})^2}{\sum f_i}
$$

- for probability

$$
\sigma^2 = \sum(x_i - E(x))^2 * P(x_i)
$$

- Standard deviation - unit of variance is different form that of the values for which we are calculating variance, so standard deviation is used

$$
\sigma = \sqrt{\frac{\sum(x_i - \bar{x})^2}{\sum f_i}}
$$

## Inferential Statistics

### Correlation

- <https://en.wikipedia.org/wiki/Covariance>
- how strong one variable affect other variable
- here is how correlation works,
    - shift the axis of the dataset so $(\bar{x}, \bar{y})$ is the origin

| -          | Quadrant I | Quadrant II | Quadrant III | Quadrant IV|
|---         |---         |---          |---           |---         |
| $\Delta x$ | +ve        | -ve         | -ve          | +ve        |
| $\Delta y$ | +ve        | +ve         | -ve          | -ve        |
| $\Delta x \cdot \Delta y$ | +ve | -ve | +ve | -ve |

$$
\operatorname {cov} (X,Y)={\frac {1}{n}}\sum _{i=1}^{n}(x_{i}-E(X))(y_{i}-E(Y))
$$

$$
\operatorname {cov} (X,Y)=\operatorname {E} [(X-\mu _{X})(Y-\mu _{Y})]
$$

- $\operatorname {cov} (X,Y) > 0$ if X follow Y
- $\operatorname {cov} (X,Y) = 0$ if there is no relation between X and Y
- $\operatorname {cov} (X,Y) \neq 0$ if X follow Y but in a negative way

- Karl Pearson's Coefficient of Correlation

Covariance is independent of choice of origin, but still depends on the **scale of measurement**.
So we use coefficient of correlation.

$$
\rho _{X,Y}
= \operatorname {corr} (X,Y)
= {\operatorname {cov} (X,Y) \over \sigma _{X}\sigma _{Y}}
= {\operatorname {E} [(X-\mu _{X})(Y-\mu _{Y})] \over \sigma _{X}\sigma _{Y}},\quad {\text{if}}\ \sigma _{X}\sigma _{Y}>0
$$

- $-1 \le \rho _{X,Y} ^2 \le 1$
- $0 \le \rho _{X,Y} ^2 \le 1$
- if $0.75 < \rho _{X,Y} ^2 < 1$, high degree of correlation
- if $0.25 < \rho _{X,Y} ^2 < 0.75$, moderate degree of correlation
- if $0 < \rho _{X,Y} ^2 < 0.25$, low degree of correlation

> Note: Correlation does not means causation.

### Spearman's rank correlation coefficient

- <https://en.wikipedia.org/wiki/Spearman%27s_rank_correlation_coefficient>
- This is used, if you have two quantities, and you rank them and find out the correlation
- For e.g. students marks in Math and English, you rank each student mark in both subjects and then find
  correlation and make a inference.

For a sample of size $n$, the $n$ raw scores $X_{i},Y_{i}$ are converted to ranks
$\operatorname {R} ({X_{i}}),\operatorname {R} ({Y_{i}})$

$$
r_{s}
=\rho _{\operatorname {R} (X),\operatorname {R} (Y)}
={\frac {\operatorname {cov} (\operatorname {R} (X),\operatorname {R} (Y))}{\sigma _{\operatorname {R} (X)}\sigma _{\operatorname {R} (Y)}}}
$$

Also, we can derive a simplified formula from this:

$$
r_{s}
= 1-{\frac {6\sum d_{i}^{2}}{n(n^{2}-1)}}
$$

- $d_{i}=\operatorname {R} (X_{i})-\operatorname {R} (Y_{i})$ is the difference between the two ranks of each observation,
- $n$ is the number of observations.
- here are some notes regarding this formula:
    - this should not be used in cases where the data set is truncated;
      that is, when the Spearman's correlation coefficient is desired for the top $X$ records, like
      correlation for top 20 performers
    - Identical values are each assigned fractional ranks equal to the average of their positions
      in the ascending order of the values, which is equivalent to averaging over all possible permutations.
    - If ties are present in the data set, the simplified formula above yields incorrect results
    - For approximation in case of ties,
      a correction factor is added, $m_i$ denotes that some $m_i$ items have common rank

$$
r_{s}
= 1-{\frac {6(\sum d_{i}^{2} + \sum \frac{1}{12}(m^3 - m))}{n(n^{2}-1)}}
$$
