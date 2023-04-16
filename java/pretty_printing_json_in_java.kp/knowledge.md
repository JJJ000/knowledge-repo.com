---
title: Print JSON in a readable format using java
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: The Jackson library can be used to pretty-print JSON in Java.
---

**Contents**

[TOC]

**Section 1: Using Jackson**

Jackson is a popular library used for parsing and formatting JSON in Java. To pretty-print JSON using Jackson, we can use the Jackson ObjectMapper class. The ObjectMapper class provides writeValueAsString() and writeValueAsPrettyPrintString() methods that can be used to serialize an object to a JSON string. The writeValueAsPrettyPrintString() method will format the JSON string with indentation and line breaks for improved readability.

**Section 2: Using Gson**

Gson is another popular library for parsing and formatting JSON in Java. To pretty-print JSON using Gson, we can use the GsonBuilder class. The GsonBuilder class provides a setPrettyPrinting() method that can be used to enable pretty printing of the JSON output. Once enabled, the Gson class can be used to serialize an object to a JSON string with indentation and line breaks for improved readability.

**Section 3: Using Json-lib**

Json-lib is a library for parsing and formatting JSON in Java. To pretty-print JSON using Json-lib, we can use the JSONObject class. The JSONObject class provides a toString(int indentFactor) method that can be used to serialize an object to a JSON string with indentation and line breaks for improved readability. The indentFactor parameter specifies the number of spaces to be used for indentation.

**Section 4: Using Json.simple**

Json.simple is a library for parsing and formatting JSON in Java. To pretty-print JSON using Json.simple, we can use the JSONValue class. The JSONValue class provides a toJSONString(Object value, int indentFactor) method that can be used to serialize an object to a JSON string with indentation and line breaks for improved readability. The indentFactor parameter specifies the number of spaces to be used for indentation.
