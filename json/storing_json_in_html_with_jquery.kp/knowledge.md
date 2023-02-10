---
title: Store a JSON object in an html data attribute using jquery
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: jQuery can be used to store JSON objects in HTML data attributes.
---

**Contents**

[TOC]

# Section 1: Storing JSON Object in Data Attribute

Using jQuery, you can store a JSON object in a data attribute in HTML. To do this, you need to use the jQuery `data()` method. This method allows you to store any type of data in an element's data-* attributes.

# Section 2: Syntax

The syntax for the jQuery `data()` method is as follows:

```
$(selector).data(key,value);
```

# Section 3: Example

Here is an example of how to store a JSON object in a data attribute in HTML using jQuery:

```
var jsonObj = {
  "name": "John",
  "age": 30
};

$("#myDiv").data("info", jsonObj);
```

# Section 4: Retrieving the JSON Object

To retrieve the JSON object from the data attribute, you can use the jQuery `data()` method again. The syntax for this is as follows:

```
$(selector).data(key);
```

Here is an example of how to retrieve the JSON object from the data attribute:

```
var jsonObj = $("#myDiv").data("info");
```
