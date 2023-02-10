---
title: Retrieving JSON items
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: JSON elements can be accessed using a combination of array indexes and object keys.
---

**Contents**

[TOC]

**Section 1: Accessing JSON Data**

JSON (JavaScript Object Notation) is a lightweight data-interchange format that is used to exchange data between different systems. It is a text-based format that is easy to read and write. JSON is a language-independent format and is used in many programming languages. 

JSON is composed of two structures: a collection of name/value pairs and an ordered list of values. It is easy to access JSON data using the dot notation or the bracket notation. 

**Section 2: Dot Notation**

The dot notation is the most common way to access JSON elements. It uses the dot operator (.) to access the values of an object. For example, if the JSON data is stored in a variable called “data”, then the value of the “name” property can be accessed using the following syntax:

data.name

**Section 3: Bracket Notation**

The bracket notation is also used to access JSON elements. It uses the square brackets ([ ]) to access the values of an object. For example, if the JSON data is stored in a variable called “data”, then the value of the “name” property can be accessed using the following syntax:

data[“name”]

**Section 4: Accessing Nested JSON Elements**

JSON data can be nested, meaning that an object can contain other objects. To access a nested element, the dot notation or the bracket notation can be used. For example, if the JSON data is stored in a variable called “data” and it contains an object “person”, then the value of the “name” property of the “person” object can be accessed using the following syntax:

data.person.name

or

data[“person”][“name”]
