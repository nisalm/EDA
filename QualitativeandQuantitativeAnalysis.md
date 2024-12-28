# Qualitative and Quantitative Analysis

## Qualitative Analysis

Qualitative analysis focuses on understanding the non-numerical attributes of the data. It emphasizes exploring the structure, patterns, relationships, and trends in categorical or descriptive data.

- **Nominal:** Categories without an inherent order (e.g., colors, gender).
- **Ordinal:** Categories with a meaningful order (e.g., rankings, education levels).

Key Features:
- Deals with categorical or textual data.
- Involves visualizations and summary descriptions to identify relationships and distributions.
- Provides insights into the qualitative nature of the dataset.

1. Distribution of Categories:

Analyzing the frequency of unique values in categorical columns (e.g., gender, product categories).
```python
data['Gender'].value_counts()
```

2. Identifying Relationships:

Checking how categorical features relate to the target variable (e.g., survival rate by gender in the Titanic dataset).
```python
data.groupby('Gender')['Survived'].mean()
```
3. Visualizing Patterns:

Using bar plots, pie charts, or heatmaps to represent categorical relationships.
```python
import seaborn as sns
sns.countplot(x='Gender', hue='Survived', data=data)
```

## Quantitative Analysis
Quantitative analysis focuses on exploring and summarizing numerical attributes of the data. It involves mathematical and statistical techniques to derive insights from the numbers.

- **Continuous:** Data that can take any value within a range (e.g., height, weight, temperature).
- **Discrete:** Data that can only take specific values (e.g., number of students, dice rolls).

Key Features:
- Deals with numerical data (e.g., age, salary, sales).
- Includes summary statistics, distributions, and advanced mathematical techniques.
- Provides precise and measurable insights.

1. Summary Statistics:

Computing measures like mean, median, standard deviation, and percentiles to describe numerical columns.  
```python
data['Age'].describe()
```

2. Outlier Detection:

Identifying extreme values in numerical data using box plots or interquartile range (IQR).
```python
sns.boxplot(x=data['Age'])
```

3. Correlation Analysis:

Calculating correlation coefficients to measure the strength of relationships between numerical variables.
```python
data.corr()
```
4. Visualizing Distributions:

Using histograms, scatter plots, or density plots to understand data spread and relationships.

```python
sns.histplot(data['Age'], bins=20)
sns.scatterplot(x='Age', y='Fare', data=data)

```

**Qualitative vs. Quantitative in EDA**

Here is the comparison between Qualitative vs Quantitiative Analysis 

| Aspect               | Qualitative Analysis                           | Quantitative Analysis                        |
|----------------------|-----------------------------------------------|----------------------------------------------|
| **Focus**            | Categorical or descriptive data               | Numerical or measurable data                |
| **Goal**             | Understand structure and relationships        | Derive precise metrics and detect patterns  |
| **Methods**          | Frequency counts, group comparisons, bar plots| Summary stats, correlations, histograms     |
| **Examples**         | Survival by gender, product sales by category | Average income, correlation between age and fare |





While **Qualitative Analysis** helps understand the distribution and relationships of categorical data, which can guide encoding strategies for AI models, Identifies class imbalances, helping to avoid biased models, **Quantitative Analysis** provides precise insights into numerical data that can guide feature engineering and model selection.
Detects trends and patterns that can influence model predictions.

### Let’s roll up our sleeves and get coding!

Opne the [EDA Titanic Dataset]() python notebook. 
