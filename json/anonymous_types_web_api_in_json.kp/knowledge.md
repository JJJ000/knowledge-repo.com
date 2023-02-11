---
title: Creating anonymous types with web api
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-11 00:00:00
updated_at: 2023-02-11 00:00:00
tldr: Web API can return anonymous types as JSON by using the JsonResult type.
---

**Contents**

[TOC]

## Section 1: What is an Anonymous Type
An anonymous type is a type that is dynamically generated at compile time by the compiler. It is not given an explicit name, and can only be referenced through its properties. Anonymous types are commonly used in LINQ queries to return a subset of properties from one or more objects.

## Section 2: Using Anonymous Types with Web API
Anonymous types can be used with Web API to return a subset of properties from an object in a JSON response. This is done by using the `Select` LINQ operator to create a new anonymous type with the desired properties. The anonymous type is then returned from the Web API controller action.

## Section 3: Serializing Anonymous Types
When an anonymous type is used with Web API, the JSON serializer must be configured to recognize the anonymous type and serialize it correctly. This can be done by setting the `SerializerSettings.TypeNameHandling` property of the `JsonSerializerSettings` object to `TypeNameHandling.All`. This will allow the JSON serializer to recognize and serialize the anonymous type correctly.

## Section 4: Example
For example, consider the following controller action that returns a list of books:
```
public IHttpActionResult GetBooks()
{
    var books = _bookRepository.GetBooks();

    var booksModel = books.Select(b => new
    {
        Title = b.Title,
        Author = b.Author
    });

    return Ok(booksModel);
}
```
In this example, an anonymous type is used to return only the `Title` and `Author` properties of the `Book` object. The `JsonSerializerSettings` object must be configured to recognize the anonymous type in order for the JSON serializer to serialize it correctly.
