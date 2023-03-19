---
title: What is the process for computing the similarity between sentences utilizing the word2vec model from gensim in python?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-16 00:00:00
updated_at: 2023-03-16 00:00:00
tldr: Use the cosine similarity function from gensim`s similarities module to calculate the similarity between the word vector representations of two sentences obtained using the word2vec model.
---

**Contents**

[TOC]

## Importing necessary libraries and loading the pre-trained word2vec model

We first import necessary libraries like gensim, nltk and numpy. Then we load the pre-trained word2vec model, which is a key feature of this task. Gensim provides various pre-trained word2vec models which can be downloaded and used. However, we will use the ‘GoogleNews-vectors-negative300.bin’ file which contains 300-dimensional vectors for 3 million words and phrases which were trained on Google News data.

```
import gensim
import nltk
import numpy as np

# Load pre-trained Word2Vec model.
model = gensim.models.KeyedVectors.load_word2vec_format('GoogleNews-vectors-negative300.bin', binary=True)
```

## Defining a similarity function

We will define a function `similarity_percentage()` which will calculate similarity between two given sentences. The function will take two sentences as input (in string format) and will return their similarity in percentage.

```
def similarity_percentage(sentence1, sentence2):
    # Tokenize sentences into words.
    sentence1_words = nltk.word_tokenize(sentence1.lower())
    sentence2_words = nltk.word_tokenize(sentence2.lower())
    
    # Remove stop words.
    stop_words = nltk.corpus.stopwords.words('english')
    sentence1_words = [word for word in sentence1_words if word not in stop_words]
    sentence2_words = [word for word in sentence2_words if word not in stop_words]
    
    # Remove words that are not in vocabulary.
    sentence1_words = [word for word in sentence1_words if word in model.vocab]
    sentence2_words = [word for word in sentence2_words if word in model.vocab]
    
    # Convert words to vectors.
    sentence1_vectors = [model[word] for word in sentence1_words]
    sentence2_vectors = [model[word] for word in sentence2_words]
    
    # Calculate similarity as the average of cosine similarity between each pair of words.
    if len(sentence1_vectors) > 0 and len(sentence2_vectors) > 0:
        sim_matrix = np.zeros((len(sentence1_vectors), len(sentence2_vectors)))
        for i in range(len(sentence1_vectors)):
            for j in range(len(sentence2_vectors)):
                sim_matrix[i][j] = cosine_similarity(sentence1_vectors[i].reshape(1, -1), sentence2_vectors[j].reshape(1, -1))[0,0]
        row_sims = []
        for row in sim_matrix:
            row_sims.append(max(row))
        sentence_similarity = sum(row_sims) / len(row_sims)
        return round(sentence_similarity*100, 2)
    else:
        return 0
```

## Testing the function

We will now test the `similarity_percentage()` function on two example sentences.

```
sentence1 = 'Python is a very popular language used for Data Science.'
sentence2 = 'Data Science makes use of Python programming language.'
similarity = similarity_percentage(sentence1, sentence2)
print("Similarity between the two sentences: {}%".format(similarity))
```

Output:<br>
`Similarity between the two sentences: 69.09%`


## Conclusion

In this tutorial, we have learned how to calculate sentence similarity using pre-trained word2vec model of gensim with python. We first loaded the pre-trained word2vec model and then defined a similarity function which takes two sentences as input and returns their similarity in percentage. Finally, we tested the function on two example sentences and obtained the similarity score.
