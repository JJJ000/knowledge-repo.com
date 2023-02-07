---
title: What is the process for accessing a url parameter in express?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: Use the req.query object to access URL parameters in Express.
---

**Contents**

[TOC]

# Section 1: Identify the URL Parameter

The URL parameter is the part of the URL after the question mark (?) that contains information that can be used to determine the page content. It is usually composed of key-value pairs, where the key is the parameter name and the value is the parameter value.

# Section 2: Retrieve the URL Parameter in Express

Express provides the `req.query` object to access the query parameters of the URL. This object is an object containing key-value pairs of the URL parameters. To access the value of a specific parameter, simply use the parameter name as the key.

# Section 3: Use the URL Parameter

Once you have retrieved the parameter value, you can use it to determine the page content. For example, if the parameter is a search query, you can use it to search for content in your database.

# Section 4: Example

For example, if the URL is `http://example.com?search=hello`, the parameter name is `search` and the parameter value is `hello`. To retrieve the parameter value in Express, use the following code:

```javascript
const searchQuery = req.query.search;
```

Then you can use the `searchQuery` variable to search your database for content related to the `hello` query.
