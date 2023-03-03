---
title: Constructing a gson instance
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-03-03 00:00:00
updated_at: 2023-03-03 00:00:00
tldr: Create a GSON object by calling the Gson() constructor.
---

**Contents**

[TOC]

**Section 1:** Creating GSON Object

Gson is a Java library that can be used to convert Java Objects into their JSON representation. It can also be used to convert a JSON string to an equivalent Java object. Gson can work with arbitrary Java objects including pre-existing objects that you do not have source-code of.

**Section 2:** Creating JSON String

To create a JSON string from a Java object, we can use the toJson() method of the Gson class. This method takes the object for which JSON representation is to be created as parameter and returns the JSON representation in the form of String.

**Section 3:** Creating JSON Object

To create a JSON Object from a Java object, we can use the fromJson() method of the Gson class. This method takes the JSON string and the class of the object to which it is to be converted as parameters. It returns an object of the specified class.

**Section 4:** Usage

Gson can be used to convert Java objects to JSON strings and vice-versa. It can also be used to convert a JSON string to an equivalent Java object. It is an open source library which is used to serialize and deserialize Java objects to JSON.
