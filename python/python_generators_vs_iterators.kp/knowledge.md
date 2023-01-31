---
title: What is the distinction between Python generators and iterators?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-01-30 00:00:00
updated_at: 2023-01-30 00:00:00
tldr: Generators are a type of iterator that produce items on demand, while iterators are objects that can be used to iterate over a sequence of items.
---

**Contents**

[TOC]

# Generators
Generators are a type of iterator that can be used to generate a sequence of values. They are created by defining a function that uses the yield keyword to return a value. Generators are used to create iterators, but with a few key differences.

# Iterators
Iterators are objects that can be used to iterate over a sequence of values. They are created by calling the iter() function on an object that supports iteration. Iterators can be used to loop over a sequence of values, but they cannot be used to generate new values.

# Key Differences
- Generators can be used to generate a sequence of values, while iterators can only be used to loop over a sequence of values. 
- Generators are created using the yield keyword, while iterators are created using the iter() function. 
- Generators keep track of their internal state, while iterators do not.
