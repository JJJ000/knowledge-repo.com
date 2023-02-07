---
title: What is the best way to choose text elements using jquery?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: Use the jQuery selector `$(`*contains(text)`)` to select text nodes.
---

**Contents**

[TOC]

## Using the :contains() Selector
The :contains() selector allows you to select elements based on their text content. This selector can be used to select text nodes with jQuery.

## Syntax
The syntax for the :contains() selector is as follows:

```
$(":contains(text)")
```

Where "text" is the text content that you want to select.

## Example
To select a text node with the text "Example Text" using the :contains() selector, you would use the following syntax:

```
$(":contains('Example Text')")
```

## Note
It is important to note that the :contains() selector is case sensitive.
