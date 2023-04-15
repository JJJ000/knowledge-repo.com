---
title: What are the different pos tags that nltk can generate?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: There are 36 possible POS tags in NLTK, including noun, verb, adjective, adverb, pronoun, preposition, conjunction, interjection, and others.
---

**Contents**

[TOC]

## Part-of-speech tagging with NLTK in Python

One of the key features of NLTK is its ability to tag words with their part of speech (POS) in a given sentence. The following sections describe the various POS tags that are available in NLTK.

### The Penn Treebank POS tags

NLTK provides one of the most popular POS tagging schemes in the Penn Treebank POS tags. There are 36 tags in this scheme, which include:

- **CC**: coordinating conjunction
- **CD**: cardinal number
- **DT**: determiner
- **EX**: existential there
- **IN**: preposition/subordinating conjunction
- **JJ**: adjective
- **JJR**: adjective, comparative
- **JJS**: adjective, superlative
- **LS**: list marker
- **MD**: modal
- **NN**: noun, singular or mass
- **NNS**: noun plural
- **NNP**: proper noun, singular
- **NNPS**: proper noun, plural
- **PDT**: predeterminer
- **POS**: possessive ending
- **PRP**: personal pronoun
- **PRP\$**: possessive pronoun
- **RB**: adverb
- **RBR**: adverb, comparative
- **RBS**: adverb, superlative
- **RP**: particle
- **SYM**: symbol
- **TO**: to
- **UH**: interjection
- **VB**: verb, base form
- **VBD**: verb, past tense
- **VBG**: verb, gerund/present participle
- **VBN**: verb, past participle
- **VBP**: verb, non-3rd person singular present
- **VBZ**: verb, 3rd person singular present
- **WDT**: wh-determiner
- **WP**: wh-pronoun
- **WP\$**: possessive wh-pronoun
- **WRB**: wh-adverb

### Other POS tagging schemes

In addition to the Penn Treebank POS tags, NLTK also provides support for other tagging schemes, such as:

- **Brown Corpus tagset**: this is based on the Brown Corpus, which is a collection of text samples from a variety of genres. There are 87 tags in this scheme.
- **Lancaster Corpus tagset**: this is based on the Lancaster Corpus, which is a version of the Brown Corpus that has been reduced to only about 10% of its original size. There are 14 tags in this scheme.
- **Others**: NLTK also provides support for other custom tagging schemes that can be defined as required.

### Using POS tags in NLTK

To use POS tags in NLTK, you will need to first tokenize a sentence using the NLTK tokenizer. Once you have tokenized the sentence, you can use the `pos_tag` function to obtain the POS tags for each token in the sentence. The following code snippet illustrates this process:

```python
import nltk
nltk.download('punkt')

sentence = "The quick brown fox jumped over the lazy dog"
tokens = nltk.word_tokenize(sentence)
tags = nltk.pos_tag(tokens)
print(tags)
```

output:
```
[('The', 'DT'), ('quick', 'JJ'), ('brown', 'NN'), ('fox', 'NN'), ('jumped', 'VBD'), ('over', 'IN'), ('the', 'DT'), ('lazy', 'JJ'), ('dog', 'NN')]
```

This will output a list of tuples, where each tuple contains the token and its corresponding POS tag. In the example above, you can see that the word "fox" has been tagged as an NN, which stands for "noun, singular or mass".
