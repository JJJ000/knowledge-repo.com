---
title: What is the best way to get out of a JSON string?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: Use backslashes to escape special characters in a JSON string.
---

**Contents**

[TOC]

# Section 1: Escaping Special Characters

When encoding a JSON string, certain characters must be escaped in order to ensure that the JSON string is valid and can be parsed correctly. The most common characters to escape are quotation marks, backslashes, and control characters (e.g. newline, tab). To escape these characters, they must be preceded by a backslash (\). For example:

```
"This is a \"quoted\" string"
```

# Section 2: Escaping Unicode Characters

In addition to the standard ASCII characters, JSON strings may also contain Unicode characters. Unicode characters must also be escaped in order to ensure that the JSON string is valid and can be parsed correctly. To escape Unicode characters, they must be preceded by a backslash (\u) followed by the four-digit hexadecimal code for the character. For example:

```
"This is a \u00A9 copyright symbol"
```

# Section 3: Escaping HTML Characters

If a JSON string contains HTML characters, they must also be escaped in order to ensure that the JSON string is valid and can be parsed correctly. To escape HTML characters, they must be preceded by a backslash (\u) followed by the six-digit hexadecimal code for the character. For example:

```
"This is a \u0026lt; less than symbol"
```

# Section 4: Escaping Other Characters

In addition to the characters mentioned above, there may be other characters that must be escaped in order to ensure that the JSON string is valid and can be parsed correctly. To escape these characters, they must be preceded by a backslash (\u) followed by the four-digit hexadecimal code for the character. For example:

```
"This is a \u00A0 non-breaking space"
```
