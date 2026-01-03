# *Document Clustering of BBC News Articles*

## *Unsupervised Machine Learning Project*

### *Project Overview*

  This project applies unsupervised learning techniques to automatically group BBC news articles   into meaningful topic clusters without using predefined labels.
  The goal is to discover natural topic structures in news data using text mining and clustering   algorithms.
  
  The project compares K-Means, Hierarchical Clustering, and DBSCAN, and evaluates their           performance using multiple clustering metrics.


### *Dataset*

  . Dataset: BBC News Articles
  . Total Articles: 2,225
  . Categories (for validation only):
      .Business
      .Entertainment
      .Politics
      .Sport
      .Tech
  
  Labels are **NOT** used during training — they are only used for evaluation.


### *Methodology*

  **The complete pipeline includes:**
  1. Text Preprocessing
    . Lowercasing
    . Removing punctuation, numbers, URLs
    . Tokenization
    . Stopword removal
    . Lemmatization (NLTK)
  
  2. Feature Extraction
    . TF-IDF Vectorization
    . Unigrams + Bigrams
    . Vocabulary size limited to 10,000
  
  3. Dimensionality Reduction
    . Latent Semantic Analysis (Truncated SVD)
    . Reduced to 100 dimensions
  
  4. Clustering Algorithms
    . K-Means (k = 9 selected using Elbow Method)
    . Hierarchical Clustering (Ward linkage)
    . DBSCAN (tested, but unsuitable for this dataset)
  
  5. Evaluation Metrics
    . Silhouette Score
    . Davies–Bouldin Index
    . Calinski–Harabasz Score
    . Cluster Purity (vs true labels)
  
  6. Visualization
    . t-SNE 2D projections for cluster visualization


### *Results Summary*

  . Best Algorithm: K-Means
  . Optimal Clusters: 9
  . Silhouette Score: 0.0907
  . Cluster Purity: 95%+ for most clusters
  
  **Key Insight:**
  
  . The model discovered subtopics within traditional categories:
  . Sports → motorsports, team sports, individual sports
  . Entertainment → movies & music
  . Business → economy & corporate finance
  . This shows that natural topic structure is more fine-grained than human labels.


### *Technologies Used*
  
  1. Python 3
  2. Jupyter Notebook
  3. pandas, numpy
  4. scikit-learn
  5. nltk
  6. matplotlib, seaborn
