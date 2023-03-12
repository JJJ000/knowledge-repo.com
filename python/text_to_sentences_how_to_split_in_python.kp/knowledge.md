---
title: What is the method to divide a text into individual sentences?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-12 00:00:00
updated_at: 2023-03-12 00:00:00
tldr: Use the `nltk` library`s `sent\_tokenize` function.
---

**Contents**

[TOC]

## Method 1: Using the NLTK library

[NLTK](https://www.nltk.org/) is a popular Python library used for natural language processing. It contains various functionalities to preprocess and manipulate textual data, including splitting texts into sentences.

1. Install NLTK using `pip install nltk`.
2. Import the `sent_tokenize` function from the NLTK library.
3. Pass the text that you want to split into sentences to the `sent_tokenize` function.
4. `sent_tokenize` returns a list of sentences.

```python
import nltk
nltk.download('punkt') # necessary only the first time

from nltk.tokenize import sent_tokenize

text = "This is a sentence. This is another sentence. This isn't a sentence."

sentences = sent_tokenize(text)

print(sentences)
```

Output:
```python
['This is a sentence.', 'This is another sentence.', "This isn't a sentence."]
```


## Method 2: Using the spaCy library

[spaCy](https://spacy.io/) is an open-source natural language processing library that provides various functionalities for processing textual data. It also includes functionalities to split texts into sentences.

1. Install spaCy using `pip install spacy`.
2. Download the language model that you want to use. For example, if you want to use the English language model, run `python -m spacy download en`.
3. Import the `sentencizer` class from the `spacy.lang.<language>` package.
4. Load the language model using `spacy.load('<language>')`.
5. Pass the text that you want to split into sentences to the language model using the `.pipe()` method.
6. Access the `.sents` attribute of the returned Doc object to get a list of sentences.

```python
import spacy

nlp = spacy.load('en_core_web_sm')

text = "This is a sentence. This is another sentence. This isn't a sentence."

doc = nlp(text)

sentences = list(doc.sents)

print(sentences)
```

Output:
```python
[This is a sentence., This is another sentence., This isn't a sentence.]
```


## Method 3: Using regular expressions

It is also possible to split texts into sentences using regular expressions. However, this approach might not be as accurate as the previous two methods and might require more fine-tuning of the regular expression.

1. Import the `re` module.
2. Define a regular expression pattern that matches the end-of-sentence punctuation (e.g., period, question mark, exclamation mark).
3. Use the `re.split()` method to split the text into sentences using the regular expression pattern as the delimiter.

```python
import re

text = "This is a sentence. This is another sentence? This isn't a sentence!"

sentence_pattern = r'(?<=[^A-Z].[.?]) +(?=[A-Z])'

sentences = re.split(sentence_pattern, text)

print(sentences)
```

Output:
```python
['This is a sentence.', 'This is another sentence?', "This isn't a sentence!"]
```
