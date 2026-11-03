# Descriptive Statistics

Let $x_1,\dots,x_n$ be the data and $x_{(1)} \le \dots \le x_{(n)}$ the values sorted in ascending order.

## Central tendency

### Mean

The sum of all values divided by the number of values.

$$
\bar{x} = \frac{1}{n}\sum_{i=1}^{n}x_i
$$

Sensitive to outliers.

### Median

The middle value of the sorted data.

For odd $n$:

$$
\mathrm{Median} = x_{\left(\frac{n+1}{2}\right)}
$$

For even $n$:

$$
\mathrm{Median} = \frac{x_{(n/2)} + x_{(n/2+1)}}{2}
$$

Resistant to outliers.

### Mode

The most frequently occurring value.

A dataset may have one mode, multiple modes, or no unique mode.

## Dispersion

### Minimum and maximum

The smallest and largest values.

$$
\min = x_{(1)}, \qquad \max = x_{(n)}
$$

### Range

The difference between the maximum and minimum.

$$
R = \max - \min
$$

### Interquartile range

The spread of the middle 50% of the data.

$$
IQR = Q_3 - Q_1
$$

$Q_1$ is the 25th percentile; $Q_3$ is the 75th percentile.

### Variance

Measures squared deviations from the mean.

Population variance:

$$
\sigma^2 = \frac{1}{N}\sum_{i=1}^{N}(x_i-\mu)^2
$$

Sample variance:

$$
s^2 = \frac{1}{n-1}\sum_{i=1}^{n}(x_i-\bar{x})^2
$$

Measured in squared units.

### Standard deviation

The square root of the variance.

$$
\sigma = \sqrt{\sigma^2}, \qquad s = \sqrt{s^2}
$$

Measured in the same units as the data.

## Shape and position

### Skewness

Measures the asymmetry of a distribution.

$$
\gamma_1 = \frac{E[(X-\mu)^3]}{\sigma^3}
$$

- **Positive:** a longer right tail.
- **Negative:** a longer left tail.

Symmetric distributions have zero skewness, but zero skewness does not necessarily imply symmetry.

### Kurtosis

Measures tail heaviness and the tendency to produce extreme values.

$$
\beta_2 = \frac{E[(X-\mu)^4]}{\sigma^4}
$$

For a normal distribution: $\beta_2 = 3$.

Excess kurtosis:

$$
\gamma_2 = \beta_2 - 3
$$

For a normal distribution, excess kurtosis is $0$.

### Quantiles

Thresholds that divide a distribution according to cumulative probability.

$$
q_p = \inf\{x : F(x) \ge p\}
$$

where $F(x) = P(X \le x)$.

- **First quartile:** $Q_1 = q_{0.25}$
- **Median:** $Q_2 = q_{0.5}$
- **Third quartile:** $Q_3 = q_{0.75}$

## Notation

- $n$: sample size; $N$: population size.
- $x_i$: an individual observation.
- $x_{(i)}$: the ith value in ascending order.
- $\bar{x}$: sample mean; $\mu$: population mean.
- $\sigma$: population standard deviation; $s$: sample standard deviation.
- $E$: expected value; $\sum$: summation.

> Sample quantiles, skewness, and kurtosis can be calculated using different conventions, so results may vary slightly between software packages.
