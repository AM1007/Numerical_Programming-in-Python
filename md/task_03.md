# Topic 3. Vector Operations in n-Dimensional Spaces

**Today, you will use vector operations to process word vectors. This approach can be useful in Natural Language Processing (NLP) tasks.**

This will help you strengthen the following skills:

- Vector and scalar dot products.

- Applying functions from `Pandas` and `Numpy`.

***

# Task (Step by Step)

For this task, use a [file](./assets/word_embeddings_subset.p) containing an NLP model.

**1. Define a DataFrame with 3D word vectors:**

- Load a word embeddings model using a file that contains the NLP model.

- Extract 3D vectors for all words from this model.

- Create a DataFrame containing information about the words and their 3D vectors.

**2. Define functions to find the nearest word:**

- Write a function that takes a 3D vector and finds the nearest word in the `word_embeddings_subset` model.

- Use this function for several examples and ensure the results are correct.

**3. Compute the cross product to find an orthogonal word:**

- Select several random pairs of words.

- Compute the cross product for each pair of words and use the previously written function to find the nearest word.

- Analyze the results and try to interpret them.

**4. Write functions to determine the angle between words:**

- Develop a function that calculates the angle between vectors for any two words.

- Test this function for different pairs of words.

- Examine the results and try to determine their interpretation.

***

# Hints

- Use functions from `numpy` and algorithms from the lecture notes for this topic.

- Refer to the documentation of `numpy` and `pandas` for additional guidance.