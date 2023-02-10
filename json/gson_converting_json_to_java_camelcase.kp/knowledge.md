---
title: Use gson to change JSON property names to Java camel case notation
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: Gson can be used to convert JSON style properties names to Java CamelCase names by using its setFieldNamingStrategy() method.
---

**Contents**

[TOC]

# Section 1 - Overview

Gson is a Java library used for serializing and deserializing Java objects from and to JSON. It is part of the Google Gson library and provides a way to convert JSON style property names to Java CamelCase names.

# Section 2 - How to Convert

To convert JSON style property names to Java CamelCase names with Gson in Json, you need to use the GsonBuilder class. This class provides a set of methods for configuring the Gson instance. One of the methods is setFieldNamingStrategy which allows you to specify a strategy for naming the fields in the JSON object.

# Section 3 - Example

For example, if you have a JSON object with a property named "first_name", you can use the GsonBuilder to convert it to "firstName" in Java.

Gson gson = new GsonBuilder().setFieldNamingStrategy(FieldNamingPolicy.LOWER_CASE_WITH_UNDERSCORES).create();

# Section 4 - Conclusion

By using the GsonBuilder class, you can easily convert JSON style property names to Java CamelCase names. This allows you to easily work with JSON objects in Java without having to worry about different naming conventions.
