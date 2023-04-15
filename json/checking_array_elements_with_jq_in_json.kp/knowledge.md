---
title: How can we determine the existence of an element in an array using jq?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use the `in` operator with the array and element to check if the element exists in the array with jq.
---

**Contents**

[TOC]

## Introduction

If you are working with JSON data using `jq`, you might encounter situations where you need to check if an element exists in an array. In this tutorial, we will learn how to use `jq` to check if an element exists in an array in JSON.

## Prerequisites

Before we begin, you should have `jq` installed on your system. If you are using a Linux or macOS system, `jq` may already be installed. If it is not, you can use your package manager to install it. On Windows, you can download `jq` from the official website.

## Checking if an element exists in an array

To check if an element exists in an array using `jq`, we can use the `index` function. The `index` function returns the index of the first occurrence of the element in the array, or -1 if the element is not found.

Here is an example:

```bash
$ echo '[1, 2, 3]' | jq 'index(2)'
1
```

In this example, we have an array `[1, 2, 3]` and we are using the `index` function to check if the element `2` exists in the array. The function returns `1`, which is the index of `2` in the array.

If the element does not exist in the array, the `index` function will return `-1`.

```bash
$ echo '[1, 2, 3]' | jq 'index(4)'
-1
```

## Using the contains function

Another way to check if an element exists in an array using `jq` is to use the `contains` function. The `contains` function returns `true` if the element exists in the array, and `false` otherwise.

Here is an example:

```bash
$ echo '[1, 2, 3]' | jq 'contains(2)'
true
```

In this example, we are checking if the element `2` exists in the array `[1, 2, 3]` using the `contains` function. The function returns `true`.

If the element does not exist in the array, the `contains` function will return `false`.

```bash
$ echo '[1, 2, 3]' | jq 'contains(4)'
false
```

## Conclusion

In this tutorial, we have learned how to check if an element exists in an array using `jq`. We can use the `index` function to get the index of the element in the array, or the `contains` function to get a boolean value indicating if the element exists in the array.
