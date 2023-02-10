---
title: What is the most effective way to include arbitrary JSON in the dom?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: The best practice for embedding arbitrary JSON in the DOM is to use the HTML5 data-* attribute.
---

**Contents**

[TOC]

## Parsing the JSON

The first step in embedding arbitrary JSON in the DOM is to parse the JSON data. This can be done using the `JSON.parse()` method. This method takes a string containing valid JSON and returns a JavaScript object.

## Creating an Element

Once the JSON has been parsed, the next step is to create an element in the DOM to contain the JSON data. This can be done using the `document.createElement()` method. This method takes a tag name as an argument and returns an HTML element.

## Setting the Data Attribute

Once the element has been created, the JSON data must be associated with the element. This can be done by setting the `data-json` attribute of the element to the parsed JSON. This can be done using the `element.setAttribute()` method.

## Appending the Element

Finally, the element must be appended to the DOM. This can be done using the `element.appendChild()` method. This method takes an element as an argument and appends it to the DOM.
