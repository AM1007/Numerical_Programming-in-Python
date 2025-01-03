# Topic 10. EM Algorithm and Gaussian Mixture Model (GMM) Separation

**Today, you will use the knowledge gained from studying Gaussian Mixture Models (GMMs).**

This will help you strengthen the following skills:

- Preparing data for modeling.

- Working with data analysis libraries.

***

# Task (Step by Step)

For this task, you will need to download the dataset from [https://www.kaggle.com/datasets/unsdsn/world-happiness](https://www.kaggle.com/datasets/unsdsn/world-happiness).

To complete the task, follow these steps:

**1. Install and import the necessary libraries:**

- You will need to install the following packages:

```python
Copy
!pip install plotly==5.20.0
!pip install "jupyterlab>=3" "ipywidgets>=7.6"
```

**2. Download the dataset:**

Use the following command to download the dataset:

```python
Copy
!wget -O WorldHappinessReport.zip https://github.com/goitacademy/NUMERICAL-PROGRAMMING-IN-PYTHON/blob/main/WorldHappinessReport.zip?raw=true
```

**3. Unzip the data:**

Use the following command to unzip the dataset:

```python
Copy
!unzip WorldHappinessReport.zip
```

**4. Read the data and display general information:**

Load the data and display summary statistics and feature types.

**5. Plot the distribution of numerical features:**

Analyze whether the distributions match or deviate from a normal distribution.

**6. Select a subset of numerical features and display the correlation matrix:**

- Based on your understanding of the domain and data, select a subset of numerical features and visualize the correlation matrix (refer to [**Topic 4: Measuring Distances and Similarities in Data Analysis**](task_04.md)).

**7. Draw conclusions about the presence and strength of linear relationships between features.**

**8. Visualize the distribution of the target feature (Happiness.Score or Happiness.Rank) by country:**

- Use the following code to create a heatmap:

```python
fig = px.choropleth(data_dataframe,
                    locations="Country",
                    color="Happiness.Score",
                    locationmode="country names")
fig.update_layout(title="Happiness Index 2017")
fig.show()
```

**9. Standardize the data to bring all values to the same statistical range:**

Use the `data_scale()` function with the following transformations:

```python

def data_scale(data, scaler_type='minmax'):
    from sklearn.preprocessing import MinMaxScaler
    from sklearn.preprocessing import StandardScaler
    from sklearn.preprocessing import Normalizer
    if scaler_type == 'minmax':
        scaler = MinMaxScaler()
    if scaler_type == 'std':
        scaler = StandardScaler()
    if scaler_type == 'norm':
        scaler = Normalizer()

    scaler.fit(data)
    res = scaler.transform(data)
    return res

data_scaled = data_scale(original_dataframe)
df_scaled = pd.DataFrame(data_scaled, columns=[original_dataframe.columns])
print(df_scaled.head())
```

**10. Display the statistics of the standardized dataset and compare them with the original dataset:**

- Draw conclusions based on the comparison.

**11. Build a clustering model using the `GaussianMixture()` function from the `sklearn` library.**

**12. Create a heatmap to visualize the distribution of countries by clusters.**

**13. Investigate the impact of different feature sets on the clustering results.**

**14. Draw a general conclusion about how well the clustering results align with the original distribution of countries based on the target feature.**

***
# Hints

- Use functions and algorithms from the lecture notes for this topic and the homework assignment.

- Refer to the documentation of `sklearn`, `plotly`, and other relevant libraries for additional guidance.
