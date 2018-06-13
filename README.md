# Overview and benchmark of traditional and deep learning models in text classification

original post: https://ahmedbesbes.com/overview-and-benchmark-of-traditional-and-deep-learning-models-in-text-classification.html

This article is an extension of a previous one I wrote when I was experimenting sentiment analysis on twitter data. Back in the time, I explored a simple model: a two-layer feed-forward neural network trained on keras. The input tweets were represented as document vectors resulting from a weighted average of the embeddings of the words composing the tweet.

The embedding I used was a word2vec model I trained from scratch on the corpus using gensim. The task was a binary classification and I was able with this setting to achieve 79% accuracy.

The goal of this post is to explore other NLP models trained on the same dataset and then benchmark their respective performance on a given test set.

We'll go through different models: from simple ones relying on a bag-of-word representation to a heavy machinery deploying convolutional/recurrent networks: We'll see if we'll score more than 79% accuracy!


----------

Here are the models that have been tested:

- Logistic regression with word ngrams
- Logistic regression with character ngrams
- Logistic regression with word and character ngrams
- Recurrent neural network (bidirectional GRU) without pre-trained embeddings
- Recurrent neural network (bidirectional GRU) with GloVe pre-trained embeddings
- Multi channel Convolutional Neural Network
- RNN (Bidirectional GRU) + CNN model
