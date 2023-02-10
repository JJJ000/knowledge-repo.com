---
title: What is the total amount of elements in the JSON object?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: The total number of items on a JSON object can be determined by counting the number of key-value pairs.
---

**Contents**

[TOC]

## Counting Properties

A JSON object can contain any number of properties. To get the total number of properties in a JSON object, you can use the `Object.keys()` method. This method returns an array of all the keys in the JSON object. The length of this array is equal to the total number of properties in the JSON object.

## Counting Values

A JSON object can also contain any number of values. To get the total number of values in a JSON object, you can use the `Object.values()` method. This method returns an array of all the values in the JSON object. The length of this array is equal to the total number of values in the JSON object.

## Counting Entries

A JSON object can also contain any number of entries. To get the total number of entries in a JSON object, you can use the `Object.entries()` method. This method returns an array of all the entries in the JSON object. The length of this array is equal to the total number of entries in the JSON object.

## Total Count

The total number of items in a JSON object can be calculated by adding the total number of properties, values, and entries. This can be done by using the `Object.keys()`, `Object.values()`, and `Object.entries()` methods and adding the lengths of the returned arrays.
