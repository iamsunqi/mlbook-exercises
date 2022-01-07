# Naive Bayes and Logistic Regression

Notes from Tom Mitchell's [Machine Learning Book](http://www.cs.cmu.edu/~tom/mlbook )

The mission of probablistic machine learning is to estimate $P(Y|X)$ ,i.e. given an input $X=x$, we want to know the output distribution $P(Y|X=x)$. (seems useless explanation...)

We would like to think of this question with a view of Bayesian. Recall Bayes' rule:

$$
P(Y=y_j|X=x_k) = \frac{P(X=x_k|Y=y_j)\cdot P(Y=y_j)}{\sum_{j=1}^JP(X=x_k|Y=y_j)\cdot P(Y=y_j)} 
$$

Now we put the learning question setting more clear: $X$ is a vector with dimension of m, and y is a scalar output, that is, $X=(X^{(1)},\cdots , X^{(m)})\in \mathbf{R}^m, Y\in \mathbf{R}$.

This statement is important to understand: **Unbiased learning of a bayesian classifier is unpractical.**
First, $P(Y)$ is easily estimated.