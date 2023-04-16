---
title: Looping through htmlcollection elements using a for loop
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: A for loop can be used to iterate through an HTMLCollection in Javascript by accessing the elements via the item() method.
---

**Contents**

[TOC]

1. Definition of HTMLCollection
    HTMLCollection is an array-like object that contains a collection of HTML elements. It is a live collection that updates itself automatically when the DOM is changed.

2. Syntax
    The syntax for a for loop for HTMLCollection elements is as follows:

    ```
    for (let i = 0; i < collection.length; i++) {
        let element = collection[i];
        // Do something with element
    }
    ```

3. Example
    ```
    let divs = document.getElementsByTagName('div');
    for (let i = 0; i < divs.length; i++) {
        let div = divs[i];
        console.log(div);
    }
    ```

4. Benefits
    Using a for loop for HTMLCollection elements is beneficial because it provides a simple and efficient way to iterate over the elements in the collection. Additionally, it allows the programmer to perform an action on each element in the collection.
