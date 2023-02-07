---
title: What is the process for converting html entities using jquery?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: jQuery`s .html() method can be used to decode HTML entities in Javascript.
---

**Contents**

[TOC]

# Section 1: Include jQuery

In order to decode HTML entities using jQuery, you must first include jQuery in your HTML document. This can be done by adding the following code to the `<head>` section of your HTML document:

```
<script src="https://ajax.googleapis.com/ajax/libs/jquery/3.4.1/jquery.min.js"></script>
```

# Section 2: Use the .html() Method

Once jQuery has been included in your HTML document, you can use the `.html()` method to decode HTML entities. This method takes a string containing HTML entities as an argument, and returns the decoded string.

For example, if you have the following HTML entities:

```
&lt;div&gt;This is a div&lt;/div&gt;
```

You can use the following code to decode it:

```
var decodedString = $('<div>').html('&lt;div&gt;This is a div&lt;/div&gt;').text();
```

# Section 3: Use the .text() Method

In addition to the `.html()` method, you can also use the `.text()` method to decode HTML entities. This method takes a string containing HTML entities as an argument, and returns the decoded string.

For example, if you have the following HTML entities:

```
&lt;div&gt;This is a div&lt;/div&gt;
```

You can use the following code to decode it:

```
var decodedString = $('<div>').text('&lt;div&gt;This is a div&lt;/div&gt;');
```

# Section 4: Considerations

When using the `.html()` or `.text()` method to decode HTML entities, it is important to note that the returned string will not contain the HTML tags. For example, if you have the following HTML entities:

```
&lt;div&gt;This is a div&lt;/div&gt;
```

The decoded string will be:

```
This is a div
```
