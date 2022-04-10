# Machine_Learning
Animate bivariate normal distribution :
The Gaussian distribution(or normal distribution) is one of the most fundamental probability distributions in nature.

The density function describes the relative likelihood of a random variable X     at a given sample. If the value is high around a given sample, that means that the random variable will most probably take on that value when sampled at random. Responsible for its characteristic “bell shape”, the density function of a given bivariate Gaussian random variable X     is mathematically defined as:

f_X(x) = \frac{1}{{ \sqrt {2\pi|\Sigma| }}} exp\begin{pmatrix}\frac{-(x-\mu)^T \Sigma^{-1}(x-\mu)}{2} \end{pmatrix}   

Where x        is any input vector \in \mathbb{R^2}         while the symbols \mu        and \Sigma        have their usual meaning.

The main function used in this article is the scipy.stats.multivariate_normal function from the Scipy utility for a multivariate normal random variable.

A “visual” view of the covariance matrix :
The covariance matrix is perhaps one of the most resourceful components of a bivariate Gaussian distribution. Each element of the covariance matrix defines the covariance between each subsequent pair of random variables. The covariance between two random variables X_1        and X_2        is mathematically defined as  \sigma(X_1,X_2) = \mathop{\mathbb{E}}[(X_1-\mathop{\mathbb{E}}[X_1])(X_2-\mathop{\mathbb{E}}[X_2])]        where \mathop{\mathbb{E}}[X]       denotes the expected value of a given random variable X  . Intuitively speaking, by observing the diagonal elements of the covariance matrix we can easily imagine the contour drawn out by the two Gaussian random variables in 2D. Here’s how:

The values present in the right diagonal represent the joint covariance between two components of the corresponding random variables. If the value is +ve, that means there is positive covariance between the two random variables which means that if we go in a direction where x_1       increases then x_2       will increase in that direction also and vice versa. Similarly, if the value is negative that means x_2       will decrease in the direction of an increase in x_1      .

Below is the implementation of the covariance matrix:

In the following code snippets we’ll be generating 3 different Gaussian bivariate distributions with same mean \mu = \begin{bmatrix}0\\[1ex]0\end{bmatrix}     but different covariance matrices: 
Covariance matrix with -ve covariance = \begin{bmatrix}1&-0.8 \\[1ex] -0.8&1 \end{bmatrix}
Covariance matrix with 0 covariance = \begin{bmatrix}1&0 \\[1ex] 0&1 \end{bmatrix}
Covariance matrix with +ve covariance = \begin{bmatrix}1&0.8 \\[1ex] 0.8&1 \end{bmatrix}
The density function is responsible for the characteristic bell shape of the distribution.
