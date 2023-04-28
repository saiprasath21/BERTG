# CS7650 Final Project
# BERTG: Graph Augmented Transformer for Text Classification
We propose the BERTG model that augments transformer based models with Graph Neural Networks (GNN). By combining the local structural relationship between input documents learnt by the GNN, with the contextual embeddings learnt by transformer based models, the proposed BERTG model outperforms existing baselines(BERT, GCN) in terms of precision, recall, and F1 scores across multiple classes, and for varying training data sizes. We demonstrate the performance of the BERTG model on the Amazon Reviews Dataset classification task, by comparing the performance with two baseline models: BERT and GCN. Our proposed architecture achieves improved performance using lesser training data proving both advantageous and efficient.

## [Dataset](./Dataset/Software_5.json.gz)

We use the“Software" category of the [Amazon reviews dataset](https://nijianmo.github.io/amazon/index.html)which has 12803 datapoints. We ignore all the user and rating metadata, and consider only the user’s text input for this project. The average length of the review is 175.98 words, with a total of 101170 unique words in the dataset. There are five different rating classes (1-5) in the dataset, and the distribution is: {1: 1500, 2: 719, 3: 1598, 4:
3016, 5: 5971}.
Samples:
![image](https://user-images.githubusercontent.com/93538009/235259275-0add0de9-538b-4726-8e65-5d4368bb1f04.png)
![image](https://user-images.githubusercontent.com/93538009/235260520-d99e5186-f064-4740-b96d-12871cbf3be3.png)



