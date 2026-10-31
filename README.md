## What do we usually include in descriptive statistics?

### Central tendency

- Mean
- Median
- Mode

### Dispersion

- Minimum, maximum
- Range
- Interquartile range
- Variance
- Standard deviation

### Shape and position

- Skewness
- Kurtosis
- Quantiles

- Python offers a **wide range of options** for descriptive statistics. The most commonly used ones are:

- **NumPy**
- **SciPy**
- **pandas**
- The built-in **statistics** module

Each serves a slightly different purpose.

---

## NumPy: a lightweight starting point

NumPy is often the first step into statistical analysis with Python. It works with **homogeneous numerical data** stored in multidimensional arrays (`ndarray`) and is well suited for quick exploratory analysis.

However, there are some limitations:

- No built-in functions for **mode, skewness, or kurtosis**
- Statistics are computed **for the population by default** (`ddof=0`)

Handling missing values also requires attention. If `NaN` values are present, most NumPy functions return `NaN`.

When preprocessing is not possible, masked arrays (`numpy.ma`) can be used to ignore missing values.

---

## SciPy: extending NumPy

If you need a broader set of descriptive measures for homogeneous data, **SciPy** is a natural extension.

With `scipy.stats`, you can compute:

- Mode (with frequency)
- Skewness
- Kurtosis
- Interquartile range

> ⚠️ By default, `scipy.stats.skew` computes **population skewness**. For sample skewness, `bias=False` must be specified.

A particularly useful function is **`stats.describe`**, which provides a compact summary similar to Excel’s Descriptive Statistics tool:

- Mean
- Variance
- Minimum and maximum
- Skewness and kurtosis
- Number of observations

Mode, however, must still be computed separately.

An important contrast with NumPy: `stats.describe` computes **sample statistics by default** (`ddof=1`).

SciPy can also work with masked arrays (`scipy.stats.mstats`), allowing missing values to be ignored.

---

## pandas: the closest analogue to Excel

For users working with **tabular, labeled data**, pandas is usually the most convenient option.

Its `DataFrame` structure closely resembles Excel tables and naturally supports:

- Missing values
- Mixed data types

The `df.describe()` method computes a standard summary:

- Number of non-missing observations
- Mean
- Standard deviation
- Minimum
- Quartiles
- Median
- Maximum

These statistics are computed **for samples only**.

Population variance and standard deviation can be obtained explicitly using:

- `DataFrame.var(ddof=0)`
- `DataFrame.std(ddof=0)`

Additional descriptive measures can be computed using dedicated pandas methods.

---

## statistics module: a special case

The built-in **statistics** module is designed for **one-dimensional numeric data** only.

Key limitations:

- No support for multidimensional data
- No handling of missing values (`None`, `NaN`)

It also relies on Python’s built-in functions for minimum, maximum, and sample size.

Its main advantage is support for **exact rational arithmetic** using `fractions.Fraction`, which avoids floating-point rounding errors.
