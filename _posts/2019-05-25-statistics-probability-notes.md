---
title: Understanding Statistics and Probability
layout: post
categories: notes maths
---

Statistics is used to summarize data. Probability is a way to find likeliness of an event to happen. Permutation and combination are ways to count events and possibilities. All these learning are from [Khan Academy](https://www.khanacademy.org/math/statistics-probability).

* Do not remove this line (it will not be displayed)
{:toc}

# Statistics
Basics of statistics for Data Science.

## Summarizing Quantitative Data
Mean median and mode are three ways to summarize the data and measure the central tendency of data. These are usually calculated for quantitative data. 

### Mean
Average or mean are one and the same thing. It is some of all the data points divided by number of data points. 

$ \mu = \frac{ \sum_{i=0}^n x_i }{ n } $

### Median 
It is the middle number. We find it by sorting the entire dataset into an ordered list. 

If it's even then it is sum of two middle number by two else it's the middle one. 

if $ n = even $ then: $ (a+b)/2 $ where a and b are middle numbers.

### Mode
It is the most *common number* or the most frequent number in the dataset. If the values in a given set all occur the same number of times, the data set has no mode because no number is any more common than any other. 

### Effect of Outliers
Removing a big outlier decreases the mean more but less change on median and we may be median doesn't change.

## Spread or Variation of Data
The spread of data can be measured by its range, interquartile range (IQR), variance or standard deviation. 

### Interquartile Range 
It is the difference in the middle of the first half and the middle of second half. Median divides the dataset into two different parts. We then find the median of these two different parts and find the difference. 

If we have even number of data points in dataset then we include the first middle number in first set and the second middle number in second set.

IQR is useful to find out how much the data is varying. 

Range can be misleading when we have outliers. But in this case interquartile range can give us much better measure of spread of data.

$ IQR $ = md 2nd quartile - md 1st quartile

### Measure of spread
Measure of spread can be found by calculating range variance and standard deviation. 
- Sample is part of data while population is entire dataset. 
- We can estimate measures from sample for entire dataset. 

**Variance**

$ \sigma^2 = \frac{ \sum(x_i - \mu)^2 }{ n } = \frac{ \sum(x_i)^2 }{ n } - \mu^2 $

**Standard Deviation**

$ \sigma = \sqrt{Variance} = \sqrt{\sigma^2} = \sqrt \frac{ \sum_{1}^n(x_i - \mu)^2 }{ n }$

**For example:**

A = [-10, 0, 10, 20, 30]

B = [8, 9, 10, 11, 12]

Mean of two data set is same (10) but range varies. So we calculate variance to show difference between datasets.

$ \sigma^2(A) = 200 $

$ \sigma^2(B) = 2 $

$ \sigma(A) = \sqrt{200} = 10\sqrt{2} $

$ \sigma(B) = \sqrt{2} $

**Result**
Hence, points in A are 10 times more deviated.

> Standard deviation cannot be negative standard deviation close to0 means the data points are close to average that means less deviation.

### Better measures

What defines dataset better, mean or median?
- Mean can give us the standard deviation, median can you give us IQR. 
- Mean is better for symmetric dataset, median is better for skewed dataset which has outliers. 
- Median is better for salaries and home prices as it has outliers.

# Probability 

Possibility of event that is fundamentally random.

And experiment can have outcome the possibility of outcome is the probability. For example if we flip a coin we can get head or tail the possibility of head is 50% and prosperous ability of tales is 50% so the probability of Fed is .5 and probability of tales is also .5 if it is a biased coin.

Probability is how likely event is going to happen. The analysis of event governed by probability is called statistics.

$ $ Probability 

Sample space is all possible outcomes.

## Sets and subsides

Here we will discuss about sets subsets supersets universe intersection union belongs to is a member of not a member of and other set terminologies

## theoretical  probability

Example flipping a coin. 

# Experimental probability. 

Finding an outcome based on past data and experience example prediction of the score. Probability gives a reasonable predictions about an outcome. It is highly likely but not hundred percent true.

# Simulation and randomness
We can use list of random numbers to simulate our experiment multiple multiple times and average out to find confidence.

# addition rule
Addition rule of probability. 

$ $

Mutually exclusive events have no intersection outcomes. Multiplication rule for independent event what happened if past event will happen no effect on current event.

$ At least $

# Combinators 

Arrange N people in key positions. For such kind of operations we need to find Combinator. For example arrange six people in three different seats seats.

$ $

This is how we can arrange six people in for chair

$ $

We divide bag how gay people can be arranged in key places that is the factorial because a a BCD and BCDER same Combinator us. We are counting this extra.

$ $
NPKNCK different formulas to be inserted here thank you

# Summary of learning
