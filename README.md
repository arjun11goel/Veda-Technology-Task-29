# Task 29: Relationship Analysis

## Overview
This task focuses on performing relationship analysis between two continuous numerical variables using a scatter plot. By visualizing data points across two dimensions, we analyze the direction, strength, and pattern of the association.

## Dataset
- **Dataset Used:** `iris_dataset.csv`
- **Variables Analyzed:** 
  - **X-axis (Predictor/Independent):** `petal_length` (cm)
  - **Y-axis (Response/Dependent):** `petal_width` (cm)

---

## Code Implementation

```python
import pandas as pd
import matplotlib.pyplot as plt

# Load dataset
df = pd.read_csv("iris_dataset.csv")

# Create plot
plt.figure(figsize=(8, 6))
plt.scatter(df["petal_length"], df["petal_width"], color="teal", alpha=0.7, edgecolors="k")

# Formatting
plt.title("Relationship Analysis: Petal Length vs. Petal Width", fontsize=14, fontweight="bold")
plt.xlabel("Petal Length (cm)", fontsize=12)
plt.ylabel("Petal Width (cm)", fontsize=12)
plt.grid(True, linestyle="--", alpha=0.5)

plt.show()
```

---

## Visualizations

![Relationship Analysis Plot](Screenshot%202026-11-07%20114443.png)

---

## Description & Key Observations

### 1. Relationship Description
The scatter plot demonstrates a strong, direct **positive linear relationship** between petal length and petal width. As petal length increases, petal width consistently increases alongside it.

### 2. Key Observations
- **Strong Positive Linear Correlation:** Data points trend upward from bottom-left to top-right with minimal scatter, indicating a strong positive correlation coefficient ($r \approx 0.96$).
- **Bimodal Distribution / Distinct Clusters:** 
  - **Cluster 1 (Bottom-Left):** Represents flowers with short petals ($\le 2\text{ cm}$) and narrow widths ($\le 0.6\text{ cm}$), corresponding to *Iris setosa*.
  - **Cluster 2 (Upper-Right):** Represents flowers with longer petals ($3\text{ cm} - 7\text{ cm}$) and larger widths ($1.0\text{ cm} - 2.5\text{ cm}$), corresponding to *Iris versicolor* and *Iris virginica*.
- **Predictive Power:** Due to the clear linear trend and tight grouping, `petal_length` is an effective feature for predicting `petal_width`.

---

## Interview Questions & Answers

### Q1: What is a scatter plot?
**Answer:**  
A scatter plot is a Cartesian visualization technique that displays values for two numerical variables using individual dots. Each dot represents a single observation in the dataset, positioned according to its values on the horizontal (X) and vertical (Y) axes. It is primarily used to discover correlations, clusters, outliers, and trend lines between continuous variables.

### Q2: What does a positive relationship mean?
**Answer:**  
A positive relationship (or positive correlation) means that as the value of one variable increases, the value of the other variable tends to increase as well. On a scatter plot, this pattern appears as a collection of points ascending from the lower-left to the upper-right.

### Q3: Does correlation always mean causation?
**Answer:**  
No, **correlation does not imply causation**. Correlation indicates that two variables move together in a statistically predictable way, but it does not prove that one variable causes the change in the other. Observed correlations can be coincidental or influenced by confounding/lurking variables. Proving causation requires experimental controls or causal inference framework testing.
