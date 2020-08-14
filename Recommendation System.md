
# Recommendation System

## Matrix Factorization

1. [Multiverse Recommendation: N-dimensional Tensor Factorization for Context-aware Collaborative Filtering](https://xamat.github.io/pubs/karatzoglu-recsys-2010.pdf)

> HOSVD decomposition, high dimension factorization with a central tensor<br>
> Hard to make explaination about the central tensor.

2. [Relational Learning via Collective Matrix Factorization](http://www.cs.cmu.edu/~ggordon/singh-gordon-kdd-factorization.pdf)
> Assign 0 of the learning rate for unobserved entries<br>
> Generialize to n-d matrix<br>
>Same latent matrix for the same entity for different relationship


3. [Item Cold-Start Recommendations: Learning Local Collective Embeddings](http://web.media.mit.edu/~msaveski/assets/publications/2014_item_cold_start/paper.pdf)

>Common latent space with locality added<br>
> Easy to follow optimization process<br>
> An extension of 2.

4. [Deep Tensor Factorization for Multi-Criteria Recommender Systems](https://ieeexplore.ieee.org/document/9005677)

> Standard tensor factorization ==> 3 latent matrices  <br>
> Use stacked denoising autoencoder to get the latent matrix for user and item<br>
> Claim to handle sparse problem in tensor factorization by using autoencoder to reduce dimension<br>

5. [DeepFM: An End-to-End Wide & Deep Learning
Framework for CTR Prediction](https://arxiv.org/pdf/1804.04950.pdf)
#### Problems Addressed:
>* CNN tends to bias toward neighboring interactions
>* RNN tends to bias toward sequential dependency
>* Low order & high order feature interactions should both be incorporated

![](/deepfm1.png)

>Build a Deep Neural Net to implenment FM structure, embedding layers captures the factorization part<br>
>End to End network without pretrain for latent vector
>Prone to overfitting, use dropout to prevent it


## Deep Learning Based

1. [Deep Interest Evolution Network for Click-Through Rate Prediction](https://arxiv.org/pdf/1809.03672.pdf)

>AUGRU attentional update gate GRU for interest evolution<br>
> Create "attention weight" based on last behavior and current behavior and evolve hidden state in GRU<br>
>Able to handle user historical behavior, Item list, user profile, context at the same time<br>

2. [BERT4Rec: Sequential Recommendation with Bidirectional
Encoder Representations from Transformer](https://arxiv.org/pdf/1904.06690.pdf)

> BERT for recommendation system, very similar to BERT in language modeling<br>
> Claim to be state of the art recommendation algorithm<br>
> Trained positional embedding<br>


3. [Personalized Top-N Sequential Recommendation via Convolutional Sequence Embedding](http://www.sfu.ca/~jiaxit/resources/wsdm18caser.pdf)

>Deep learning for Sequential Recommendation. Capable of recommending items in different categories.

4. [Deep Neural Networks for YouTube Recommendations](https://static.googleusercontent.com/media/research.google.com/en//pubs/archive/45530.pdf)
> 2 step recommendation: candidate generation + ranking<br>
> Recommendation as Classification: Learn user embedding in classification

![](/dnnforyoutube.png) 
![](/dnnforyoutube2.png)

#### Key Take Aways:
> * perform average on embeddings<br>
> * feed the timestamp of video(product) as a feature to add the time sensitivity to the model<br>
> * control the influence of dominating users by restrict sample size from certain users<br>
> * Aware of the user consumption sequence<br>

## Online Learning

1. [How to Retrain Recommender System? A Sequential Meta-Learning Method](https://arxiv.org/pdf/2005.13258.pdf)

>New way to incorperate new data. Use NN (CNN) to model the update from W_{t-1} to W_{t}<br>
>However, the transfer model itself is hard to design and optimize. It also does not account for second order time dependency.

## Rule Based

https://arxiv.org/ftp/arxiv/papers/2005/2005.14026.pdf

## Regression Based

1. [Pairwise Preference Regression for Cold-start Recommendation](http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.211.9762&rep=rep1&type=pdf)

> Used normalized Discounted Cumulative Gain (𝑛𝐷𝐶𝐺) as evaluation matrix for ranking<br>
> Pairwise loss designed for multiple items recommended to the same user<br>
> Recommendation is evaluated in terms of the item ranking for a user in the case that each user needs a recommendation<br>
> Closed form solution<br>
> Idea in cold start testing: random select half user(item) as new user(item) to test model performance in cold start

## Reinforcement Learning

1. [Generative Adversarial User Model for RL Based Recommendation System](https://arxiv.org/pdf/1812.10613v3.pdf)

> Fine designed reward function for the recommendation, Generative Adversarial Training to mimic rewarding function<br>
> User history as state, weighted/truncated M-step history can also be used<br>
> Cascading Q-learning (introduced by this paper), small modification in Q-learning<br>
> Neuralnet structure for Q value<br>
> Adding a GAN to estimate reward offers more flexibility to the reward function of a user

## Graph Neural Network
1. [ATBRG: Adaptive Target-Behavior Relational Graph Network
for Effective Recommendation](https://arxiv.org/pdf/2005.12002.pdf)

#### Problems Addressed

>* current GNN cannot deal with users' history & interest
>* current neightbour sample may mis-sample irrelevant information while leave out important nodes
>* GNN based methods do not take mutual influence between target user behaviors and item into consideration in the procedure of information aggregation

![](/ATBRG1.png)

### Key Points
> Graph Connect: Find entity connections that user's historical behavior & target have in common<br>
> Graph Prune:  Prune the entities which do not connect different items
> Attention Layer: Weigh each item differently based on how related the item is to the target item

![](/ATBRN2.png)


2. [Unifying Knowledge Graph Learning and Recommendation:
Towards a Better Understanding of User Preferences](https://arxiv.org/pdf/1902.06236.pdf)




## Evaluation Matrix

1. [Beyond Optimizing for Clicks: Incorporating Editorial Values in News Recommendation](https://arxiv.org/pdf/2004.09980.pdf)

> Recommendation system for news focusing on 4 matrices in result evaluation: diversity, coverage, serendipity, and dynamism<br>
> **Diversity**: Inverse of the simmlarity of recommended item. Based on similarity of features<br>
> **Coverage**: The proportion of recommended items over all items<br>
>**Serendipity**: Inverse of simmlarity of recommended item v.s. user history<br>
>**Dynamism**: The recency of timestamp for each recommended items<br>
> Item simmlarity is useful in the evaluation. Actually most of such matrices can be added as a loss function in the recommendation algorithm, which is not fully discussed in the paper

## Survey

1. [Deep Learning based Recommender System: A Survey and New Perspectives](https://arxiv.org/pdf/1707.07435.pdf)
