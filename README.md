# Cultural Patterns Analysis using World Values Survey (WVS)

## Overview
This project explores cultural patterns across nations using the World Values Survey (WVS) dataset. By employing hierarchical clustering and data enrichment techniques, the project provides insights into how cultural values vary globally and correlate with socioeconomic and political factors such as GDP per capita, political regime types, and more.

## Objectives
- Identify clusters of countries based on cultural indices derived from the WVS dataset.
- Analyze the relationship between cultural values and external factors such as regime type and economic indicators.
- Provide a comprehensive understanding of global cultural trends and their implications for societal development.

## Dataset
- **Source**: World Values Survey (Seventh Wave, 2017-2022).
- **Size**: Data from 66 countries and territories, encompassing 89,940 rows after cleaning.
- **Key Features**:
  - **Cultural Indices**: Defiance, Disbelief, Relativism, Scepticism, Autonomy, Equality, Choice, and Voice.
  - **Socioeconomic and Political Variables**: GDP per capita, regime type, population size, etc.

## Technologies and Tools
- **Programming Languages**: Python, R.
- **Libraries**:
  - `scikit-learn` for clustering and multidimensional scaling (MDS).
  - `pandas` and `numpy` for data manipulation.
  - `matplotlib` and `seaborn` for visualization.
  - R packages for self-organizing maps (SOM).

## Project Components
### 1. Data Preparation
- **Data Cleaning**: Removal of missing values, consolidation of responses, and standardization.
- **Data Enrichment**: Integration of external data on GDP, population, and regime type using ISO country codes.

### 2. Feature Selection
- Focused on eight cultural indices constructed from survey responses.
- Additional variables include regime type, GDP per capita, and educational levels.

### 3. Clustering Analysis
- **Hierarchical Clustering**: Used to identify clusters of countries based on cultural indices.
  - Best results obtained using Ward's method.
  - Visualized using dendrograms and MDS.
- **Additional Experiments**:
  - K-means clustering with UMAP for dimensionality reduction.
  - Silhouette score used to validate the number of clusters.

### 4. Results and Interpretation
- Identified 9 distinct clusters of countries, each characterized by unique cultural and socioeconomic traits:
  - Cluster 0: Predominantly Asian and African countries with high religiosity and low civil liberties.
  - Cluster 5: Affluent Western nations with progressive values and high education levels.
  - [Other clusters detailed in the report].
- Insights into the impact of regime type and GDP per capita on cultural values.



## Usage
1. Preprocess the dataset:
   ```bash
   python preprocess_data.py
   ```
2. Perform clustering analysis:
   ```bash
   python clustering_analysis.py
   ```
3. Generate visualizations:
   ```bash
   python generate_visualizations.py
   ```

## References
- [World Values Survey](https://www.worldvaluessurvey.org/wvs.jsp)
- [Scikit-learn Documentation](https://scikit-learn.org/stable/)
- [R Kohonen Package](https://cran.r-project.org/web/packages/kohonen/index.html)
