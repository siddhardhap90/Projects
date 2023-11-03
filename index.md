# Banking Data Analytics Project

As a demonstration of my data analysis proficiency, I have embarked on a banking data analytics project. This endeavor serves to practice and exhibit my skills in data science, particularly in the context of financial risk assessment and optimization. Below are the key questions that will guide my research and analysis:

1. **Predicting Loan Defaults**: How can we improve predictions on customer loan defaults?
2. **Dynamic Risk Assessment**: Is it possible to dynamically adjust risk profiles based on customer behavior and economic indicators?
3. **Interconnected Risk**: How are various financial activities and the likelihood of default interrelated?
4. **Stress Testing**: Can our predictive models withstand extreme economic scenarios?
5. **Optimization of Lending Portfolio**: How can we optimize the bank’s lending portfolio for maximum return on investment with minimal risk?

## In-Depth Look at Predicting Loan Defaults

The first question I am tackling is the prediction of loan defaults. The steps I will undertake to address this question include:

- **Data Loading & Preprocessing**: The dataset, sourced from the [UCI Machine Learning Repository](https://archive.ics.uci.edu/dataset/350/default+of+credit+card+clients), will be loaded and cleaned to ensure quality analysis.
- **Exploratory Data Analysis (EDA)**: I will perform a thorough exploratory analysis to understand underlying patterns and trends.
- **Feature Engineering**: I plan to engineer features that could enhance the predictive power of the machine learning models.
- **Model Building**: Various predictive models will be built and tested to find the most effective one for our purpose.
- **Evaluation**: Each model’s performance will be rigorously evaluated using appropriate metrics.
- **Insights & Recommendations**: Finally, I will extract insights and make recommendations based on the model outcomes.

 This work is being done on jupyter notebooks on the google colab environment. 

### Loading the necessary python libraries

```python
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns
```
### Loading dataset into a dataframe and understanding the dataset

```python
dataset = '/content/drive/MyDrive/data practice/defaultcredit.xls'
df = pd.read_excel(datapath,skiprows=[0])
df.head()
```

|   ID   | LIMIT_BAL |  SEX  | EDUCATION | default payment next month |
| ------ | --------- | ----- | --------- | -------------------------- |
|   1    |   20000   |   2   |     2     |             1              |
|   2    |  120000   |   2   |     2     |             1              |
|   3    |   90000   |   2   |     2     |             0              |
|   4    |   50000   |   2   |     2     |             0              |
|   5    |   50000   |   1   |     2     |             0              |

A preview of the dataset, which is only a subset of the rows and columns are shown here. The full dataset has 30k rows and 25 columns. For every customer ID, we have some features like account balance, sex and education. We also have information on whether they have defaulted or not, given by a 1 or 0. 



