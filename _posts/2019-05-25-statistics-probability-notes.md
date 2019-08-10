---
title: Understanding Statistics and Probability
layout: post
categories: notes maths
---

Statistics is used to summarize data. Probability is a way to find likeliness of an event to happen. Permutation and combination are ways to count events and possibilities. All these learning are from [Khan Academy](https://www.khanacademy.org/math/statistics-probability) and [AMPBA - ISB](https://www.isb.edu/advanced-management-programme-in-business-analytics).

* Do not remove this line (it will not be displayed)
{:toc}

# Statistics
Basics of statistics for Data Science.

**Central tendency** measures tell us how values are grouped around the centre value.

**Variation** tells us how disperse the data is or how much it is scattered

**Shape** shows pattern of distribution of values. How the data is distributed in a frequency.

## Summarizing Quantitative Data
Mean median and mode are three ways to summarize the data and measure the central tendency of data. These are usually calculated for quantitative data. 

**Mean**

Average or mean are one and the same thing. It is some of all the data points divided by number of data points. 

$$ \mu = \frac{ \sum_{i=0}^n x_i }{ n } $$

It gets affected by the outliers .

**Median**

It is the middle number in an ordered list. 

If it's even then it is sum of two middle number by two else it's the middle one. 

if $n = even$ then: $(a+b)/2$ where a and b are middle numbers.

It is not affected by the extreme values.

**Mode**

It is the most *common number* or the most frequent number in the dataset. 

*No mode*, if the values in a given set all occur the same number of times, the data set has no mode because no number is any more common than any other. 

*Several mode* if more than one number is repeated same number of times.

It is not affected by extreme values.

**Geometric Mean**

It is used to measure rate of change of variable over time. For eg, rate of return on investment over years.

$$ X_G = (X_1 \ x \  X_2 \ x\ ... \ x\  X_n)^{(1/n)} $$

GM rate of return, here $$ R_i $$ is rate of return in time period i

$$ R_G = [ (1 + R_1) \ x \ (1 + R_2) \ x ... x \ (1 + R_n) ]^{(1/n)} - 1 $$

**Effect of Outliers**

Removing a big outlier decreases the mean more but less change on median and we may be median doesn't change.

## Spread and Variation of Data
The spread of data can be measured by its range, interquartile range (IQR), variance, standard deviation. and coefficient of Variation.

**Range**

It is difference between largest and smallest value in data. It is not dependent on distribution of data and is sensitive to outliers.

**Interquartile Range**

Quartiles divide the ordered data in to 4 segments. Each have equal number of values.  Median (Q2) divides the dataset into two different parts. IQR is the difference in the middle of the first half (Q1) and the middle of second half (Q3). We then find the median of these two different parts and then find the difference. 

If we have even number of data points in dataset then we include the first middle number in first set and the second middle number in second set.

IQR is useful to find out how much the data is varying. 

Range can be misleading when we have outliers. But in this case interquartile range can give us much better measure of spread of data.

$IQR$ = md 2nd quartile - md 1st quartile

**Quartile Measures**

- Q1, is the value for which 25% of the observations are smaller and 75% are larger
- Q2 is the same as the median (50% of the observations are smaller and 50% are larger)
- Only 25% of the observations are greater than the Q3

A *box plot* shows Min, Q1, Q2, Q3 and Max values of data.

**Measure of spread**

Measure of spread can be found by calculating range variance and standard deviation. 
- Sample is part of data while population is entire dataset. 
- We can estimate measures from sample for entire dataset. 

**Variance**

Squared deviation of values from the mean

$$ \sigma^2 = \frac{ \sum(x_i - \mu)^2 }{ n } = \frac{ \sum(x_i)^2 }{ n } - \mu^2 $$

**Standard Deviation**

Variation about the mean. It has *same unit as the original data*.

$$ \sigma = \sqrt{Variance} = \sqrt{\sigma^2} = \sqrt \frac{ \sum_{1}^n(x_i - \mu)^2 }{ n }$$

**For example:**

A = [-10, 0, 10, 20, 30]

B = [8, 9, 10, 11, 12]

Mean of two data set is same (10) but range varies. So we calculate variance to show difference between datasets.

$$ \sigma^2(A) = 200 $$

$$ \sigma^2(B) = 2 $$

$$ \sigma(A) = \sqrt{200} = 10\sqrt{2} $$

$$ \sigma(B) = \sqrt{2} $$

**Result**

Hence, points in A are 10 times more deviated.

**Note:**

- The more the spread, the greater is range, variance and SD
- Thr more data is contracted, the smaller these measures are.
- If all values are same (no variation) then all these are zero.
- None of these measures can ever be negative.
- Adding a number to all values, $x_i$, makes no difference to variance.
- Multiplying a number, k, to all values, $x_i$, makes variance  $\sigma^2 \times k$  

**Coefficient of Variation**

It measures relative variation in %. It shows variation relative to mean. Can compare data with different units.

$$ CV = \frac{ S }{ X } * 100 % $$

For example, 

Stock A = $50, SD = $5

CV(A) = (5/50)*100% = 10%

Stock B = $100, SD = $5

CV(B) = (5/100)*100% = 5%

Hence, both stocks have same SD, but stock B is less variable relative to its price.

**Better measures**

What defines dataset better, mean or median?
- Mean can give us the standard deviation, median can you give us IQR. 
- Mean is better for symmetric dataset, median is better for skewed dataset which has outliers. 
- Median is better for salaries and home prices as it has outliers.

## Shape of Distribution

This tells us how data is distributed. It can be measure by:
- Skewness: Extent to which data values are not symmetrical
- Kurtosis: Affects the peakedness of the curve of the distribution. It tell the sharpness of rise of curve. Bell shaped is Mesokurtic (Kurtosis = 0).

### Skewness

Data can be symmetric, left or right skewed. If it is symmetric then we can work on half of the sample of data.

Left: Mean < Median
Symmetric: Mean = Median
Right: Median < Mean

### Kurtosis

How sharply the curve rises. Eg:
- High rise, Kurtosis > 0, Leptokurtic.
- Bell shaped, Kurtosis = 0, Mesokurtic.
- Low rise, Kurtosis < 0, Platykurtic.

> Image of shape and quartiles and box plot

## Frequency Distribution

We can break data in to different classes, then find frequency of data in each class. It is what we see in histogram.

Each class has a mid point, a frequency. We can find **Relative Frequency** which is frequency divided by total frequency (number of data points). So this give us percentage of data point is a particular class interval.

For eg, class A (10 but less than 20) has frequency 3, total observations 20, so relative freq 0.15, hence, 15% data points are in class A.

We can also find cumulative frequency and relative cumulative frequency or **Cumulative Percentage**. It can help us find probability of that a data is under or less than that class interval.

**Use of Frequency Distribution**

- Raw to useful form
- Visually see the data distribution
- See interval in which data is contracted or clustered.

**Tips:**

- Play with class interval to see different picture of data.
- In large dataset, boundaries don't make much difference.
- When comparing different groups with sample, use relative frequency or percentage distribution.


## Probability Distribution

A frequency distribution can be a probability distribution if the area under the curve is equal to 1. The f(x) of Prob Dist gives us probability of occurrence of x in the given distribution.

A **Continuous** is distribution of a continuous random variable. It is the variable that can take any value on continuum.

The probability distribution can be uniform or normal.

### Uniform Distribution

$$ f(X) = \frac{1}{(b - a)} $$ 
where a is min and b is max

$$ \mu = \frac{a + b}{2} $$

$$ \sigma = \sqrt{  \frac{(b - a)^2}{ 12 }  } $$

Probability that 3 <= x <= 5, are under the line between 3 and 5. As it is a rectangle, the area can be (base)(height).

### The Normal Distribution

It is:
- Bell Shaped
- Symmetrical
- Mean, Median and Mode are equal

The random variable has infinite range. It is defined by:

$$ f(x) = \frac{1}{\sqrt{2\pi}\sigma}e^{-\frac{1}{2}(\frac{X - \mu}{\sigma})^2} $$

e = 2.71828
$\pi$ = 3.14159

Mean moved distribution left/right, sd increases/decreases spread.

#### Standardized Normal or Z score

Any normal distribution can be transformed to **standard normal distribution** $(Z)$ using mean and sd.

Need to transform X units to Z units.

It has mean of 0 and SD of 1.

$$ z = \frac{X - \mu}{\sigma} $$

Also, known as *Z distribution*.

For eg, if mean=100, sd=50 then Z for X=$200, (200-100)/50 = 2

This says that X = 200 is two standard deviations (2 increments of 50 units) above the mean of 100.

So for X and Z distribution the shape remains the same, only scale changes.

**Note:** We measure a few scores compared to the mean. Like performance in class. How far are we from the mean in terms of SD. are we 1sd far from mean or so on. One such score is Z score.

## Normal Probabilities

The probability is area under the curve. So P(a <= X <= b) is area under curve between x=a and x=b.

**Note:** 
- P(a <= X <= b) = P(a < X < b), as P(a) or P(any point) = 0. 
- The total area under the probability curve is 1 and curve is symmetric so half above mean and half below.

**Z Table** is cumulative probability of standardized normal. So Z(2) = 0.9772, this is P(Z < 2, till -infinity)

To find a probability for normal X distribution, convert X to Z the find Z value for it.

### Empirical Rules 

1σ covers 68.26% of X

2σ covers 95.44% of X

3σ covers 99.7% of X


## Sampling  Distributions 

Population is the large group of data that we want to study. We pick a sample of people and try to compare how they perform compared to the population. We collect different sample from the population for example 50 different records from a population.

There will be variation in each of these different samples. So each of these sample gives us slight variation from each other. So sample A is different from sample B and so on. When we collect different samples and find their mean or sd, then this set of information makes sample distribution.

### Developing a Sampling Distributions

If I choose **every possible** sample of size "n" from a population then I get "sampling distribution". Now if we collect mean of each of these possible sample then we get "Sampling distribution of Sample Means".

When we make probability distribution of a population that is unbiased, there are equally likely chance to pick a number. So it is a uniform distribution.

Next, we take all possible sample and find mean of each. The prob distribution of the mean of sample will be a normal distribution.

So we find $\mu_\bar{X}$ and $\sigma_\bar{X}$ and n, here n is number of items in each sample.


### Standard Error of the Mean

Standard error is standard deviation of mean of means. For eg, if we take random samples from a population, we get mean for each sample. S(A) give mean X(A) and so on. Now all these means (X(A), X(B), X(C)..) for a distribution. The standard deviation of this distribution gives us Standard Error.

It is variability in the mean from sample to sample of same size.

### Central Limit Theorem

It says that the distribution of mean of samples is mostly normal distribution. It is not dependent on shape of original population.

$$ \sigma_\bar{X} = \frac{\sigma}{\sqrt{n}} $$

**Note:** The standard error of the mean decreases as the sample size increases.

### P Value

It is same as probability but also take equally likely outcome and rare outcome. So p(two heads, HH) = 0.25. p value of HH is P(HH) + P(TT) + 0 for rare.

### Point and Interval Estimates

Point is a single number and we can find confidence interval for that number. Interval estimate tells us more information about the population than a point estimate tells us.

Point estimate $$\pm$$ (Critical Value)(Standard Error)

Point is the sample statistic estimating population parameter of interest.

Critical Value is table value, based on confidence interval

Standard error is SD of point estimate.

### Confidence Intervals and Levels

95% confidence interval = (1 - α) = 0.95 

=> α    = 0.05

=> α/2  = 0.025

We are interested in points where the probability left out is 0.025. So point till -infinity the probability is 0.025.

Hence, in Z table, the score 0.025 can be found for Z value 1.96.

Here, $$ Z_{\alpha/2} = \pm1.96 $$, this is the normal distribution critical value for a probability of α/2 in each tail.

90% = 1.645

95% = 1.96

99% = 2.58

This tells us that 95% of intervals contains μ.

**CI, when σ is known:**

$$ \bar{X} \pm Z_{\alpha/2} \frac{\sigma}{\sqrt{n}} $$

If σ is unknown, then we can substitute the sample standard deviation, S.This introduces extra uncertainty, since S is variable from sample to sample
n. So we use the t distribution instead of the normal distribution.


### Student's t Distribution

It is a family of distributions. Its value depends on degrees of freedom (d.f) = n - 1.

t -> Z as n increases.

### Sampling Error

There is an error associated with mean of a sample. We can find a sample size to get desired *margin of error (e)* with (1 - α) level of confidence.

$$ e = Z_{\alpha/2}\frac{\sigma}{\sqrt{n}} $$

$$ n = \frac{Z_{\alpha/2}^2 \sigma^2}{e^2} $$


# Probability 

Probability is how likely event is going to happen. It is possibility of event that is fundamentally random. Any experiment can have outcome. The possibility of outcome is the probability. 

For example, if we flip a coin we can get either heads or tails. The possibility of heads is 50% and possibility ability of tails is 50%. So the probability of Heads is .5 and probability of tails is also .5, if it is a biased coin.

The analysis of event governed by probability is called statistics.

$$ P(e) = \frac{ Possibilities }{ Outcomes } $$

Sample space is all possible outcomes.

**Theoretical  probability** is what can be stated and seems fixed. For example flipping a coin. 

**Experimental probability** Finding an outcome based on past data and experience example prediction of the score. Probability gives a reasonable predictions about an outcome. It is highly likely but not hundred percent true. Also known as **subjective probability**.

**Simulation and Randomness** We can use list of random numbers to simulate our experiment multiple times and average out to find confidence.



## Events

Every possible outcome of a variable is an event.

**Simple event** is an event described by a single characteristic. For eg, a day in January from all days in 2018.

**Joint event** is an event described by two or more characteristics. For eg, a day in January that is also a Wednesday from all days in 2018.

**Complement of an event** A (denoted A’). All events that are not part of event A. For eg, all days from 2018 that are not in January.

**Mutually Exclusive** have no intersection outcomes. They cannot occur simultaneously. For eg, A = day in Jan, B = day in Feb. A and B cannot occur simultaneously.

**Collectively Exhaustive Events** are those in which:

- One of the event must occur
- The set of events covers the entire sample space

For eg, A = Weekday; B = Weekend; C = January; D = Spring;

Events A, B, C and D are collectively exhaustive (but not mutually exclusive – a weekday can be in January or in Spring).

Events A and B are collectively exhaustive and also mutually exclusive.


## Addition Rule
Addition rule of probability. 

P(A or B) = P(A) + P(B) - P(A and B) 

here P(A and B) is probability of intersection of A and B. If A and B are mutually exclusive, then P(A and B) = 0.

For eg, P(Jan or Wed) = P(Jan) + P(Wed) - P(Jan and Wed) = 31/365 + 52/365 - 5/365 = 78/365

## Multiplication Rule 

For independent event, what happened in past event will have no effect on current event. For eg, P(HH) or P(at least 1H in 10 flips).

$$ P(HH) = 0.5 \times 0.5 $$

P(at least 1H in 10 flips) = 1 - P(All T in 10 flips) 

$$ 1 - (0.5)^{10} = 1023 \div 1024 = 99.9% $$

**Conditional Probability**

If dependent, the probability of A and B is:

P(A and B) = P(A) X  P(B\|A) , where B\|A is 'B happening after A' or 'conditional prob of B given that A has occurred'.

if independent, then  P(A and B) = P(A) X P(B) 


## Counting Events

### Permutation

Arrange $n$ people in $k$ seats. To count number of ways in which this can be done we use permutation.

For eg, arrange 6 people in 3 seats, 6.5.4 = 6! / 3! = 120.

$$ _nP_k = \frac{n!}{(n - k)!} = n(n-1)... (k  times) $$

Used when order matters and pick once (without replacement). 

For eg,

$$ _{10}P_3 = 10.9.8 $$

### Combinations

$$ _nC_k = \binom{n}{k} = \frac{_nP_k}{k!} = \frac{n!}{k!(n - k)!} = \frac{n(n-1)...[k \space times]}{k!} $$

We divide it by the number of ways in which k people can be arranged in k places, i.e, k! because ABCD and BCDA are same and we are counting this extra.

Order doesn't matter, 123 = 312. 

For eg, 

$$ _{10}C_3 = \frac{10.9.8}{3.2.1} $$

## Approach to solve a problem

We can take following approaches to solve a probability problem

1. use simple definition, 
$$ P(e) = \frac{events possible}{sample space} $$

2. Make a contingency table with possibilities.

3. Make a decision tree, use when question has **after**.

4. At least or at most, use 
$$ P(at least/most) = 1 - P(e) $$

**Example**

Find number of ways to arrange 1 - 10 digits in 3 places,

Repetition allowed, order matters = 10.10.10

Repetition not allowed, order matters = Permutation = 10.9.8 

Repetition allowed, order doesn't matter = 

$$ \frac{10.10.10}{3.2.1} $$

Repetition not allowed, order doesn't matter = Combination = 

$$ \frac{10.9.8}{3.2.1} $$ 


## Binomial Probability Distribution

When we have to make $k$ success in $n$ attempts, then we can following formula:

$$ P = _nC_k . π^k . (1-π)^{(n-k)} $$

Here π is probability to get success. eg, throwing a basket ball.

Now if we move k from 0 to n, we get different values of P. This can make a distribution. We call this binomial distribution.

## Poisson Probability Distribution

