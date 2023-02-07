---
title: What is the distinction between using "process.stdout.write" and "console.log" in node.js?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: `process.stdout.write` writes output to the terminal without adding a new line, while `console.log` writes output to the terminal and adds a new line.
---

**Contents**

[TOC]

## Process.stdout.write
Process.stdout.write is a method in the Node.js standard library that prints a string or buffer to the terminal. It does not add a new line character to the end of the output, and it does not interpret any formatting or styling.

## Console.log
Console.log is a method in the Node.js standard library that prints a string or object to the terminal. It adds a new line character to the end of the output, and it interprets formatting and styling.

## Difference
The main difference between process.stdout.write and console.log is that process.stdout.write does not add a new line character to the end of the output, and it does not interpret any formatting or styling, while console.log adds a new line character to the end of the output and interprets formatting and styling.
