---
title: How can I prevent the explicit promise construction antipattern?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-04 00:00:00
updated_at: 2023-02-04 00:00:00
tldr: The explicit promise construction antipattern is when a promise is created and immediately resolved or rejected, which can lead to unexpected behavior; it is best avoided by using the Promise constructor only when necessary.
---

**Contents**

[TOC]

## What is the Explicit Promise Construction Antipattern?
The Explicit Promise Construction Antipattern is when a developer uses the `new Promise` constructor to create a promise object instead of using the `async`/`await` syntax. This can lead to code that is hard to read and maintain.

## Why is it an Antipattern?
Using the `new Promise` constructor to create a promise object is an antipattern because it can lead to code that is difficult to read and maintain. It also means that the code is not using the latest language features, which can make it more difficult to debug and update.

## How to Avoid it in Javascript
The best way to avoid the Explicit Promise Construction Antipattern in Javascript is to use the `async`/`await` syntax instead. This syntax allows developers to write code that is more concise and easier to read and maintain. It also allows developers to take advantage of the latest language features, which can make debugging and updating code easier.
