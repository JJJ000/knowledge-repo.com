---
title: What is the best way to store an es6 map in localstorage (or another location)?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-11 00:00:00
updated_at: 2023-02-11 00:00:00
tldr: You can convert the ES6 Map to a JSON string using the built-in JSON.stringify() method, then store it in localstorage.
---

**Contents**

[TOC]

1. Converting Map to JSON

In order to persist a ES6 Map in localstorage or elsewhere in JSON, the Map must first be converted to JSON. This can be done by using the `JSON.stringify()` method on the Map object. This method takes the Map object and returns a JSON string representation of it.

2. Storing Map in LocalStorage

Once the Map has been converted to JSON, it can be stored in localstorage by using the `localStorage.setItem()` method. This method takes two parameters: the key to use for storage and the value to store. In this case, the key should be a descriptive name for the Map, and the value should be the JSON string representation of the Map.

3. Retrieving Map from LocalStorage

When the Map needs to be retrieved from localstorage, the `localStorage.getItem()` method can be used. This method takes the key that was used to store the Map and returns the value that was stored. In this case, the value will be the JSON string representation of the Map.

4. Converting JSON to Map

Once the JSON string representation of the Map has been retrieved from localstorage, it can be converted back to a Map object by using the `JSON.parse()` method. This method takes the JSON string representation of the Map and returns a Map object.
