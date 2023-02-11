---
title: No mediatypeformatter is available to convert a 'string' object from 'text/plain' content
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-11 00:00:00
updated_at: 2023-02-11 00:00:00
tldr: No, a MediaTypeFormatter cannot be used to read a String from content with media type `text/plain` in Json.
---

**Contents**

[TOC]

1. What is a MediaTypeFormatter?
A MediaTypeFormatter is an object used to serialize and deserialize an object to and from an HTTP message body. It is used to convert an object to a specific format, such as XML, JSON, or binary.

2. What is the Problem?
The problem is that there is no MediaTypeFormatter available to read an object of type 'String' from content with media type 'text/plain' in JSON.

3. Possible Solutions
One possible solution is to use a custom MediaTypeFormatter. This would allow you to read the string from the content with the media type 'text/plain' in JSON.

Another possible solution is to use a library such as Newtonsoft.Json. This library provides a JsonConverter class that can be used to deserialize a string from content with media type 'text/plain' in JSON.

4. Conclusion
In order to read an object of type 'String' from content with media type 'text/plain' in JSON, either a custom MediaTypeFormatter or a library such as Newtonsoft.Json can be used.
