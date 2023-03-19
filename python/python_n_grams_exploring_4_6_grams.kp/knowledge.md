---
title: What are the four, five, and six gram n-grams in python?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-11 00:00:00
updated_at: 2023-03-11 00:00:00
tldr: n-grams in Python are a way to split text into groups of n consecutive words or characters, with common values being four, five, and six grams.
---

**Contents**

[TOC]

Section 1: What are n-grams?

An n-gram is a contiguous sequence of n items from a given text, where "item" can be a word, character, or any other meaningful unit of text. N-grams are commonly used in natural language processing, text mining, and machine learning, among other fields. The value of n determines the length of the n-grams: for example, a 2-gram (or a bigram) for the word "hello" would be "he" and "el," while a 3-gram (or a trigram) would be "hel," "ell," and "llo."

Section 2: How to generate n-grams in Python?

In Python, n-grams can be generated using the NLTK library or the built-in zip function. The following code shows how to generate four, five, and six grams from a given list of words using the zip method:

```python
words = ["hello", "world", "how", "are", "you", "doing", "today"]
four_grams = zip(words, words[1:], words[2:], words[3:])
five_grams = zip(words, words[1:], words[2:], words[3:], words[4:])
six_grams = zip(words, words[1:], words[2:], words[3:], words[4:], words[5:])
```

This will create three lists of tuples, where each tuple contains four, five, or six consecutive words from the original list.

Alternatively, we can use the NLTK library to generate n-grams, as shown below:

```python
from nltk import ngrams

words = ["hello", "world", "how", "are", "you", "doing", "today"]
four_grams = ngrams(words, 4)
five_grams = ngrams(words, 5)
six_grams = ngrams(words, 6)
```

This will create three n-gram generator objects that can be iterated over to get all the four, five, or six grams from the original list.

Section 3: What are some applications of n-grams?

N-grams have various applications in natural language processing, text mining, and machine learning, including:

- Language modeling: N-grams are commonly used to represent the structure of language and estimate the probability of a word given its context (i.e., the previous n-1 words). This is useful in tasks such as speech recognition, machine translation, and text generation.

- Text classification: N-grams can be used as features in machine learning models for text classification tasks, such as sentiment analysis, spam filtering, and document categorization. By representing text as a bag of n-grams (i.e., a set of all the n-grams in the text), we can capture the relevant information about the text without relying on explicit domain knowledge or hand-crafted features.

- Information retrieval: N-grams can be used to index and search through large collections of documents. By generating all the n-grams in the documents and storing them in a database, we can quickly retrieve relevant documents based on a user's query.

Section 4: Conclusion

N-grams are a powerful and versatile tool for analyzing and processing text data in various applications. By generating all the contiguous sequences of n items in a text, we can capture the structure and meaning of the text and use it for tasks such as language modeling, text classification, and information retrieval. Python provides several libraries and methods for generating n-grams, making it easy to incorporate them into your text analysis pipeline.
