# Topic 7. Bayes' Theorem. Bayesian Inference

**Today, you will use the Naive Bayes classifier for spam filtering on a dataset that corresponds to real messages.**

This will help you strengthen the following skills:

- Applying Bayes' Theorem in practical data analysis tasks.

- Preprocessing data for machine learning algorithms.

***

# Task (Step by Step)

For this task, you will need to download the [Email Spam Classification Dataset](https://www.kaggle.com/datasets/purusinghvi/email-spam-classification-dataset/data). In this dataset, the labels for the texts are:

- `1` → Spam

- `0` → Not Spam.

To complete the task, follow these steps:

**1. Download the dataset:**

Use the following command to download the dataset:

```python
!wget -O SpamEmailClassificationDataset.zip 
https://github.com/goitacademy/NUMERICAL-PROGRAMMING-IN-PYTHON/blob/main/SpamEmailClassificationDataset.zip?raw=true
```

**2. Unzip the dataset:**

- Use the following command to unzip the dataset:

```
!unzip SpamEmailClassificationDataset.zip
```
- After this, the file will be located in the local memory of Colab at ./combined_data.csv.

**3. Import necessary libraries:**

You will need specialized libraries for text processing. The import statements might look like this:

```python
import pandas as pd
import seaborn as sns
import matplotlib.pyplot as plt

import re
from nltk.corpus import stopwords
from nltk.tokenize import word_tokenize

# Download stopwords and other resources
import nltk
nltk.download('stopwords')
nltk.download('punkt')
stop_words = set(stopwords.words('english'))
nltk.download('wordnet')
```
4. Read the data:

- Use the following command to read the data:

```python
df = pd.read_csv('./combined_data.csv')
```
- The original dataset contains 83,448 records. For further work, it makes sense to select only a few thousand records.

**5. Visualize the distribution of messages:**

- Visualize the distribution of messages across the two classes using a histogram or pie chart. It is better if the sample contains an almost equal number of messages from both classes.

**6. Apply text preprocessing:**

- Use the nltk library to preprocess the text: convert to lowercase, lemmatize words, and remove duplicate words in messages. Example:

```python
from nltk.stem import WordNetLemmatizer
corpus = []
lemmatizer = WordNetLemmatizer()
stop_words = set(stopwords.words("english"))

for document in df["text"]:
    document = re.sub("[^a-zA-Z]", " ", document).lower()
    document = document.split()
    document = [lemmatizer.lemmatize(word) for word in document if word not in stop_words]
    document = list(set(document))
    document = " ".join(document)
    corpus.append(document)

df["text"] = corpus
```

**7. Prepare data structures:**

- Prepare the data structures `train_spam`, `train_ham`, and `test_emails`, which will contain spam messages for training, ham (non-spam) messages for training, and a dictionary of test messages. Examples of these data structures are provided in the lecture notes.

**8. Apply the Naive Bayes algorithm:**

- Use the implementation of the Naive Bayes algorithm provided in the lecture notes.

**9. Analyze the quality of the classifier:**

- Which words are most likely to appear in spam messages?

***
# Hints

- Use functions from `numpy` and algorithms from the lecture notes for this topic.

- Refer to the documentation of `numpy`, `pandas`, and `nltk` for additional guidance.
