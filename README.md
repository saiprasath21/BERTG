# CS7650 Final Project
# BERTG: Graph Augmented Transformer for Text Classification
We propose the BERTG model that augments transformer based models with Graph Neural Networks (GNN). By combining the local structural relationship between input documents learnt by the GNN, with the contextual embeddings learnt by transformer based models, the proposed BERTG model outperforms existing baselines(BERT, GCN) in terms of precision, recall, and F1 scores across multiple classes, and for varying training data sizes. We demonstrate the performance of the BERTG model on the Amazon Reviews Dataset classification task, by comparing the performance with two baseline models: BERT and GCN. Our proposed architecture achieves improved performance using lesser training data proving both advantageous and efficient.

## [Dataset](./Dataset/Software_5.json.gz)

We use the“Software" category of the [Amazon reviews dataset](https://nijianmo.github.io/amazon/index.html)which has 12803 datapoints. We ignore all the user and rating metadata, and consider only the user’s text input for this project. The average length of the review is 175.98 words, with a total of 101170 unique words in the dataset. There are five different rating classes (1-5) in the dataset, and the distribution is: {1: 1500, 2: 719, 3: 1598, 4:
3016, 5: 5971}.
### Samples:
![image](https://user-images.githubusercontent.com/93538009/235259275-0add0de9-538b-4726-8e65-5d4368bb1f04.png)

![image](https://user-images.githubusercontent.com/93538009/235261694-dce6b6ce-4334-4272-a2e2-ee68421730b6.png)

## [Implementation](./BERTG.ipynb)
The proposed BERTG model captures both the local structural information, and the contextual information by combining the BERT and the GCN model respectively. The document node embeddings learnt by the GCN model is concatenated with the embeddings of the ‘[CLS]’ token from the last hidden state of the BERT model, before being passed to an MLP for classification. We analyse two different models: (1) BERT - Pretrained + GCN with Pretrained node initialization, and (2)BERT - Finetuned + GCN with Finetuned weight initialization.
The code in the [code notebook](./BERTG.ipynb) is organised to first show baseline BERT model, then how it is finetuned, graph creation, Baseline GCN model based on created graph using pretrained BERT embeddings, GCN model based on finetuned BERT Embeddings and finally the BERTG architecture that has Graph augmented BERT embeddings passed to an MLP for text classification

## Empirical analysis of our approach
<img width="546" alt="image" src="https://user-images.githubusercontent.com/93538009/235262555-7f100015-2afd-4670-88eb-5aec8e5cc6d1.png">
<div><img width="400" alt="image" src="https://user-images.githubusercontent.com/93538009/235262657-62e6d590-280a-4852-98e5-d283ee3248e3.png"> <img width="450" alt="image" src="https://user-images.githubusercontent.com/93538009/235262612-35748119-2709-441c-9975-b05b6d05e723.png"></div>



