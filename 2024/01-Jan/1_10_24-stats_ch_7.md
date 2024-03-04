Current Streak: 10
All Time Best Streak: 11
All Time Total: 25

Convolutional Neural Network
#Tags: #statistics #data #brilliantatbasics #regression
# NEW FOCUS
I need to reengage the basics of my profession. To do this, I'm going to work my way through some text books foundational to being a data scientist. First is Statistics (9th Edition) by Robert S. Witte and John S. Witte. 

# Chapter 7: Regression

## Least Squares Regression
- **Least squares regression** is a method that minimizes the total of all squared prediction errors for known scores in a correlation analysis. Solving for the total of all squared prediction errors is preferred over the total of all non-squared prediction errors because in the later method results in positive and negative scores cancelling each other out. The sum of squares method penalizes large errors and prevents negative scores from canceling out positive scores.
- Regressions don't provide evidence of causal relationships.
## Standard Error of Estimate
- The sum of squares method does not remove all predictive error. 
- The formula for standard error is
$$S_{y|x}=\sqrt{\sum(Y-Y^{'})^2\over n-2}$$(1) Definition Formula

$$S_{y|x}=\sqrt{SS_y(1-r^2)\over n-2}$$(2) Computation Formula

- Standard error of estimates can be thought of as a rough measure of the average amount of predictive error. The average amount by which known Y values deviate from their predicted Y' values.
## Multiple Regression Equations
- **Multiple regression equations** are a least squares equation that contains more than one predictor or x variable.
## Regression Toward the Mean
- Scores tend to shrink toward the mean. 
### Regression Fallacy
- The **regression fallacy** occurs whenever regression toward the mean is interpreted as a real, rather than a chance effect.