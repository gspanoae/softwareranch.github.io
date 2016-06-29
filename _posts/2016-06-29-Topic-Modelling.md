---
layout: post
title:  "A brief introduction to Topic Modelling"
date:   2016-06-29 20:00:26 +0000
categories: nlp
author: atti
---

### The business case

What if you have a large body of documents and these are stored haphazardly on your network. They started out with a well defined structure but grew out of control over time. 
Could you categorize these documents automatically. Are there any hidden (latent) features which can be used to find correlations between documents. 
How can you correlate similar documents, which features should be used for this exercise: the title, the author the body of the document?
Even if you manage to group similar documents into the same category could you label the categories automatically? 

If your in this situation then there might be a solution, this is were the tools and techniques of Natural Language Processing could help you.

### The solution

A part of natural language processing (NLP) focuses on categorizing/classifying documents automatically, this is achieved using unsupervised statistical learning techniques. 
Splitting documents into categories is nice but what if you could also name the categories automatically, Topic Modelling techniques do this for you and they can also be used to generate tags (metadata) for documents.

First you have to do some feature engineering this usually involves tokenising the documents and then building vectors so you can compare them. 
The tokens can be individual words or groups of words (n-grams). After the tokens have been prepared the next step is to find a common denominator based on which the documents can be compared this usually involves building a vector.
For text this can be a bag-of-words vector or something else that you have come up with.

The next step is to run this through some classification algorithm like K-Means or LDA. If we use a topic modelling algorithm we get a nice distribution of relevant words (topics) for each class of documents. 
A good technique for topic modelling is Latent Dirichlet Allocation (LDA) and there are several libraries that implement it. 
LDA will give us a list of topics for each document class and will also give us a probability distribution which will tell us how likely it is that a given document is in a topic. 
We can then decide what is the threshold for accepting a document within a topic. It seems like black magic doesn't it, but under the hood it's all statistics and maths and some domain knowledge to get the features right.

There are some caveats however related to the inputs for LDA and it's performance/scalability. 
It's very resource intensive although there are some good packages out there that implement online LDA, which essentially means that the data is streamed to the classifier, which makes it scalable.
The inputs are also tricky to get right, you will probably spend some time getting the features ready and you also have to decide on how many categories you want. 
It will be an iterative process until you find the sweet spot which gives you the best categories and topics for your documents.

See below for more details about how LDA works and how to implement it.

### Resources for Topic Modelling and LDA

#### Videos

* [LDA Topic Modelling](https://www.youtube.com/watch?v=ePUAZ8RG-3w)
* [Understanding Probabilistic Topic Models - LDA - Pydata NYC 2015](https://www.youtube.com/watch?v=_R66X_udxZQ)

#### Papers / Blogs

* David Blei - [Probabilistic topic models](https://www.cs.princeton.edu/~blei/papers/Blei2011.pdf)
* Edwin Chen - [Introduction to LDA](http://blog.echen.me/2011/08/22/introduction-to-latent-dirichlet-allocation/)
* Hannah Wallach - [Ideas for LDA](http://dirichlet.net/pdf/hannah14topic.pdf)
* Visualising LDA - [NLP Stanford](http://nlp.stanford.edu/events/illvi2014/papers/sievert-illvi2014.pdf)
* Latent Dirilecht allocation (LDA) paper [AI Stanford](http://ai.stanford.edu/~ang/papers/jair03-lda.pdf)
* Gensim topic modelling [tutorials](http://radimrehurek.com/gensim/tutorial.html)
* [LDA with Python](https://rstudio-pubs-static.s3.amazonaws.com/79360_850b2a69980c4488b1db95987a24867a.html)
* Topic Modelling and Text Analysis for the Humanities [DARIAH-DE](https://de.dariah.eu/tatom/)
* Allen Riddel's [Blog](https://ariddell.org/wustl2012.html)
* .. and many more here (Here)[http://dirichlet.net/publications/]

#### Libraries

* [Gensim](http://radimrehurek.com/gensim/)
* [Sklearn LatentDirichletAllocation](http://scikit-learn.org/stable/auto_examples/applications/topics_extraction_with_nmf_lda.html#example-applications-topics-extraction-with-nmf-lda-py)
* Lda package by Allen Riddel - [LDA](https://github.com/ariddell/lda)
* Ben Mabey visualisation - [PyLdaVis](https://github.com/bmabey/pyLDAvis)

Hope you enjoyed this post, there is a lot to take in with this approach. Have you come across this approach, what was your experience with it, leave us your thoughts below.




