# US Crime Rates Clustering Analysis

This project analyzes violent crime statistics across the 50 U.S. states using unsupervised learning techniques, primarily **K-Means clustering**. The goal is to explore patterns in murder, assault, rape, and urbanization rates and understand how states cluster based on these indicators.

---

## 📁 Dataset Overview

- **Source**: `US_violent_crime.csv` : https://www.kaggle.com/datasets/mathchi/violent-crime-rates-by-us-state
- **Features**:
  - `Murder`: Number of murders per 100,000 residents
  - `Assault`: Number of assaults per 100,000 residents
  - `UrbanPop`: Percentage of urban population
  - `Rape`: Number of rapes per 100,000 residents

---

## Exploratory Data Analysis (EDA)

- Checked data types and nulls: Clean data, no missing values
- Descriptive statistics and distributions
- **Correlation Matrix**:
  - `Murder` and `Assault`: Strong positive correlation (0.80)
  - `Rape` shows moderate correlation with both
  - `UrbanPop` is weakly correlated with crime

---

## Clustering Workflow

### Hopkins Test

- Score ≈ 0.37 → Weak natural clustering tendency
- Still proceeded with clustering for learning purposes

### K-Means Clustering

- Initial clustering with `k=2`
- Refined with **Elbow Method** and **Yellowbrick** to find optimal `k`
- Final model: **k=4 clusters**

### Evaluation

- **Silhouette Score**: ~0.50 → Fairly well-clustered structure
- **Adjusted Rand Index (ARI)**: ~0.22 → Weak alignment with any predefined labels

---

## Visualizations

- Static cluster scatter plots (matplotlib)
- Cluster centroids highlighted
- Interactive visualization with Plotly
- Correlation heatmaps
- Elbow plot for optimal `k`

---

## Tech Used

- Python 3
- pandas, numpy
- seaborn, matplotlib, plotly
- scikit-learn, yellowbrick
- pyclustertend (Hopkins statistic)

---

## Key Insights

- States naturally group by high vs. low violent crime rates
- Urban population doesn’t significantly correlate with violent crime
- Strong link found between murder and assault trends
- Clustering remains useful for categorizing states into similar profiles, even if natural groupings are weak
