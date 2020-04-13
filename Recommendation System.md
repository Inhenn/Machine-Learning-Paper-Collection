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


## Regression Based

1. [Pairwise Preference Regression for Cold-start Recommendation](http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.211.9762&rep=rep1&type=pdf)

&nbsp; &nbsp; &nbsp; &nbsp; Used normalized Discounted Cumulative Gain (𝑛𝐷𝐶𝐺) as evaluation matrix for ranking

&nbsp; &nbsp; &nbsp; &nbsp; Pairwise loss designed for multiple items recommended to the same user

&nbsp; &nbsp; &nbsp; &nbsp; Recommendation is evaluated in terms of the item ranking for a user in the case that each user needs a recommendation

&nbsp; &nbsp; &nbsp; &nbsp; Closed form solution

&nbsp; &nbsp; &nbsp; &nbsp; Idea in cold start testing: random select half user(or item) as new user(or item) to test model performance in cold 
&nbsp; &nbsp; &nbsp; &nbsp; start case





