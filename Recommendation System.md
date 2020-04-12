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


4. [Deep Tensor Factorization for Multi-Criteria Recommender Systems](https://ieeexplore.ieee.org/document/9005677)

&nbsp; &nbsp; &nbsp; &nbsp; Standard tensor factorization ==> 3 latent matrices  

&nbsp; &nbsp; &nbsp; &nbsp; Use stacked denoising autoencoder to get the latent matrix for user and item

&nbsp; &nbsp; &nbsp; &nbsp; Claim to handle sparse problem in tensor factorization by using autoencoder to reduce dimension





