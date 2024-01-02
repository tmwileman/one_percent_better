Current Streak: 2
All Time Best Streak: 11
All Time Total: 17

# Gradient Descent
#Tags: #GradientDescent #Interview

# Interview Question
What is a good answer to the question: Explain the concept of gradient descent and its role in optimizing ML models?

# Answer
Gradient descent is the process of incrementally steping toward an optimal solution by minimizing some loss function. It is used to better fit an algorithm to the data. 

For example, consider fitting a line to a scatter plot. We start by just drawing a line randomly between the points in the plot. But we don't really know how well this line fits the data. So we measure how far away our line is from all of the data points, determine the direction our line should move, and repeat until our line is in the optimal position.

In this example we brush over concepts like the Sum of Squared Residuals (SSR), derivatives, and Chain Rule. What's important to remember is that the whole point of gradient descent is that we repeat the process of measuring the error in our current algorithm, adjust its values, and measure the error again until we arrive at a convergence. A point where we can no longer minimize our error.

# Papers read
- [Decomposing Language Models Into Understandable Components](https://www.anthropic.com/index/decomposing-language-models-into-understandable-components?utm_source=substack&utm_medium=email)
    - Summary of Anthropic's work looking into LLM interpretability by finding "clusters" of neurons that correspond to an observed behavior (called features) vs focusing on individual neurons to try an explain why a model acts in a particular way.

- [Mini-GPTs: Efficient Large Language Models throughContextual Pruning](https://arxiv.org/pdf/2306.11644.pdf)
    - Examination of how removing neruons, activations layers, and embedding layers that don't meet a requirement threshold can improve llm efficiency. Authors used relatively small LLMs (1.3-1.5b parameters), trimmed elements that did not meet a required level of activity, and then examined resulting llm size and performance. Found some improvement in model size with relatively same performance.