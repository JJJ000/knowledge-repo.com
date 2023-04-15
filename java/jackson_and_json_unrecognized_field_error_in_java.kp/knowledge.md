---
title: Jackson encountered an unrecognized field in the JSON which was not marked as ignorable
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: The unrecognized field will be ignored by default, but can be marked as ignorable with the @JsonIgnore annotation.
---

**Contents**

[TOC]

### What is JSON?

JSON (JavaScript Object Notation) is a lightweight data-interchange format that is used to exchange data between different applications. It is based on a subset of the JavaScript programming language and is easy to read and write. JSON is commonly used in web applications to transfer data between the client and the server.

### What is an Unrecognized Field?

An unrecognized field is a field in a JSON document that is not recognized by the application that is trying to parse it. This can occur when the application is expecting a specific type of data, but the data provided is in a different format or is not in the expected format.

### How to Handle Unrecognized Fields?

When an unrecognized field is encountered, it can be handled in several ways. One way is to ignore the unrecognized field and continue parsing the rest of the JSON document. This is usually done when the unrecognized field is not important to the application.

Another way to handle unrecognized fields is to mark them as ignorable. This can be done in Java by using the @JsonIgnoreProperties annotation. This annotation tells the parser to ignore any fields that are not explicitly specified.

### Conclusion

Unrecognized fields can be a source of errors when parsing JSON documents. To prevent these errors, it is important to mark unrecognized fields as ignorable. In Java, this can be done by using the @JsonIgnoreProperties annotation. By doing this, the parser will ignore any unrecognized fields and allow the application to continue parsing the rest of the JSON document.
