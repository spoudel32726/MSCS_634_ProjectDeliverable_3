
 Project Overview
This project applies classification, clustering, and association rule mining techniques to the Online Retail Dataset (UCI Machine Learning Repository). The dataset contains customer transactions, making it ideal for customer segmentation, prediction of high-value customers, and discovery of purchase patterns.
Key tasks completed:
Developed and evaluated classification models (Decision Tree, k-NN).


Applied hyperparameter tuning using GridSearchCV for Decision Trees.


Built K-Means clustering for customer/product grouping.


Applied FP-Growth to identify frequent itemsets and strong association rules.


Created visualizations to communicate insights clearly.



 Classification Model Development
Two classification models were implemented:
Decision Tree Classifier


Baseline model performed with Accuracy = 0.64 and F1 = 0.73.


k-Nearest Neighbors (k=5)


Achieved Accuracy = 0.62 and F1 = 0.71.


Hyperparameter tuning was performed for the Decision Tree using GridSearchCV:
Optimal parameters: max_depth = 5, min_samples_split = 5.


Slightly improved interpretability, with performance at Accuracy = 0.62, F1 = 0.72.


Evaluation metrics included:
Confusion matrices.


ROC curves with AUC comparison.


Accuracy and F1 scores.


 Key Insight: Decision Trees performed slightly better than k-NN, and both models can distinguish high-value customers but with moderate predictive power.

 Clustering Model Development
A K-Means clustering model was developed with k=3 clusters. Results showed:
Cluster 0: Low-spend, frequent purchases (typical day-to-day buyers).


Cluster 1: Premium buyers (low volume, high price items).


Cluster 2: Bulk buyers (large quantities, often low unit price).


Key Insight: Clustering provides segmentation that businesses can use for targeted marketing, loyalty programs, or specialized promotions.

Association Rule Mining
The FP-Growth algorithm was applied to extract frequent itemsets and generate association rules.
Example frequent itemsets:


jumbo bag red retrospot


regency cakestand 3 tier


party bunting


Example strong rules:


lunch bag black skull → lunch bag pink polkadot (Confidence = 0.92, Lift = 13.1)


lunch bag pink polkadot → lunch bag black skull (Confidence = 0.79, Lift = 13.1)


Key Insight: Strong product associations reveal cross-selling opportunities. For instance, customers buying themed lunch bags are very likely to purchase complementary designs.
Visualizations
Top 20 frequent items bar chart.


Co-occurrence heatmap of top 20 items.


ROC curves comparing classifier performance.


K-Means clustering results (scatter plot with clusters).


 Key Insight: Visualizations provided clear evidence of purchase trends, model performance, and customer groupings.

Challenges and Solutions
Class imbalance: High-value customers represented a smaller share. Addressed by using the 75th percentile spend threshold for balanced labeling.


Feature limitations: Dataset contained limited numeric features; applied scaling and engineered TotalSpend to strengthen classification.


Association mining complexity: Limited to a sample of transactions (200 invoices) for computational feasibility while still capturing strong patterns.


 Practical Applications
Retail Strategy: Identifying high-value customers helps prioritize loyalty efforts.


Customer Segmentation: Clustering enables differentiated campaigns (e.g., bulk discounts vs. premium offers).


Cross-Selling: Association rules suggest which products to bundle together to increase basket size.


Operational Efficiency: Insights can guide inventory management by stocking commonly co-purchased products together.



Repository Checklist:  MSCS_634_ProjectDeliverable_3.ipynb – notebook with code, outputs, and visuals.
README.md – this file.

