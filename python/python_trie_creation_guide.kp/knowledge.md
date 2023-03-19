---
title: Could you provide instructions on building a trie data structure using python?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-12 00:00:00
updated_at: 2023-03-12 00:00:00
tldr: To create a trie in Python, one can define a TrieNode class and implement methods for insertion and searching.
---

**Contents**

[TOC]

## Introduction 

When working with data, a trie data structure can be incredibly useful for efficient lookups, especially for strings. Essentially, a trie is a tree-like data structure that stores keys (usually strings), where each node represents a prefix or complete string. This makes it extremely fast for searching for keys or values that start with certain strings.

In this guide, we'll go over the steps to create a trie in Python using a dictionary to represent the tree structure. 

## Creating the class 

First, we'll start by creating a trie class that will hold all the necessary methods for adding, searching and deleting nodes from the trie. 

```python
class Trie:
    def __init__(self):
        self.root = {}

    def add_word(self, word):
        # TODO: implement method

    def search_word(self, word):
        # TODO: implement method

    def delete_word(self, word):
        # TODO: implement method
```

We start by defining the `__init__` method that initializes the `root` node as an empty dictionary. We also create three other methods: `add_word`, `search_word`, and `delete_word`. We'll fill these in later.

## Adding words to the trie 

To add words to the trie, we'll iterate over each character in the word and create a new sub-dictionary for each character that doesn't already exist. If the character already exists, we'll simply move on to the next character. 

```python
class Trie:
    def __init__(self):
        self.root = {}

    def add_word(self, word):
        current_node = self.root

        for char in word:
            if char not in current_node:
                current_node[char] = {}
            current_node = current_node[char]

        # Indicate end of word by adding empty dictionary to last node
        current_node[""] = {}

    def search_word(self, word):
        # TODO: implement method

    def delete_word(self, word):
        # TODO: implement method
```

In the `add_word` method, we keep track of the current node in the `current_node` variable. We then iterate over each character in the word and check if it exists in the current node. If it doesn't, we create a new sub-dictionary for that character. We also update `current_node` to point to the newly created dictionary. 

At the end, we add an empty sub-dictionary to the final node to indicate that the word has ended there. This will be used later for searching and deleting words.

## Searching for words in the trie 

The `search_word` method will take a string as input and return `True` if the string is found in the trie and `False` otherwise. This can be done by iterating over each character in the string and checking if it exists in the current node. If it does, move on to the next character and the next node. If the final character has a sub-dictionary with an empty value, that means the full word exists in the trie. 

```python
class Trie:
    def __init__(self):
        self.root = {}

    def add_word(self, word):
        current_node = self.root

        for char in word:
            if char not in current_node:
                current_node[char] = {}
            current_node = current_node[char]

        # Indicate end of word by adding empty dictionary to last node
        current_node[""] = {}

    def search_word(self, word):
        current_node = self.root

        for char in word:
            if char not in current_node:
                return False
            current_node = current_node[char]

        # If last node has empty dictionary, word has been found
        return "" in current_node

    def delete_word(self, word):
        # TODO: implement method
```

## Deleting words from the trie 

The `delete_word` method will take a string as input and remove it from the trie if it exists. This can be done by iterating over each character in the string and checking if it exists in the current node. Once the final character is reached, we check if the current node has an empty sub-dictionary. If it does, we remove it from the trie by setting the value of the final node to `None`. We then iterate backwards through the string and remove any nodes that are no longer necessary (i.e. that aren't being used by any other words in the trie). 

```python
class Trie:
    def __init__(self):
        self.root = {}

    def add_word(self, word):
        current_node = self.root

        for char in word:
            if char not in current_node:
                current_node[char] = {}
            current_node = current_node[char]

        # Indicate end of word by adding empty dictionary to last node
        current_node[""] = {}

    def search_word(self, word):
        current_node = self.root

        for char in word:
            if char not in current_node:
                return False
            current_node = current_node[char]

        # If last node has empty dictionary, word has been found
        return "" in current_node

    def delete_word(self, word):
        current_node = self.root
        nodes_to_delete = []

        # Iterate over each character in word
        for char in word:
            if char not in current_node:
                return
            nodes_to_delete.append((char, current_node))
            current_node = current_node[char]

        # If last node has empty dictionary, delete it
        if "" in current_node:
            current_node[""] = None

            # Iterate backwards through string and remove unnecessary nodes
            for char, node in reversed(nodes_to_delete):
                if len(node[char]) == 0:
                    del node[char]
                else:
                    break
``` 

In the `delete_word` method, we keep track of all the nodes that we have traversed through by appending each character and the current node to the `nodes_to_delete` list. Once we've iterated over all the characters, we check if the final node has an empty sub-dictionary. If it does, this means that the word exists in the trie and can be removed. We do this by setting the value of the sub-dictionary to `None`.

We then iterate backwards through the string using the `nodes_to_delete` list and check if each node is being used by any other words in the trie. If it isn't, we remove it by calling the `del` method on the parent node's dictionary. 

## Conclusion 

In this guide, we've gone over the steps to create a trie in Python using a dictionary to represent the tree structure. We've also added methods to add, search and delete words from the trie. While this implementation is not the most optimized, it should provide a good understanding of how a trie works and can be a good place to start for more complex applications.
