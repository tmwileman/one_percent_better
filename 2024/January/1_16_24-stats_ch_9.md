Current Streak: 2
All Time Best Streak: 11
All Time Total: 28

Convolutional Neural Network
#Tags: #statistics #data #brilliantatbasics #Distributions #SamplingDistributionOfTheMean

# NEW FOCUS
I need to reengage the basics of my profession. To do this, I'm going to work my way through some text books foundational to being a data scientist. First is Statistics (9th Edition) by Robert S. Witte and John S. Witte. 

# Chapter 9: Sampling Distribution of the mean

## What is a sampling distribution
- A **sampling distribution** is the distribution of a statistic based on all possible samples of a given size from a population. For example, if you were to draw all possible samples of size 10 from a population and then calculate the mean of each of those samples, the distribution of the means of those samples would be the **sampling distribution of the mean**.
- Sampling distributions are important because they allow us to make inferences about the population from which the samples were drawn. For example, if we know the sampling distribution of the mean, we can make inferences about the population mean. 

## Creating a sampling distribution
- To create a sampling distribution, we need to draw a large number of samples from a population. As an example, if we wanted to obtain all possible random samples of size two (with replacement) from a population of size four, we would need to draw 16 samples (1 & 1, 1 & 2, 1 & 3, 1 & 4, 2 & 1, 2 & 2, 2 & 3, 2 & 4, 3 & 1, 3 & 2, 3 & 3, 3 & 4, 4 & 1, 4 & 2, 4 & 3, 4 & 4). Since we know the number of possible samples, we also know the probability of each sample occurring. In this case, the probability of each sample occurring is 1/16. This enables us to also calculate the probability of each sample mean occurring (additive property). 

## Mean of all sample means
- The **mean of the sampling distribution of the mean** is equal to the mean of the population from which the samples were drawn.

## Standard error of the mean
- The **standard error of the mean** is the standard deviation of the sampling distribution of the mean. The standard error of the mean is equal to the standard deviation of the population from which the samples were drawn divided by the square root of the sample size.

## Central Limit Theorem
- The **Central Limit Theorem** states that the sampling distribution of the mean is approximately normally distributed for large sample sizes (n > 30) regardless of the shape of the population distribution from which the samples were drawn.
- This is important because it allows us to make inferences about the population mean from the sample mean. For example, if we know the mean of the sampling distribution of the mean, we can make inferences about the population mean.