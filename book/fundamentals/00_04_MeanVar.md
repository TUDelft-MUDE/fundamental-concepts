(meanvar)=
# Expectation (mean) and variance

## Mean or expectation
The mean is the first moment of a probability distribution and is also referred to as the *expectation* of the random variable $X$, and is defined as:

$$
\mathbb{E}(X) = \mu_X = \sum_{i=1}^N x_i p_X (x_i)
$$

for discrete distributions, where $p_Y(x_i)$ are the probability masses for all possible outcomes $x_i$, $i=1,\ldots,N$.

For continuous distributions the equivalent is:

$$
\mathbb{E}(X) = \mu_X = \int_{-\infty}^{\infty} x f_X (x)dx
$$

where $f_X (x)$ is the probability density function.

We will often use the notation $\mathbb{E}(X)=\mu_X$.

The empirical or sample mean based on $m$ outcomes (or: realizations) $x_i$ can be computed as:

$$
\hat{\mu}_X = \frac{1}{m}\sum_{i=1}^m x_i
$$

where we use the ^-symbol to indicate it is an *estimate* of the mean based on a number of realizations.

## Variance 

The outcomes or realizations of a random variable will by definition inhibit a certain spread; they will fluctuate around the mean. The variance  or dispersion  of a random variable  is a measure of these fluctuations around the mean, and is defined by:

$$
\begin{align*}
\mathbb{D}(X) = \sigma^2_X &= \mathbb{E}((X-\mu_X)^2)\\
&= \int_{-\infty}^{\infty} (x-\mu_X)^2 f_X (x)dx
\end{align*}
$$

Hence, the variance equals the expectation of the squared deviations from the mean value. The variance is the *second central moment*.

Based on the formula for the sample mean, we can also find the expression for the sample variance:

$$
\hat{\sigma}_{X}^2 = \frac{1}{m-1}\sum_{i=1}^m (x_i-\hat{\mu}_X)^2
$$

Note that here we divide by $m-1$ instead of $m$. The reason is that otherwise you would get a sample variance which on average would deviate from the true value. In other words, by dividing by $m-1$ we guarantee that if you would repeatedly determine the sample variance based on a new set of $m$ observations, the average of these sample variances converges to the true variance. For large $m$ this of course does not matter much.

The standard deviation $\sigma_X$ of random variable $X$ is given by the square root of its variance.

## Difference between Mean, Median and Mode
There is sometimes confusion about the Mean, especially in datasets of values that are not symmetrically distributed. Moreover, in some cases it may be more useful to mention the Median, while in other cases Mode is also quite meaningful. Here is a definition of these terms:
Mean: Adding all values in a dataset and divide by the total number of values in the set
Median: First, arrange the dataset from the lowest to the highest value. If the data set contains an odd number of values, the median is the middle value. If the data set has an even number of values, the median is the average of the two middle values.
Mode: If the distribution of the data is presented in a histogram or a distribution function, the Mode is the value where the top of the histogram or distribution function lies, i.e. it is the value that occurs most in the dataset.

Here is an example considering the following dataset of integer values in arbitrary order: [6, 6, 3, 7, 5, 2, 6, 3, 4].
Mean: (6+6+3+7+5+2+6+3+4) / 9 = 4.67.
Median: In ascending order: [2, 3, 3, 4, 5, 6, 6, 6, 7]. The value in the middle, which is the Median, is 5.
Mode: The value 6 appears three times, which is the most of all other values. Hence, the Mode is 6.
