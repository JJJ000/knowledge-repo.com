---
title: What is the best way to delete the final character from a string?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: The last character of a string in Java can be removed using the substring() method.
---

**Contents**

[TOC]

`**` Using substring()**

The `substring()` method can be used to remove the last character from a string in Java. The syntax is `string_name.substring(0, string_name.length()-1)`, where `string_name` is the name of the string. This will return a new string with the last character removed.

`**` Using StringBuilder**

The `StringBuilder` class can also be used to remove the last character from a string in Java. The syntax is `stringBuilder_name.deleteCharAt(stringBuilder_name.length()-1)`, where `stringBuilder_name` is the name of the `StringBuilder` object. This will modify the existing `StringBuilder` object, and will not return a new string.

`**` Using StringBuffer**

The `StringBuffer` class can also be used to remove the last character from a string in Java. The syntax is `stringBuffer_name.deleteCharAt(stringBuffer_name.length()-1)`, where `stringBuffer_name` is the name of the `StringBuffer` object. This will modify the existing `StringBuffer` object, and will not return a new string.

`**` Using Regular Expressions**

Regular expressions can also be used to remove the last character from a string in Java. The syntax is `string_name.replaceAll("(.*).$", "$1")`, where `string_name` is the name of the string. This will return a new string with the last character removed.
