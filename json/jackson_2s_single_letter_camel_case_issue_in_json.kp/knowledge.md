---
title: Why does Jackson 2 not recognize the first capital letter if the initial word in camel case is only one letter long?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-15 00:00:00
updated_at: 2023-02-15 00:00:00
tldr: Jackson 2 does not recognize the first capital letter if the leading camel case word is only a single letter long because it is not considered a valid identifier in Java.
---

**Contents**

[TOC]

# Section 1: Definition of Camel Case
Camel case is a method of writing compound words or phrases in which each word or abbreviation in the middle of the phrase begins with a capital letter, with no intervening spaces or punctuation.

# Section 2: Overview of JSON
JSON (JavaScript Object Notation) is a lightweight data-interchange format. It is a text-based, human-readable format for representing simple data structures and associative arrays (called objects).

# Section 3: Reasons for Jackson 2 Not Recognizing Single Capital Letter
The reason why Jackson 2 does not recognize the first capital letter if the leading camel case word is only a single letter long in Json is because it is not a valid syntax according to the JSON specification. The JSON specification states that names (keys) must be double-quoted strings, and strings in JSON must be composed of Unicode characters. Therefore, a single letter is not a valid syntax. 

# Section 4: Solution
The solution is to use a different data-interchange format such as YAML (YAML Ain't Markup Language) which does not have the same restrictions as JSON. YAML supports single letter capitalization and does not require double-quoting of names.
