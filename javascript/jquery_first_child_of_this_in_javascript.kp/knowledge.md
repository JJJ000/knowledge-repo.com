---
title: The first child of 'this' in jquery
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: jQuery`s equivalent of the Javascript `this` keyword is $(this), and the first child of this can be accessed with $(this).children().first().
---

**Contents**

[TOC]

1. What is jQuery?
    jQuery is a fast, small, and feature-rich JavaScript library. It makes things like HTML document traversal and manipulation, event handling, animation, and Ajax much simpler with an easy-to-use API that works across a multitude of browsers.

2. How to Select the First Child of "this"
    To select the first child of "this" using jQuery, you can use the `.children()` method. This method takes a selector as an optional argument, and returns all direct children of the selected element. If no selector is provided, it will return all children of the selected element.

3. Example Syntax
    The syntax for selecting the first child of "this" using jQuery is:
    ```
    $(this).children(:first)
    ```

4. Example Usage
    Here is an example of how the `.children()` method can be used to select the first child of "this":
    ```
    $(this).children(:first).css("background-color", "red");
    ```
    This will set the background color of the first child of "this" to red.
