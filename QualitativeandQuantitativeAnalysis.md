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

**A Small Story About the Titanic Dataset**

![image](https://github.com/user-attachments/assets/9c096437-0f38-44b8-8d18-2e18733e0c8f)


The Titanic dataset takes us back to one of history's most tragic and well-known maritime disasters—the sinking of the RMS Titanic on April 15, 1912. Known as the **unsinkable ship,** the Titanic was a luxurious British passenger liner that embarked on its maiden voyage from Southampton to New York City with over 2,200 passengers and crew onboard.

However, the ship struck an iceberg in the North Atlantic and sank, claiming the lives of more than 1,500 people. The Titanic tragedy exposed not only the limits of technology at the time but also the stark socio-economic divides of the early 20th century, as survival rates were significantly influenced by factors such as class, gender, and age.

The Titanic dataset is a structured collection of information about the passengers aboard the ship. It contains details such as:

- **Passenger demographics:** Age, gender, and class (1st, 2nd, or 3rd).
- **Family information:** Number of siblings/spouses and parents/children aboard.
- **Ticket and fare details:** Ticket number, price paid, and cabin information.
- **Survival status:** Whether the passenger survived the tragedy or not.

### Why It’s Fascinating

The Titanic dataset offers a unique opportunity to analyze survival patterns and uncover insights into how different factors influenced a passenger's chance of survival.

### A Data Story Waiting to Be Told

Every passenger in the Titanic dataset has their own story:

- A wealthy first-class traveler enjoying luxury cabins.
- A young third-class immigrant seeking a better life in America.
- Crew members working hard to ensure the voyage's success.
By analyzing this dataset, we uncover patterns and insights that not only provide a glimpse into the past but also teach us valuable lessons about human behavior, risk, and survival.

As we explore the dataset through EDA, think of it as piecing together fragments of history to understand the human side of one of the world's most infamous shipwrecks.

Opne the [EDA Titanic Dataset](https://github.com/nisalm/EDA/blob/18406da2c1a19068ae9f70913e6bc996eeadfdfc/EDA_of_Titanic_Dataset.ipynb) python notebook. 
