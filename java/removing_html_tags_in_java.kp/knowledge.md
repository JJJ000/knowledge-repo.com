---
title: Strip html tags from a string
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: Use the String.replaceAll() method to replace all HTML tags with an empty string.
---

**Contents**

[TOC]

### Using Regular Expressions

Java provides a powerful regex library that can be used to remove HTML tags from a String. The following code snippet demonstrates how to use regex to remove HTML tags from a String:

```java
String str = "<p>This is a sample string with HTML tags</p>";
String strWithoutTags = str.replaceAll("<[^>]*>", "");
```

The `replaceAll` method takes a regex pattern as an argument and replaces all occurrences of the pattern in the String with an empty String. In this case, the regex pattern `<[^>]*>` matches any HTML tag and replaces it with an empty String.

### Using Java Libraries

There are also several Java libraries that can be used to remove HTML tags from a String. The following code snippet demonstrates how to use the Jsoup library to remove HTML tags from a String:

```java
String str = "<p>This is a sample string with HTML tags</p>";
String strWithoutTags = Jsoup.parse(str).text();
```

The `parse` method takes a String as an argument and parses it into a Jsoup Document object. The `text` method then extracts the text from the Document object and returns a String without any HTML tags.

### Using a Custom Parser

It is also possible to create a custom parser to remove HTML tags from a String. The following code snippet demonstrates how to create a custom parser to remove HTML tags from a String:

```java
String str = "<p>This is a sample string with HTML tags</p>";
String strWithoutTags = "";

for (int i = 0; i < str.length(); i++) {
    char c = str.charAt(i);
    if (c != '<' && c != '>') {
        strWithoutTags += c;
    }
}
```

The code iterates over each character in the String and checks if it is an HTML tag. If it is not an HTML tag, it is added to the `strWithoutTags` String. This approach is not as efficient as the other two approaches, but it can be useful if the other approaches are not available.
