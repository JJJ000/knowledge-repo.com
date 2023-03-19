---
title: What is the method for identifying the language in a document?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-11 00:00:00
updated_at: 2023-03-11 00:00:00
tldr: Using the langdetect library in Python, you can determine the language of a piece of text by analyzing its character frequency and comparing it to known language models.
---

**Contents**

[TOC]

## Introduction
Determining the language of a piece of text is important in various natural language processing tasks, such as sentiment analysis, machine translation, and named entity recognition. In Python, there are several libraries and tools available for language detection. This tutorial will cover two popular methods for language detection: 
1. Using the langid library 
2. Using the TextBlob library 


## Using the langid library
The langid library is a simple and efficient library for language identification. It works by classifying text based on character n-grams and language models. Here's how to use it:

1. Install the langid library using pip:
```
!pip install langid
```

2. Import the langid module:
```python
import langid
```

3. Use the `langid.classify` method to detect the language of your text. The method returns a tuple consisting of a two-letter language code and a float representing the probability of the classification. For example:
```python
text = "Hola, ¿cómo estás? Me llamo Maria."
lang, prob = langid.classify(text)

print(lang, prob)
# Output: es 0.9999985694880233
```
In this example, the text is in Spanish, and langid returns the two-letter language code "es" and a high probability of 0.9999985694880233.

4. You can also use the `rank` parameter to get a list of language codes and their corresponding probabilities. For example:
```python
text = "How are you? My name is John."

langs = langid.classify(text, rank=5)

for lang, prob in langs:
    print(lang, prob)
# Output:
# en 0.9999999999343148
# cy 5.836030905465938e-11
# ga 5.3442432146306976e-11
# gd 1.4276585676394305e-11
# to 8.23772745857629e-13
```
In this example, the text is in English, and the `rank=5` parameter returns the five most probable language codes for the text and their corresponding probabilities. As expected, "en" (English) has the highest probability.



## Using the TextBlob library
The TextBlob library is a popular library for natural language processing tasks, such as sentiment analysis and part-of-speech tagging. It also has built-in language detection capabilities. Here's how to use it:

1. Install the TextBlob library using pip:
```python
!pip install textblob
```

2. Import the TextBlob module:
```python
from textblob import TextBlob
```

3. Create a TextBlob object with your text, and use the `detect_language` method to detect the language:
```python
text = "Bonjour, comment ça va? Je m'appelle Pierre."
blob = TextBlob(text)

lang = blob.detect_language()
print(lang)
# Output: fr
```
In this example, the text is in French, and TextBlob returns the two-letter language code "fr".

4. You can also get the language name and confidence score using the `translate` method:
```python
lang_name, confidence = blob.translate(to='en').detect_language()
print(lang_name, confidence)
# Output: French 1.0
```
In this example, the `translate` method is used to translate the text to English, and then detect the language. The `detect_language` method returns "French" as the language name with a confidence score of 1.0.



## Conclusion
In this tutorial, we've covered two popular methods for language detection in Python. The langid library is a simple and efficient library that uses character n-grams and language models to classify text. The TextBlob library is a more comprehensive library for natural language processing tasks, and has built-in language detection capabilities. Both libraries are easy to use and produce accurate results.
