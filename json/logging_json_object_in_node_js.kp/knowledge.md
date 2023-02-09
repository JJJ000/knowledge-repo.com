---
title: What is the process for printing the contents of a JSON object in node.js?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-08 00:00:00
updated_at: 2023-02-08 00:00:00
tldr: You can log the content of a JSON object in Node.js using the JSON.stringify() method.
---

**Contents**

[TOC]

#1 Console.log

The simplest way to log content of a JSON object in Node.js is by using the `console.log` method. This method takes in the JSON object as an argument and prints it to the console.

#2 Stringify

Another way to log content of a JSON object in Node.js is by using the `JSON.stringify` method. This method takes in the JSON object as an argument and returns a string representation of the object. This string can then be logged to the console using the `console.log` method.

#3 Pretty Print

If you want to log the content of a JSON object in a more readable format, you can use the `JSON.stringify` method with the `pretty` option set to `true`. This will return a string representation of the object in a more readable format. This string can then be logged to the console using the `console.log` method.
