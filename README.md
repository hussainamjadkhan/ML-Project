# Document Clustering of BBC News Articles

## Unsupervised Machine Learning Project

### Project Overview

This project applies unsupervised learning techniques to automatically group BBC news articles into meaningful topic clusters without using predefined labels.
The goal is to discover natural topic structures in news data using text mining and clustering algorithms.

The project compares K-Means, Hierarchical Clustering, and DBSCAN, and evaluates their performance using multiple clustering metrics.


### Dataset

Dataset: BBC News Articles

Total Articles: 2,225

Categories (for validation only):

Business

Entertainment

Politics

Sport

Tech

Labels are not used during training — they are only used for evaluation.


### Methodology

The complete pipeline includes:

Text Preprocessing

Lowercasing

Removing punctuation, numbers, URLs

Tokenization

Stopword removal

Lemmatization (NLTK)

Feature Extraction

TF-IDF Vectorization

Unigrams + Bigrams

Vocabulary size limited to 10,000

Dimensionality Reduction

Latent Semantic Analysis (Truncated SVD)

Reduced to 100 dimensions

Clustering Algorithms

K-Means (k = 9 selected using evaluation metrics)

Hierarchical Clustering (Ward linkage)

DBSCAN (tested, but unsuitable for this dataset)

Evaluation Metrics

Silhouette Score

Davies–Bouldin Index

Calinski–Harabasz Score

Cluster Purity (vs true labels)

Visualization

t-SNE 2D projections for cluster visualization


### Results Summary

Best Algorithm: K-Means

Optimal Clusters: 9

Silhouette Score: 0.0907

Cluster Purity: 95%+ for most clusters

Key Insight:

The model discovered subtopics within traditional categories:

Sports → motorsports, team sports, individual sports

Entertainment → movies & music

Business → economy & corporate finance

This shows that natural topic structure is more fine-grained than human labels.


### Technologies Used

Python 3

Jupyter Notebook

pandas, numpy

scikit-learn

nltk

matplotlib, seaborn
