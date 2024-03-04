Current Streak: 4
All Time Best Streak: 11
All Time Total: 19

Convolutional Neural Network
#Tags: #statistics #data #brilliantatbasics
# NEW FOCUS
I need to reengage the basics of my profession. To do this, I'm going to work my way through some text books foundational to being a data scientist. First is Statistics (9th Edition) by Robert S. Witte and John S. Witte. 

# Chapter 1: Introduction
## What is statistics
- Statistical knowledge is key to understanding research reports within your area of interest. When someone says, *on average* or *no evidence of a relationship*, you'll know to ask questions like, *which average?* or *what constitutes a lack of evidence?* and gain a great understanding of the issue at hand and the rigor of the test. 
- Statistics exists because there is variability in the real world. Not everyone has the same intelligence, likes, etc. and we need a way of quantifying this variability.
- **Descriptive Statistics** provides us tools to organize and summarize the variability of observations (tables, graphs, averages).
- **Inferential Statistics** provides tests and estimates for generalizing beyond collections of actual observations. 
	- **Population vs Sample** - A population is any complete collection of observations while a sample is a smaller collection drawn from a population. Often it is difficult to obtain observations from an entire population. Thus we're required to make inferences about the population based on a sample. This not only requires different testing techniques but also considerations about how representative the sample is. 
	- Random sampling helps to ensure a sample is representative of the population but can be difficult when the population lacks structure.
	- Random assignment (equal changes of being assigned to the control or experiment group) is another technique that can aid testing.
## Three types of data
- **Qualitative Data** represents categories (i.e. yes or no, *0 or 1*).
- **Ranked Data** represents relative standing (i.e.*1st, 2nd, 3rd* ).
- **Quantitative Data** represents numbers indicative of an amount or count (i.e 120, 140, etc.).
## Levels of measurement
- This is important as we can use it to further clarify differences in data and ascertain the appropriateness of various arithmetic operations. You wouldn't add two social security numbers despite it being composed of numbers.
- **Nominal Measurement** reflects differences in kind not differences in amount. Male or female is one such example. In our case these differences are typically represented as 0 or 1.
- **Ordinal Measurement** reflects order. It's important to remember that these are indicative of relative standing. 
- **Interval/Ratio Measurement** reflects counts or amounts. We can use these to infer differences between observations assuming that there are equal intervals and a true zero. 
## Types of variables
- A **variable** is a characteristic or property that can take on different values. 
- **Constant** - a characteristic or property that can only take one value. 
- **Discrete Variable** - a quantitative variable isolated by gaps (i.e. 1, 2, 3).
- **Continuous Variable** - A quantitative variable whose values have not restrictions (i.e. 1.2, 4.3234, 5.0). Continuous variables can also be considered approximate numbers as we assume the numbers have been rounded off.
- **Independent Variables** are those we control. Whether or not a subject is provided the treatment is up to us. Thus, the treatment is an independent variable.
- **Dependent Variables** are those we don't control. More often than not these are what we're interested in. What we observe to occur as a result of the subject being administered or not administered the treatment is the dependent variable. It depends on the independent. 
- **Confounding Variables** are uncontrolled and can compromise a study or experiment. 
- **Experiment vs Observational Study** - We can either set up an experiment and examine the treatment's impact in a controlled setting or we can look for relationships in observations not manipulated by the investigator. In an experiment, an investigator obtains a sample, divides that sample into treatment and control groups, and examines the impact. In a study the investigator collects data in an uncontrolled environment and then attempts to identify relationships after controlling for biases and confounding variables. 

