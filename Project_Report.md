# Project Report: Customer Segmentation Using K-Means Clustering

**Course:** AIML Minor Project — Boosting / Unsupervised Learning  
**Dataset:** Mall Customer Segmentation Data  
**Source:** https://www.kaggle.com/datasets/vjchoudhary7/customer-segmentation-tutorial-in-python

## 1. Problem statement
Retail businesses serve customers with different income levels and spending behaviours. Treating every customer identically may make marketing less relevant. This project explores whether customers can be grouped into interpretable segments using annual income and spending score, while also examining age and basic data quality.

## 2. Objectives
1. Understand the dataset and its features.
2. Check missing values, duplicates, data types, and invalid ranges.
3. Create at least four visualizations with observations.
4. Apply K-Means clustering after scaling features.
5. compare candidate cluster counts using the elbow method and silhouette score.
6. Profile the segments and propose cautious, testable marketing actions.

## 3. Dataset description
The dataset commonly contains 200 customer records and five fields: CustomerID, Gender, Age, Annual Income (k$), and Spending Score (1–100). CustomerID identifies records; Spending Score is a mall-assigned score based on observed customer behaviour. Dataset size and column definitions should be verified after downloading the CSV.

## 4. Data preparation
The notebook standardizes column names, checks missing values and duplicate rows, removes exact duplicates, excludes rows missing the core numeric fields, and flags/removes values outside broad validity ranges. Customer ID is excluded from clustering because it is an identifier rather than a behavioural feature. The primary clustering features are annual income and spending score. These features are standardized because K-Means is distance-based.

## 5. Exploratory analysis
The notebook includes:
- Age distribution histogram
- Annual income distribution histogram
- Age vs. spending score scatter plot
- Numeric-feature correlation heatmap
- K-Means cluster map with centroids
- Segment-size bar chart
Each chart should be accompanied by a brief observation based on the actual output.

## 6. Method
K-Means assigns each customer to the nearest cluster centroid. Candidate values of k are compared using inertia (within-cluster sum of squared distances) and silhouette score. Silhouette values range from -1 to +1; higher values generally indicate better-separated clusters, while values near zero indicate overlap. The selected k is a baseline chosen from the tested silhouette scores and should also be checked against the elbow plot and interpretability.

## 7. Evaluation and Insights
Baseline k selected by highest silhouette score: 5
Cluster sizes and profiles: 81, 39, 22, 35 and 23 customers
Final silhouette score: 0.555
Final inertia: 65.568
Evaluation method: Elbow method and silhouette score
Accuracy: Not applicable because the dataset has no ground-truth cluster labels.

## 8. Expected business use
After reviewing the calculated cluster profiles, the mall could test different offers for high-income/high-spending, high-income/low-spending, or lower-income/high-spending groups where those patterns actually appear. The suggestions should be treated as experiments and evaluated using real campaign outcomes.

## 9. Limitations
The dataset is small and educational; it may not represent the broader customer population. Spending score is not necessarily actual revenue. There is no transaction history, customer lifetime value, product preference, or time dimension. K-Means favours compact clusters and results depend on feature selection, scaling, and k. Clusters are descriptive and do not establish causality.

## 10. Conclusion
The project builds an end-to-end unsupervised-learning workflow from data cleaning through cluster evaluation and interpretation. The final conclusion should be completed after running the notebook on the Kaggle CSV and inserting the measured silhouette score, chosen cluster count, cluster sizes, and the strongest segment differences. The most useful outcome is a set of understandable customer groups and testable marketing hypotheses—not a claim that the model predicts future spending.

## References
- Kaggle dataset: https://www.kaggle.com/datasets/vjchoudhary7/customer-segmentation-tutorial-in-python
- scikit-learn clustering: https://scikit-learn.org/stable/modules/clustering.html
- StandardScaler: https://scikit-learn.org/stable/modules/generated/sklearn.preprocessing.StandardScaler.html
- Silhouette analysis: https://scikit-learn.org/stable/auto_examples/cluster/plot_kmeans_silhouette_analysis.html
