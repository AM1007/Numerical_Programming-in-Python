# Topic 8. LDA and QDA Algorithms in Classification Tasks

**Today, you will use the knowledge gained about discriminant methods to implement your own version of the QDA (Quadratic Discriminant Analysis) method.**

This will help you strengthen the following skills:

- Matrix operations, which are the foundation of the programmatic implementations of these methods.

- Understanding the specifics of how the QDA method works.

***
# Task (Step by Step)

For this task, you will need to load the Iris dataset from the `sklearn` library.

To complete the task, follow these steps:

**1. Load the dataset:**

- Use the `load_iris()` function from the `sklearn` library to load the Iris dataset.

**2. Split the data into training and testing sets:**

- Use the `train_test_split()` function from the `sklearn` library to divide the data into training and testing sets.

**3. Extract feature samples for each class separately:**

- Separate the feature samples for each class in the training data.

**4. Implement the calculation of covariance matrices:**

- Compute the covariance matrices for the feature sets of each class.

**5. Implement the calculation of inverse covariance matrices:**

- Compute the inverse of the covariance matrices for each class.

**6. Calculate the prior probabilities of each class:**

- Compute the prior probabilities of each class based on the training data.

**7. Implement a function to compute the discriminant function values for a single row (vector) of test data:**

- Write a function that calculates the discriminant function values for a single test data point.

**8. Implement a function to compute the discriminant function values and class probabilities for the entire test data matrix:**

- Write a function that calculates the discriminant function values and class probabilities for all test data points.

**9. Perform predictions on the test data using the `QuadraticDiscriminantAnalysis()` function from the `sklearn` library:**

- Compare the results obtained from your implementation with those from the `sklearn` library.

**10. Draw conclusions about the similarity of the results:**

Analyze and compare the results from your custom implementation and the `sklearn` library.

***
# Hints

Use functions from numpy and algorithms from the lecture notes for this topic.

Refer to the documentation of numpy and `sklearn` for additional guidance.