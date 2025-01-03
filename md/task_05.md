# Topic 5. Vector Spaces and Differentiation in Mathematical Analysis

**Today, we will use gradient descent to build polynomial regression. You will generate a dataset for computational experiments and programmatically implement several variants of the gradient descent method: SGD, RMSProp, Adam, and Nadam. During the computational experiments, you will compare the speed and the number of iterations required for each variant.**

This will help you strengthen the following skills:

- Understanding gradients and using the gradient descent method.

- Optimization in machine learning.

***

# Task (Step by Step)

For this task, you will need to generate data. For 100 random features $x_1$ and $x_2$, compute $y$ y as a 2nd-degree polynomial. For example:

$
  y = 4x_1^2 + 5x_2^2 - 2x_1 x_2 + 3x_1 - 6x_2 
$.

As a result, you will obtain a feature array of size (100, 2) and a target variable array of size (100,).

To complete the task, follow these steps:

**1. Generate the data:**

- Use the `np.random.rand()` function to generate 100 random values for the features $x_1$ and $x_2$.

- Implement a function polynomial(x1, x2) to compute the target variable $y$ y using the specified polynomial.

**2. Generate additional features for each degree:**

Use the `PolynomialFeatures` function from the `sklearn` library to generate additional features for each degree.

**3. Implement functions for gradient descent methods:**

- Implement the function `polynomial_regression_gradient_descent()` to compute the coefficients of polynomial regression using gradient descent.

- Implement the function `polynomial_regression_SGD()` for the SGD variant of gradient descent.

- Implement the function `polynomial_regression_rmsprop()` for the RMSProp variant of gradient descent.

- Implement the function `polynomial_regression_adam()` for the Adam variant of gradient descent.

- Implement the function `polynomial_regression_nadam()` for the Nadam variant of gradient descent.

**4. Compute the runtime of the implemented functions:**

- Use the `%timeit` function to measure the runtime of each implemented function.

**5. Determine the optimal number of iterations for each variant:**

- Experiment with different numbers of iterations for each gradient descent variant to find the optimal number.

**6. Draw conclusions about the computational efficiency of the considered gradient descent variants:**

- Analyze the results and compare the speed and number of iterations required for each method.

***

# Hints

Use functions from `numpy` and algorithms from the lecture notes for this topic.

Refer to the documentation of `numpy`, `sklearn`, and other relevant libraries for additional guidance.