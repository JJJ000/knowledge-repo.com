---
title: What is the definition of enumerate()?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: Enumerate() is a built-in function in Python that allows for looping through an iterable and keeping track of the index of each item.
---

**Contents**

[TOC]

# Definition
Enumerate() is a built-in Python function that allows you to loop over a sequence and return both the index and the value of each item in the sequence. 

# Syntax 
The syntax for the enumerate() function is:

enumerate(sequence, start=0)

# Parameters
sequence - any iterable object (list, tuple, string, etc.)
start (optional) - index to start the sequence from

# Return Value
The enumerate() function returns an enumerate object. This object contains a count (from start which defaults to 0) and the values obtained from iterating over the sequence.
