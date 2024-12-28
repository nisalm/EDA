# Qualitative and Quantitative Analysis

1. **Qualitative Analysis**

   Qualitative analysis focuses on understanding the non-numerical attributes of the data. It emphasizes exploring the structure, patterns, relationships, and trends in categorical or descriptive data.

Key Features:
- Deals with categorical or textual data.
- Involves visualizations and summary descriptions to identify relationships and distributions.
- Provides insights into the qualitative nature of the dataset.

Distribution of Categories:

Analyzing the frequency of unique values in categorical columns (e.g., gender, product categories).
```python
data['Gender'].value_counts()

Identifying Relationships:

Checking how categorical features relate to the target variable (e.g., survival rate by gender in the Titanic dataset).
```python
data.groupby('Gender')['Survived'].mean()

Visualizing Patterns:

Using bar plots, pie charts, or heatmaps to represent categorical relationships.
```python
import seaborn as sns
sns.countplot(x='Gender', hue='Survived', data=data)
