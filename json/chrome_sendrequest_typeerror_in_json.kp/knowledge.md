---
title: Error when chrome attempted to send a request typeerror unable to convert circular structure into JSON format
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-08 00:00:00
updated_at: 2023-02-08 00:00:00
tldr: Circular structures cannot be converted to JSON, so an error will be thrown.
---

**Contents**

[TOC]

## Section 1: What is a Circular Structure?
A circular structure is an object or data structure that contains a reference to itself. This can happen when an object has a property that references itself, or when two objects have properties that reference each other.

## Section 2: What is JSON?
JSON (JavaScript Object Notation) is a lightweight data-interchange format. It is a text-based data format that is designed to be easy for humans to read and write, and for machines to parse and generate.

## Section 3: What is the Error?
When attempting to convert a circular structure to JSON, the Chrome sendrequest error will throw a TypeError. This is because JSON does not support circular structures, and therefore attempting to convert one will result in an error.

## Section 4: How to Resolve the Error?
The best way to resolve the error is to avoid using circular structures in the first place. If the data structure is necessary, then the circular references must be broken by replacing the references with unique identifiers. This will allow the data structure to be converted to JSON without any errors.
