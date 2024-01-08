Current Streak: 7
All Time Best Streak: 11
All Time Total: 22

Convolutional Neural Network
#Tags: #statistics #data #brilliantatbasics
# NEW FOCUS
I need to reengage the basics of my profession. To do this, I'm going to work my way through some text books foundational to being a data scientist. First is Statistics (9th Edition) by Robert S. Witte and John S. Witte. 

# Chapter 4: Describing Variability
Variability is the amount by which scores in a distribution are dispersed. It is important because it tells us how "spread out" the data is. Variance is also a key factor in determining if a treatment results in a real difference between control and test groups. 

Lower variability is associated with more stable distributions whereas higher variability is are associated with less statistically stable distributions. 
## Range
- The difference between the highest and lowest scores in a distribution. For example, a distribution with a high score of 10 and a low score of 0 has a range of 10 (10-0=10). Range is good for understanding the total spread of the data but falls short of telling you anything of real value because it leaves out the remaining scores. 
## Variance
- Variance is the mean of squared deviation scores. For example, you have the following distribution, 1, 2, and 3. The mean of this distribution is 2. The respective deviations for each score is -1, 0 and 1. The square of all deviations are 1, 0 and 1 (notice the -1 is turned to a positive integer). The mean of these scores is 2/3. 
- Variance is a preferred measure of variability but can be difficult to communicate because the units are squared. As a result, many prefer to use **standard deviation** which is just the square root of **variance**.
## Standard Deviation
- **Standard deviation** is a rough measure of the average amount by which scores deviate on either side of their mean. It is calculated by just taking the square root of the **variance**. It's important to remember that it's an approximation and often differs from the mean absolute deviation. 
- Another way to think about standard deviation is in reference to how many scores fall within one, two, or three standard deviations of the mean. This is because in most frequency distributions, ~68% of scores fall within one standard deviation on either side of the mean. In that same line, as few as 5% of scores deviate three or more standard deviations from the mean.
- Mean is a measure of position. Standard deviation is a measure of distance. 
- As with other measures, we distinguish between population and sample. 
- **Sum of squares** is the sum of squared deviation scores.
## Degrees of Freedom
- **Degrees of freedom (df)** refers to the number of values that are free to vary. df is used in sample calculations because we're estimating some unknown characteristic of a population. Degrees of freedom are directly linked to the sample size and the number of parameters estimated. A higher number of degrees of freedom generally indicates a larger sample size or fewer constraints, leading to more reliable and accurate estimates. When calculating the sample variance or standard deviation, the formula typically divides by `n - 1` rather than `n`, where `n` is the sample size. The degrees of freedom in this case are `n - 1`. This adjustment is made because one degree of freedom is lost by estimating the mean from the data.