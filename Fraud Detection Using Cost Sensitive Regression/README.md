# Cost-Sensitive-Regression

## Link for the Dataset: https://drive.google.com/drive/folders/1OU_cbT1X7mVJupgLX_bz55JFv8EdOsjP?usp=sharing

### This project explores cost-sensitive logistic regression models for binary classification. Traditional logistic regression treats false positives and false negatives equally, which may not align with real-world scenarios where different misclassifications carry varying penalties. 

This project implements two cost-sensitive approaches:

* Bahnsen's approach: Incorporates example-dependent costs into logistic regression, adjusting penalties for different types of misclassifications. It’s particularly useful for applications like credit scoring, where the cost of a false negative may be much higher than a false positive.

* Gunnemann's approach: Focuses on applying distinct penalties for misclassifications, based on a predefined cost structure, and aims to minimize the total misclassification cost during model training.

Both models were trained and evaluated on a custom dataset, comparing the performance and trade-offs introduced by these cost-sensitive methods. However, due to heavy penalties for true positives, the models underfitted the data.
