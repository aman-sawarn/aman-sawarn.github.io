---
layout: post
title:  "LDA for the People"
date:   2019-08-04
mathjax: true
---

# LDA for the People

Latent Dirichlet Allocation (LDA) is a popular computational technique in natural language processing, computational science, and the digital humanities. LDA automatically learns a set of **topics** for an input set of documents, allowing for quick data exploration and analysis. The magical part is that LDA does not require any labeled training data; all you need are a set of texts, and LDA will give you topics.

For example, if we had a set of newspaper articles, we might expect some topics like this:

| Topic 1 | baseball basketball score run player football |
|---------|-----------------------------------------------|
| Topic 2 |                                               |


LDA is frequently used because of the highly interpretable topics it produces and the easy-to-use packages available (e.g. [MALLET](http://mallet.cs.umass.edu/)). However, understanding how LDA actually works can be challenging. The math can seem intimidating, and most available teaching resources are either too high level, providing only the intuitions, or too low level, stuck in the math without motivating why each step is necessary.

The good news is that you can benefit from my struggles. I've tried to write a tutorial that combines the intuitions and the math and is concise but doesn't leave anything important out. 

## The Generative Process

LDA is a **generative** model. This means that the model makes some extremely simplifying assumptions about how the training documents were **generated**. The data was not actually generated this way, but since it is too difficult to model the real-world process, the model instead makes a set of simplifying **assumptions**.

<!-- Since actually modeling how humans write documents is very hard, LDA will just pretend that instead of humans writing the documents, the documents were **generated** by a simple, automatic process.  -->

<!-- The **generative process** describes how the model **imagines** that our training data has been generated.  -->

While you and I might think of a topic as a theme or subject, LDA thinks of a **topic** as a probability distribution over words. Similarly, LDA thinks of each **document** as some distribution over topics. Obviously, this isn't how the documents were actually generated, but this is what the model assumes.

For example:

|         | Word 1 | Word 2 | Word 3 | Word 4 | Word 5 | ... |
|---------|--------|--------|--------|--------|--------| ----|
| Topic 1 | 0.01   | 0.02   | 0.3    | 0.005  | 0.07   | ... |
|---------|--------------------------------------------|-----|

LDA's other assumptions include the following.

* **Bag of Words Assumption**: each word is generated independently of all other words. 
* **Mixture Assumption**: each document is generated from a mixture of topics.
* **Sparsity Assumption**: only one or two topics dominate in each document.

The generative process itself looks like this:

1. To generate a new document \\(d\\):
    1. Randomly choose \\(\theta_{d}\\), a distribution over topics for the current document \\(d\\).

    2. To generate each word \\(w\\) in document \\(d\\):
        1. Randomly choose a topic \\(k\\) from \\(\theta_{d}\\), the topic distribution for the current document \\(d\\).
        2. Randomly choose a word \\(w\\) from \\(\phi_{k}\\), the distribution over all words for the chosen topic \\(k\\).



In other words, we are trying to model the probability of the observed data given some assumptions about how that data was generated. This generative process is described by the following joint distribution:

$$ p(w,k,\theta,\phi|\alpha,\beta) = \prod_{k=1}^{K}p(\phi_{k}|\beta) \prod_{d=1}^{D} \Big[ p(\theta_{d}|\alpha) \prod_{n=1}^{N}p(k_{k,n}|\theta_{d})p(w_{d,n}|k_{d,n},\theta) \Big] $$

where

* \\(K\\) is the number of topics
* \\(D\\) is the number of documents in the corpus
* \\(V\\)  is the number of unique words in the corpus
* \\(N\\) is the number of words in document \\(d\\)
* \\(w_{d,n}\\) is the \\(n\\)th word in document \\(d\\) (this is our observation)
* \\(k\\) is the topic assignment for the \\(n\\)th word in document \\(d\\)
* \\(\theta_{d}\\) is the topic distribution for document \\(d\\) (it is a vector of length \\(K\\)
* \\(\phi_{k}\\) is the word distribution for topic \\(k\\) (it is a vector of length \\(V\\)
* \\(\alpha\\) is the Dirichlet distribution parameter for \\(\theta\\) (it is a distribution over distributions)
* \\(\beta\\) is the Dirichlet distribution parameter for \\(\phi\\) (it is a distribution over distributions)

In the above equation, we can see the bag of words assumption when \\(p(w_{d,n})\\) depends only on \\(k_{d,n}\\) and \\(\theta\\) and not on any other \\(w\\). We can see the sparsity assumption in the dependence of \\(\phi\\) and \\(\theta\\) on the \\(\alpha\\) and \\(\beta\\) Dirichlet priors. Finally, we can see the mixture assumption 

One way to think about this equation is to imagine it as a series of *for* loops. First, for every topic \\(k\\), we calculate the probability of that topic's distribution over the words in the vocabulary, \\(\phi_{k}\\). ***insert pseudo-code?***



## The Posterior Distribution

In the previous section, we learned that the joint distribution is how the model assumes that documents are created. In this section, let's consider reality, where we're training LDA with a dataset. 

We are given a corpus of documents which contain words \\(w\\), and we want to find \\(\phi\\), \\(\theta\\), and \\(k\\). Therefore, we need to calculate the conditional probability, \\(p(\phi,\theta,k\|w)\\).

Conditional probabilities can be rewritten according to the equation ***. Therefore, we can rewrite \\(p(\phi,\theta,k\|w)\\) as 

$$ p(\phi,\theta,k|w) = \frac{p(\phi,\theta,k,w)}{p(w)} $$

This is known as the posterior distribution. Posterior because % Xanda: unfinished?

That is, given an observed word, what is the probability of a certain topic, distribution over topics, and distribution over words?

Unfortunately, we cannot solve this equation for all possible models---there are too many of them! Therefore, we will need to find a different learning method. 


## Gibbs Sampling


## Differences

Compare to BERT, LSA, embeddings, clustering


## Tricks of the Trade

Setting parameters, choosing number of topics, evaluation

- Lots of duplicate documents can result in topics that look very similar to each other.
- To make your topics more interpretable, you can remove stopwords either before or after training (ref Xanda)

## Favorite Resources

* [Introduction to Probabilistic Topic Models](https://www.semanticscholar.org/paper/Introduction-to-Probabilistic-Topic-Models-Blei/5f1038ad42ed8a4428e395c96d57f83d201ef3b3) by David Blei + [slides](https://pdfs.semanticscholar.org/01f3/290d6f3dee5978a53d9d2362f44daebc4008.pdf)
* [Probabilistic Topic Models](https://www.semanticscholar.org/paper/Probabilistic-Topic-Models-Erlbaum-Steyvers/418c7e1e2d9cd5695ddbe9898ed3852b565faefc) by Mark Steyvers and Tom Griffiths
* [Latent Dirichlet Allocation: Toward a Deeper Understanding](https://www.semanticscholar.org/paper/Latent-Dirichlet-Allocation%3A-Towards-a-Deeper-Unde-Reed/321478fa5adf3f6a4fe373f502b88d8cc21c853d) by Colorado Reed
* [Latent Dirichlet Allocation](http://www.utdallas.edu/~nrr150130/cs6375/2015fa/lects/Lecture_20_LDA.pdf) by Nicholas Ruozzi
* [Introduction to Latent Dirichlet Allocation](http://blog.echen.me/2011/08/22/introduction-to-latent-dirichlet-allocation/) by Edwin Chen  