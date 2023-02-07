---
title: I want to take out the quotation marks from a string
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: Use the replace() method to replace double quotes with an empty string.
---

**Contents**

[TOC]

#1. Using String.replace()

The String.replace() method can be used to remove double quotes from a String. The syntax for this method is as follows:

```
string.replace(/["]/g, '');
```

This will replace all occurrences of double quotes in the String with an empty string, effectively removing them.

#2. Using Regular Expressions

Regular expressions can also be used to remove double quotes from a String. The syntax for this is as follows:

```
string.replace(/"/g, '');
```

This will replace all occurrences of double quotes in the String with an empty string, effectively removing them.

#3. Using String.split()

The String.split() method can be used to remove double quotes from a String. The syntax for this method is as follows:

```
string.split('"').join('');
```

This will split the String at each occurrence of a double quote and then join the resulting array of substrings together, effectively removing the double quotes.

#4. Using String.substr()

The String.substr() method can be used to remove double quotes from a String. The syntax for this method is as follows:

```
string.substr(1, string.length - 2);
```

This will return a substring of the original string, starting from the second character and ending at the second-to-last character, effectively removing the double quotes.
