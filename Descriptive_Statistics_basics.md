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
