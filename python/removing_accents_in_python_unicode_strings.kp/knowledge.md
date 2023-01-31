---
title: How can I normalize a Python unicode string by removing accents?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-01-30 00:00:00
updated_at: 2023-01-30 00:00:00
tldr: The best way to remove accents (normalize) in a Python unicode string is to use the unicodedata.normalize() function.
---

**Contents**

[TOC]

**Section 1: Using unicodedata Module**

The `unicodedata` module provides access to the Unicode Character Database which defines character properties for all Unicode characters. This module can be used to normalize (remove accents) from a Python unicode string.

The `normalize()` function takes two parameters: the first parameter is the form of normalization, and the second parameter is the string to be normalized. To remove accents, the `NFD` form should be used.

```python
import unicodedata

# Normalize string
normalized_string = unicodedata.normalize('NFD', string)

# Remove accents
no_accents_string = ''.join(c for c in normalized_string if not unicodedata.combining(c))
```

**Section 2: Using Regular Expressions**

Regular expressions can also be used to remove accents from a Python unicode string. The following code snippet will remove all diacritic marks from a string:

```python
import re

# Remove accents
no_accents_string = re.sub(r'[^\w\s]','',string)
```

**Section 3: Using str.translate()**

The `str.translate()` method can also be used to remove accents from a Python unicode string. The following code snippet will remove all diacritic marks from a string:

```python
import unicodedata

# Create a mapping of characters to be removed
combining_chars = ''.join(c for c in map(chr, range(sys.maxunicode)) if unicodedata.combining(c))

# Create a mapping table
mapping_table = {ord(c):None for c in combining_chars}

# Remove accents
no_accents_string = string.translate(mapping_table)
```

**Section 4: Using a Lookup Table**

A lookup table can also be used to remove accents from a Python unicode string. The following code snippet will remove all diacritic marks from a string:

```python
# Create a lookup table
lookup_table = {
    'á': 'a',
    'é': 'e',
    'í': 'i',
    'ó': 'o',
    'ú': 'u',
    ...
}

# Remove accents
no_accents_string = ''.join(lookup_table.get(c, c) for c in string)
```
