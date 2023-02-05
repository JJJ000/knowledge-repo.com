---
title: Shuffle two numpy arrays in sync
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: Using numpy.random.shuffle() on both arrays simultaneously is the best way to shuffle two numpy arrays in unison.
---

**Contents**

[TOC]

**Section 1: Preparing the Data**

Before shuffling two numpy arrays, it is important to ensure that the two arrays have the same number of elements. If the arrays have different lengths, they cannot be shuffled in unison. Additionally, if the arrays contain different types of data, they should be converted to the same data type before shuffling.

**Section 2: Using the Numpy Random Function**

The easiest way to shuffle two numpy arrays in unison is to use the numpy.random.shuffle() function. This function will randomly rearrange the elements of the two arrays in the same order. The syntax for using this function is:

```
numpy.random.shuffle(arr1, arr2)
```

Where arr1 and arr2 are the two arrays to be shuffled.

**Section 3: Using the Numpy Random Permutation Function**

Another way to shuffle two numpy arrays in unison is to use the numpy.random.permutation() function. This function will randomly rearrange the elements of the two arrays in the same order. The syntax for using this function is:

```
numpy.random.permutation(arr1, arr2)
```

Where arr1 and arr2 are the two arrays to be shuffled.

**Section 4: Using the Numpy Random Choice Function**

A third way to shuffle two numpy arrays in unison is to use the numpy.random.choice() function. This function will randomly select elements from each array and place them in a new array. The syntax for using this function is:

```
numpy.random.choice(arr1, arr2, size=len(arr1))
```

Where arr1 and arr2 are the two arrays to be shuffled and size is the length of arr1.
