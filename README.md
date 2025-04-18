# Wine Quality Clustering Analysis

A comprehensive comparative performance study of various clustering algorithms using different preprocessing techniques on the Wine Quality dataset from the UCI Machine Learning Repository.

---

## Objective
To analyze and compare the effectiveness of multiple clustering algorithms on the **Wine Quality** dataset by:
- Applying different preprocessing techniques
- Using different cluster numbers
- Evaluating clustering performance using multiple metrics
- Visualizing the results for interpretability
---

## Dataset
- **Source**: [UCI Machine Learning Repository - Wine Quality](https://archive.ics.uci.edu/ml/datasets/Wine+Quality)
- **File Used**: `winequality-white.csv`
- **Attributes**: 11 physicochemical input variables (e.g. acidity, sugar, pH) + 1 output variable (quality score)
---

## Preprocessing Techniques Applied
| Technique Name         | Description                                                |
|------------------------|------------------------------------------------------------|
| No Data Processing     | Raw dataset without any preprocessing                      |
| Normalization          | Scales all features between 0 and 1 using MinMaxScaler     |
| Log Transformation     | Applies `log1p` transformation to reduce skewness          |
| PCA                    | Dimensionality reduction (2 principal components)          |
| Transform + Normalize  | Applies log transform followed by normalization            |
| T + N + PCA            | Log transform → Normalize → PCA                            |

---

## Clustering Algorithms Used
| Algorithm             | Description                                                |
|-----------------------|------------------------------------------------------------|
| K-Means               | Partitional clustering with user-defined `k`               |
| Agglomerative         | Hierarchical clustering using bottom-up approach           |
| MeanShift             | Centroid-based clustering based on kernel density estimate |

---

## Evaluation Metrics
| Metric                 | Description                                                   |
|------------------------|---------------------------------------------------------------|
| Silhouette Score       | Measures how similar a point is to its own cluster            |
| Calinski-Harabasz Index| Ratio of between-cluster dispersion to within-cluster dispersion |
| Davies-Bouldin Score   | Average similarity between each cluster and its most similar one (lower is better) |

---

## Results
Results are saved in `wine_clustering_results.csv`.
| Algorithm     | Preprocessing      | Clusters | Silhouette | Calinski-Harabasz | Davies-Bouldin |
|---------------|--------------------|----------|------------|-------------------|----------------|
| KMeans        | Using PCA          | 3        | 0.395      | 402               | 0.58           |
| Hierarchical  | T + N              | 4        | 0.372      | 331               | 0.69           |
| MeanShift     | No Data Processing | 2        | 0.482      | 387               | 0.43           |
| ...           | ...                | ...      | ...        | ...               | ...            |

---

## Visualizations
- **Bar Charts**: Comparison of metrics across algorithms and preprocessing
  ![image](https://github.com/user-attachments/assets/1ba5cfd8-48a0-4ea8-bc97-98396b7d7052)
  ![image](https://github.com/user-attachments/assets/a352d7d9-e335-4eef-a8cb-5ba9b49edae4)
  ![image](https://github.com/user-attachments/assets/ab818731-4664-4909-8ad8-c71d92d545a7)

- **Heatmap**: Silhouette scores for different cluster numbers (KMeans)
  ![image](https://github.com/user-attachments/assets/cf732a3c-1886-4aa2-9907-7553cb1da5d5)
  
- **Scatter Plot**: PCA-based 2D visualization with cluster coloring
  ![image](https://github.com/user-attachments/assets/f43bc134-59d0-448b-8334-cea67a7515e4)

---

## How to Run
1. Clone this repo:
   ```bash
   git clone https://github.com/rishikam23/Clustering-Techniques.git
   cd wine-clustering-analysis
   ```
2. Open wine_clustering_analysis.ipynb in Google Colab or Jupyter Notebook
3. Run all cells to generate results and visualizations
---

## License
This project is licensed under the MIT License.

---

## Contributing
Contributions and collaborations are welcome and encouraged!  
Feel free to fork the repo, open issues, or submit pull requests to improve or expand the project. Let's make it better together!

---
