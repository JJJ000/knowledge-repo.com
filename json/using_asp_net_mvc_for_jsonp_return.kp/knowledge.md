---
title: Creating a jsonp response with ASP.NET mvc
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-12 00:00:00
updated_at: 2023-02-12 00:00:00
tldr: Yes, ASP.net MVC can return JSONP by setting the `dataType` parameter to `jsonp` when making an AJAX call.
---

**Contents**

[TOC]

## Section 1: What is JSONP?

JSONP (JSON with Padding) is a technique used to overcome the same-origin policy restrictions of modern web browsers. It allows a web page to request data from a server in a different domain. This is done by adding a special parameter to the request that contains a callback function name. The server then sends back the requested data in the form of a JavaScript function call, with the data as the argument.

## Section 2: How Does JSONP Work?

JSONP works by adding a special parameter to the request that contains a callback function name. The server then sends back the requested data in the form of a JavaScript function call, with the data as the argument. The web page then executes the callback function, passing the data as an argument.

## Section 3: How to Return JSONP in ASP.NET MVC

To return JSONP in ASP.NET MVC, you can use the JsonpResult class. This class is available in the System.Web.Mvc namespace. To use it, you need to create an instance of the JsonpResult class, passing the data you want to return as a parameter. You also need to specify the callback function name.

## Section 4: Example

The following example shows how to return JSONP in ASP.NET MVC. It returns a list of books in the form of a JavaScript function call.

```csharp
public ActionResult GetBooks()
{
    var books = new List<Book>
    {
        new Book { Title = "Book 1", Author = "Author 1" },
        new Book { Title = "Book 2", Author = "Author 2" }
    };

    return new JsonpResult(books, "callback");
}
```

The above code will return the following JavaScript:

```javascript
callback([
    { "Title": "Book 1", "Author": "Author 1" },
    { "Title": "Book 2", "Author": "Author 2" }
]);
```
