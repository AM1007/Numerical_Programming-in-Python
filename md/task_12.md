# Topic 12. Optimization and Gradient Descent Methods

**This is your final project, which will serve as a summary and consolidation of all the knowledge and skills you have acquired during the Numerical Programming in Python course.**

During this task, you will use your knowledge of optimization methods to tune the parameters of a classifier.

This will help you strengthen the following skills:

- Applying dimensionality reduction for visualization and modeling in a reduced feature space.

- Using clustering to preliminarily identify dependencies in the data.

- Classification methods that can leverage prior clustering results.

- Tuning classifier parameters using gradient descent methods.

- Tuning classifier parameters using genetic algorithms.

***

# Dataset

We will use the **Breast Cancer Wisconsin (Diagnostic)** dataset for binary classification. This dataset contains information about various characteristics of cells and a target variable indicating whether a cell is benign or malignant. Key features include radius, texture, perimeter, and other cell characteristics.

We can load this dataset from the `sklearn.datasets` library and use it for binary classification. Below is the code to load the dataset:

```python
Copy
from sklearn.datasets import load_breast_cancer

# Load the dataset
data = load_breast_cancer()

# Features
X = data.data

# Target variable (0 - malignant, 1 - benign)
y = data.target
```

This dataset contains 30 features, making it suitable for binary classification.
***

Task (Step by Step)
To complete the task, follow these steps:

**1. Load the data.**

**2. Visualize pairwise scatter plots** of the target variable with the features.

**3. Perform clustering** using Spectral Clustering, k-means, and Gaussian Mixture Models (GMM). Compare the resulting cluster distribution with the actual class distribution. Explain the results.

**4. Reduce the dimensionality** of the data using PCA (Principal Component Analysis).

**5. Visualize the scatter plot** of the class distribution in the new feature space.

**6. Perform classification** using the LogisticRegression method from the sklearn library.

**7. Perform classification** using logistic regression with parameter optimization via gradient descent methods. Test different methods suggested in the lecture notes.

**8. Perform classification** using logistic regression with parameter optimization via a Genetic Algorithm.

**9. Evaluate the quality** of each classifier using the confusion_matrix() and f1_score() functions.

**10. Draw general conclusions** about the quality of parameter optimization for the classifiers.

***

# Hints

- Use functions and algorithms from the lecture notes for this topic and the homework assignment.

- Refer to the documentation of `sklearn`, `numpy`, and other relevant libraries for additional guidance.