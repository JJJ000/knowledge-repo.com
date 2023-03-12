---
title: What is the purpose of the tf.nn.embedding_lookup function?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-12 00:00:00
updated_at: 2023-03-12 00:00:00
tldr: The tf.nn.embedding\_lookup function is used to lookup word embeddings for a given list of indices.
---

**Contents**

[TOC]

# tf.nn.embedding_lookup function

The `tf.nn.embedding_lookup` function is a useful tool for obtaining the word embedding vectors of the words in a given text corpus. It is frequently used in natural language processing (NLP) tasks such as text classification, sentiment analysis, and word prediction. 

## Input Requirements

The function takes in two inputs:

1. A tensor of word embeddings of size [vocab_size, embedding_dim], where `vocab_size` is the number of unique words in the corpus, and `embedding_dim` is the size of the word embedding vector. This tensor contains the word embeddings learned during training using techniques such as Word2Vec or GloVe.
2. A tensor of indices representing the words to be looked up, and can be of any shape [batch_size, num_steps]. If an index in this tensor is out of bounds, the function raises an error.

## Functionality 

The function returns a tensor of size `[batch_size, num_steps, embedding_dim]`, where each element of the tensor represents the word embedding of a single word in the input tensor. Essentially, the function maps each index in the input tensor to its corresponding word embedding in the embedding tensor.

In summary, `tf.nn.embedding_lookup` is a powerful tool for obtaining the word embeddings of words in a given text corpus, and can be used in a range of NLP tasks.
