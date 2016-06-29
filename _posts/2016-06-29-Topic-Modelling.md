---
layout: post
title:  "A brief introduction to NLP Topic Modelling"
date:   2016-06-29 21:00:26 +0000
categories: NLP
author: atti
---

### A brief introduction to NLP Topic Modelling

What if you wanted to categorize a large number of documents automatically. Maybe there are hidden (latent) features which can be used to find correlations between documents. Which features should be used for this exercise, the title, the author the body of the document?

A part of natural language processing (NLP) focuses on categorizing/classifying documents this is achieved using unsupervised statistical learning techniques. Splitting documents into categories is nice but what if you could also name this categories automatically this is where Topic Modelling can be used. This technique can also be used to generate tags for documents.

First you have to do some feature engineering this usually involves tokenising the documents and then building vectors so you can compare them. The tokens can be individual words or groups of words (n-grams). After the tokens have been prepared the next step is to find a common denominator based on which the documents can be compared this usually involves building a vector. For text this can be a bag-of-words vector or something else that you have come up with.

The next step is to run this through some classification algorithm. If we use a topic modelling algorithm we get a nice distribution of relevant words (topics) for each class of documents. A good technique for topic modelling is Latent Dirichlet Allocation (LDA) and there are several libraries that implement it. LDA will give us a list of topics for each document class and will also give us a probability distribution which will tell us how likely it is that a given document is in a topic. We can then decide what is the threshold for accepting a document within a topic. 

There are some caveats some caveats related to the inputs for LDA and it's performance scalability. It's very resource intensive although there are some good packages out there that implement online LDA, which essentially means that the data is streamed to the classifier. This approach is a more scalable.

### Resources for Topic Modelling and LDA

#### Videos
* [LDA Topic Modelling](https://www.youtube.com/watch?v=ePUAZ8RG-3w)
* [Understanding Probabilistic Topic Models - LDA - Pydata NYC 2015](https://www.youtube.com/watch?v=_R66X_udxZQ)

#### Papers / Blogs
Hannah wallach ideas for lda
Hierarchical LDA process, conda/github

* David Blei - [Probabilistic topic models](https://www.cs.princeton.edu/~blei/papers/Blei2011.pdf)
* Edwin Chen - [Introduction to LDA](http://blog.echen.me/2011/08/22/introduction-to-latent-dirichlet-allocation/)
* Hannah Wallach - [Ideas for LDA](http://dirichlet.net/pdf/hannah14topic.pdf)
* More Publications (Here)[http://dirichlet.net/publications/]

#### Libraries

* [Gensim](http://radimrehurek.com/gensim/)
* [Sklearn LatentDirichletAllocation](http://scikit-learn.org/stable/auto_examples/applications/topics_extraction_with_nmf_lda.html#example-applications-topics-extraction-with-nmf-lda-py)
* Lda package by Allen Riddel - [LDA](https://ariddell.org/wustl2012.html)
* Ben Mabey visualisation - [PyLdaVis](https://github.com/bmabey/pyLDAvis)






