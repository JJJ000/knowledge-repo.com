---
title: What is the method for determining the likeness of two textual documents?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: One way to compute the similarity between two text documents in Python is to use the cosine similarity measure.
---

**Contents**

[TOC]

Section 1: Text Preprocessing
To compute the similarity between two text documents, we need to first preprocess the text data. Here are some common preprocessing steps we can take:

1. Convert all text to lowercase
2. Remove punctuation and special characters
3. Remove stop words (common words like “the”, “and”, “a”)
4. Stemming or Lemmatization (reducing words to their root form)

We can perform these steps using various libraries in Python such as NLTK, spaCy, and Scikit-learn.

Section 2: Vectorizing the Text
After preprocessing, we need to represent our text documents as numerical vectors so that we can apply mathematical operations on them to compute similarity. Vectorizing can be done using the following techniques:

1. Count Vectorization: Here, we convert each document into a vector of word counts, where each element of the vector represents the frequency of a particular word in the document.
2. TF-IDF Vectorization: Here, we convert each document into a vector of TF-IDF scores, where each element of the vector represents the importance of a particular word in the document.

Scikit-learn’s CountVectorizer and TfidfVectorizer classes can be used to perform count and TF-IDF vectorization.

Section 3: Computing Document Similarity
After vectorizing the text, we can compute the similarity between two documents using various distance/similarity metrics such as:

1. Euclidean Distance: It calculates the root of the sum of the squared differences between the elements of the two vectors being compared.
2. Manhattan Distance: Also known as the “city-block” distance, it calculates the sum of the absolute differences between the elements of the two vectors being compared.
3. Cosine Similarity: It calculates the cosine of the angle between the two vectors being compared.

Scikit-learn’s pairwise_distances function can be used to compute these metrics.

Section 4: Example Code
Here’s an example code snippet that demonstrates the steps mentioned above:

```
import nltk
from nltk.tokenize import word_tokenize
from nltk.corpus import stopwords
from nltk.stem.porter import PorterStemmer
from sklearn.feature_extraction.text import TfidfVectorizer
from sklearn.metrics.pairwise import cosine_similarity

# Preprocessing
def preprocess_text(text):
    text = text.lower()
    tokens = word_tokenize(text)
    stop_words = set(stopwords.words('english'))
    tokens = [token for token in tokens if token not in stop_words]
    stemmer = PorterStemmer()
    tokens = [stemmer.stem(token) for token in tokens]
    return " ".join(tokens)

# Vectorizing
corpus = ["The quick brown fox jumps over the lazy dog.",
          "A quick brown dog jumps over the lazy fox.", 
          "A quick brown fox jumps over the lazy dog."]

vectorizer = TfidfVectorizer()
X = vectorizer.fit_transform([preprocess_text(text) for text in corpus])

# Computing Similarity
similarity_matrix = cosine_similarity(X)

print(similarity_matrix)
```

In the above code, we first perform preprocessing on the input corpus using NLTK library functions. Then, we use Scikit-learn’s TfidfVectorizer to vectorize the text. Finally, we use Scikit-learn’s cosine_similarity function to compute the similarity between the documents. The output is a similarity matrix where each element (i, j) represents the similarity between the i-th and j-th documents in the corpus.
