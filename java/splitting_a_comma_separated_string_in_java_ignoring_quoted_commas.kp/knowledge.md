---
title: Creating a list from a comma-separated string while disregarding commas within quotation marks in java
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use a regular expression with a negative lookahead to split the string on commas that are not preceded by a quote.
---

**Contents**

[TOC]

### Solution 1: Using Regular Expressions

One approach to solving this problem is to use regular expressions. Regular expressions allow for the matching of patterns within a string. This can be used to identify the parts of the string that are within quotes and to exclude them from the comma-separated string split. 

The following code snippet demonstrates this approach:

```java
String[] parts = str.split("(?<!\\\")\\s*,\\s*(?!\\\")");
```

The regular expression `(?<!\\\")\\s*,\\s*(?!\\\")` is used to identify the commas that are not inside quotes. This expression matches any comma that is preceded by an odd number of backslashes (`(?<!\\\")`) and followed by an even number of backslashes (`(?!\\\")`). This ensures that the commas inside quotes are not matched and are therefore not split. 

### Solution 2: Using a Tokenizer

Another approach to solving this problem is to use a tokenizer. A tokenizer is a class that is used to break a string into tokens. It can be used to split the string on commas, while ignoring the commas that are inside quotes. 

The following code snippet demonstrates this approach:

```java
StringTokenizer st = new StringTokenizer(str, ",");
List<String> parts = new ArrayList<>();

while (st.hasMoreTokens()) {
    parts.add(st.nextToken().trim());
}
```

The `StringTokenizer` class is used to break the string into tokens based on the specified delimiter (in this case, a comma). The `hasMoreTokens()` method is used to check if there are any more tokens to be processed, and the `nextToken()` method is used to get the next token from the string. The `trim()` method is used to remove any whitespace from the token.

### Solution 3: Using a Scanner

A third approach to solving this problem is to use a scanner. A scanner is a class that is used to parse primitive types and strings from an input source. It can be used to split the string on commas, while ignoring the commas that are inside quotes. 

The following code snippet demonstrates this approach:

```java
Scanner scanner = new Scanner(str);
scanner.useDelimiter(",");
List<String> parts = new ArrayList<>();

while (scanner.hasNext()) {
    parts.add(scanner.next().trim());
}
```

The `Scanner` class is used to parse the string. The `useDelimiter()` method is used to specify the delimiter (in this case, a comma). The `hasNext()` method is used to check if there are any more tokens to be processed, and the `next()` method is used to get the next token from the string. The `trim()` method is used to remove any whitespace from the token.
