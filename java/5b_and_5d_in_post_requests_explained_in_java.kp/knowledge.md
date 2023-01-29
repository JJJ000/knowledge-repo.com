---
title: What do the symbols '%5b' and '%5d' represent in post requests?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: %5B and %5D represent the opening and closing brackets, respectively, when passing data in a POST request in Java.
---

**Contents**

[TOC]

### Meaning

%5B and %5D are URL-encoded representations of the characters "[" and "]". These characters are used in POST requests to represent an array in Java.

### Usage

When making a POST request, the data sent to the server is typically in the form of a key-value pair. If the value is an array, the array must be encoded in the request. The %5B and %5D characters are used to represent the brackets which typically denote an array in Java.

For example, if the data being sent is an array of numbers, it might look like this:

`numbers[]=1&numbers[]=2&numbers[]=3`

The same data encoded in the URL would look like this:

`numbers%5B%5D=1&numbers%5B%5D=2&numbers%5B%5D=3`

### Example

Here is an example of a POST request in Java which sends an array of numbers:

```
URL url = new URL("http://example.com/post_request");
HttpURLConnection connection = (HttpURLConnection) url.openConnection();
connection.setRequestMethod("POST");
String urlParameters = "numbers%5B%5D=1&numbers%5B%5D=2&numbers%5B%5D=3";
connection.setDoOutput(true);
DataOutputStream wr = new DataOutputStream(connection.getOutputStream());
wr.writeBytes(urlParameters);
wr.flush();
wr.close();
```
