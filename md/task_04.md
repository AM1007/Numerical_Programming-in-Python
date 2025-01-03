# Topic 4. Measuring Distances and Similarities in Data Analysis

**Today, you will use distance metrics to compute a distance matrix and apply data clustering, as well as correlation coefficients to find relationships between features.**

This will help you strengthen the following skills:

- Norms, metrics, and their use in describing data.

- Applying functions from `Pandas` and `Numpy`.

***

# Task (Step by Step)

**1. Load and explore the data:**

- Load the Breast Cancer dataset using the `load_breast_cancer()` function from the `sklearn` library.

- Review the dataset description to understand its structure and characteristics.

**2. Create a DataFrame:**

- Create a DataFrame using the data from the Breast Cancer dataset.

**3. Display information about the data:**

- Use the `info()` function to display information about column types and the number of non-null values in each column.

**4. Display descriptive statistics:**

Use the `describe()` function to display descriptive statistics of the data.

**5. Standardize the data:**

Apply data standardization using functions from the lecture notes or the `sklearn` library.

**6. Create scatter plots:**

- Use the pairplot() function from the seaborn library to create scatter plots between all columns.

**7. Compute distance matrices:**

- Use algorithms and functions from the lecture notes to compute distance matrices for different metrics: `cityblock`, `cosine`, `euclidean`, `l1`, `manhattan`.

**8. Visualize the resulting matrices:**

Use the `heatmap` function from the `seaborn` library or other visualization methods to display the computed distance matrices.

**9. Draw conclusions:**

Draw conclusions based on the analysis of the results and compare the effectiveness of different distance metrics for this dataset.

***

# Hints

Use functions from `numpy` and algorithms from the lecture notes for this topic.

Refer to the documentation of `numpy`, `pandas`, and `seaborn` for additional guidance.