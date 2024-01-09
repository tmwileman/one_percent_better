Current Streak: 8
All Time Best Streak: 11
All Time Total: 23

Convolutional Neural Network
#Tags: #statistics #data #brilliantatbasics
# NEW FOCUS
I need to reengage the basics of my profession. To do this, I'm going to work my way through some text books foundational to being a data scientist. First is Statistics (9th Edition) by Robert S. Witte and John S. Witte. 

# Chapter 4: Normal Distributions and Standard (z) Scores

## The Normal Curve
- A theoretical curve that has a symmetrical, bell-shaped form.
- A normal curve has the following properties:
	- Symmetrical bell-shaped form
	- The lower half is a mirror of the upper half
	- Peaks at a point midway along the horizontal spread and tapers gradually in either direction
	- The mean, median, and mode are the same for a normal curve
- It's important to note that normal curves are not all the same. While they all share the four properties described above, normal curves can have different heights/spreads. For this reason it is important to know the mean and standard deviation of a normal curve to be able to accurately describe it.
- Despite different appearances, due to a shared mathematical origin we can interpret each curve in exactly the same way as long as we use standard deviation units (z-scores). This is useful because a z-score tells us how much area is under a normal curve at a particular point. A z-sore of 1 indicates that 68% of the data falls under the normal curve between -1 and 1.
## z Scores
- A z score is a unit-free standardized score indicating how many standard deviations a score is above or below the mean of its distribution.
- To calculate the z score, subtract the mean from a value and then divide by the standard deviation. This score consists of two parts:
	- A positive or negative sign indicating whether it's above or below the mean
	- A number indicating the size of the deviation from the mean in standard deviation units
## Standard Normal Curve
- The **standard normal curve** is the one tabled normal curve for z scores. It has a mean of 0 and a standard deviation of 1. This table is a mathematical fact. And while there are infinite normal curves, there is only one **standard normal curve** with a mean on 0 and a standard deviation of 1. 
- The **standard normal table** can be used to find the area between a z score and the mean or between a z score and the rest of the standard normal curve. Knowing how to use it gives you easy access to knowing how much of the data falls between a mean and the z score or after the z score.
- A lot of problems tell you to "assume a standard normal distribution" and the ask what proportion of the data fits between two values. These are essentially asking you how likely some event is. To solve these, convert the values to z scores, then use the **standard normal table** appropriately to find the respective proportions, and finally apply the right operation to get the desired answer.
## z Scores for Non-normal Distributions
- z Scores are not limited to normal distributions. You can find tables for other types of curves and use them when needed.
## Other Notes
- Remember, z scores reflect performance relative to some group rather than an absolute standard. Ensure a reference group is specified.
