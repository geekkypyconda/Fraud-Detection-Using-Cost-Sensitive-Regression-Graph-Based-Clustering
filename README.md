# Fraud-Detection-Using-Cost-Sensitive-Regression-Graph-Based-Clustering

## Cost-Sensitive-Regression

### Link for the Dataset: https://drive.google.com/drive/folders/1OU_cbT1X7mVJupgLX_bz55JFv8EdOsjP?usp=sharing

### This project explores cost-sensitive logistic regression models for binary classification. Traditional logistic regression treats false positives and false negatives equally, which may not align with real-world scenarios where different misclassifications carry varying penalties. 

This project implements two cost-sensitive approaches:

* Bahnsen's approach: Incorporates example-dependent costs into logistic regression, adjusting penalties for different types of misclassifications. It’s particularly useful for applications like credit scoring, where the cost of a false negative may be much higher than a false positive.

* Gunnemann's approach: Focuses on applying distinct penalties for misclassifications, based on a predefined cost structure, and aims to minimize the total misclassification cost during model training.

Both models were trained and evaluated on a custom dataset, comparing the performance and trade-offs introduced by these cost-sensitive methods. However, due to heavy penalties for true positives, the models underfitted the data.

----------------------------------------------------------------------------------------------------------------------------------------------------------------------------
----------------------------------------------------------------------------------------------------------------------------------------------------------------------------

## Identify-clusters-using-Node2Vec-Embedding-Spectral-and-GCN-embeddings
This project identifies clusters in a transaction dataset using three node embedding techniques: Node2Vec, Spectral Embedding, and Graph Convolutional Networks (GCN). The dataset consists of sender-receiver payment transactions, with the transaction amount as the edge weight in the graph.

### Link for Dataset: https://drive.google.com/file/d/1fvg_uOfLAJKfZwBiH-ofzejJLcLRHA45/view?usp=sharing

## Methodology:
### Data Processing:
* The transaction data was transformed into a graph where each node represents a sender or receiver, and edges are weighted by the transaction amounts.

### Embeddings:
* Node2Vec: Performed random walks on the graph and used skip-gram to generate 8-dimensional embeddings, later reduced to 3 dimensions via PCA.
* Spectral Embedding: Created an adjacency matrix, followed by a Laplacian matrix. The largest three eigenvectors were used to form the embeddings.
* GCN Embedding: Built a graph convolutional network to capture structural information in the graph.

### Clustering:
* Used K-Means clustering to detect patterns of fraudulent and non-fraudulent transactions, with the number of clusters set to 2.
