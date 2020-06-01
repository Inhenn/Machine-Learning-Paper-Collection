# Recommendation System

## Matrix Factorization

1. [Multiverse Recommendation: N-dimensional Tensor Factorization for Context-aware Collaborative Filtering](https://xamat.github.io/pubs/karatzoglu-recsys-2010.pdf)

&nbsp; &nbsp; &nbsp; &nbsp; HOSVD decomposition, high dimension factorization with a central tensor

&nbsp; &nbsp; &nbsp; &nbsp; Hard to make explaination about the central tensor.

2. [Relational Learning via Collective Matrix Factorization](http://www.cs.cmu.edu/~ggordon/singh-gordon-kdd-factorization.pdf)

&nbsp; &nbsp; &nbsp; &nbsp; Assign 0 of the learning rate for unobserved entries
        
&nbsp; &nbsp; &nbsp; &nbsp; Generialize to n-d matrix
        
&nbsp; &nbsp; &nbsp; &nbsp; Same latent matrix for the same entity for different relationship
        
        
3. [Item Cold-Start Recommendations: Learning Local Collective Embeddings](http://web.media.mit.edu/~msaveski/assets/publications/2014_item_cold_start/paper.pdf)
        
&nbsp; &nbsp; &nbsp; &nbsp; Common latent space with locality added
        
&nbsp; &nbsp; &nbsp; &nbsp; Easy to follow optimization process

&nbsp; &nbsp; &nbsp; &nbsp; An extension of 2.

4. [Deep Tensor Factorization for Multi-Criteria Recommender Systems](https://ieeexplore.ieee.org/document/9005677)

&nbsp; &nbsp; &nbsp; &nbsp; Standard tensor factorization ==> 3 latent matrices  

&nbsp; &nbsp; &nbsp; &nbsp; Use stacked denoising autoencoder to get the latent matrix for user and item

&nbsp; &nbsp; &nbsp; &nbsp; Claim to handle sparse problem in tensor factorization by using autoencoder to reduce dimension


## Deep Learning Based

1. [Deep Interest Evolution Network for Click-Through Rate Prediction](https://arxiv.org/pdf/1809.03672.pdf)

&nbsp; &nbsp; &nbsp; &nbsp; AUGRU attentional update gate GRU for interest evolution

&nbsp; &nbsp; &nbsp; &nbsp; Create "attention weight" based on last behavior and current behavior and evolve hidden state in GRU

&nbsp; &nbsp; &nbsp; &nbsp; Able to handle user historical behavior, Item list, user profile, context at the same time

2. [BERT4Rec: Sequential Recommendation with Bidirectional
Encoder Representations from Transformer](https://arxiv.org/pdf/1904.06690.pdf)

&nbsp; &nbsp; &nbsp; &nbsp; BERT for recommendation system, very similar to BERT in language modeling 

&nbsp; &nbsp; &nbsp; &nbsp; Claim to be state of the art recommendation algorithm 

&nbsp; &nbsp; &nbsp; &nbsp; Trained positional embedding


3. [Personalized Top-N Sequential Recommendation via Convolutional Sequence Embedding (http://www.sfu.ca/~jiaxit/resources/wsdm18caser.pdf)

&nbsp; &nbsp; &nbsp; &nbsp Deep learning for Sequential Recommendation. Capable of recommending items in different categories.

## Online Learning

1. [How to Retrain Recommender System? A Sequential Meta-Learning Method](https://arxiv.org/pdf/2005.13258.pdf) 

&nbsp; &nbsp; &nbsp; &nbsp; New way to incorperate new data. Use NN (CNN) to model the update from W_{t-1} to W_{t}

&nbsp; &nbsp; &nbsp; &nbsp; However, the transfer model itself is hard to design and optimize. It also does not account for second order time dependency.

## Rule Based

https://arxiv.org/ftp/arxiv/papers/2005/2005.14026.pdf

## Regression Based

1. [Pairwise Preference Regression for Cold-start Recommendation](http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.211.9762&rep=rep1&type=pdf)

&nbsp; &nbsp; &nbsp; &nbsp; Used normalized Discounted Cumulative Gain (𝑛𝐷𝐶𝐺) as evaluation matrix for ranking

&nbsp; &nbsp; &nbsp; &nbsp; Pairwise loss designed for multiple items recommended to the same user

&nbsp; &nbsp; &nbsp; &nbsp; Recommendation is evaluated in terms of the item ranking for a user in the case that each user needs a recommendation

&nbsp; &nbsp; &nbsp; &nbsp; Closed form solution

&nbsp; &nbsp; &nbsp; &nbsp; Idea in cold start testing: random select half user(item) as new user(item) to test model performance in cold start

## Reinforcement Learning

1. [Generative Adversarial User Model for RL Based Recommendation System](https://arxiv.org/pdf/1812.10613v3.pdf)

&nbsp; &nbsp; &nbsp; &nbsp; Fine designed reward function for the recommendation, Generative Adversarial Training to mimic rewarding function

&nbsp; &nbsp; &nbsp; &nbsp; User history as state, weighted/truncated M-step history can also be used

&nbsp; &nbsp; &nbsp; &nbsp; Cascading Q-learning (introduced by this paper), small modification in Q-learning

&nbsp; &nbsp; &nbsp; &nbsp; Neuralnet structure for Q value

&nbsp; &nbsp; &nbsp; &nbsp; Adding a GAN to estimate reward offers more flexibility to the reward function of a user

## Evaluation Matrix

1. [Beyond Optimizing for Clicks: Incorporating Editorial Values in News Recommendation](https://arxiv.org/pdf/2004.09980.pdf)

&nbsp; &nbsp; &nbsp; &nbsp; Recommendation system for news focusing on 4 matrices in result evaluation: diversity, coverage, serendipity, and dynamism

&nbsp; &nbsp; &nbsp; &nbsp; Diversity: Inverse of the simmlarity of recommended item. Based on similarity of features

&nbsp; &nbsp; &nbsp; &nbsp; Coverage: The proportion of recommended items over all items

&nbsp; &nbsp; &nbsp; &nbsp; Serendipity: Inverse of simmlarity of recommended item v.s. user history

&nbsp; &nbsp; &nbsp; &nbsp; Dynamism: The recency of timestamp for each recommended items

&nbsp; &nbsp; &nbsp; &nbsp; Item simmlarity is useful in the evaluation. Actually most of such matrices can be added as a loss function in the recommendation algorithm, which is not fully discussed in the paper

## Survey

1. [Deep Learning based Recommender System: A Survey and New Perspectives](https://arxiv.org/pdf/1707.07435.pdf)




