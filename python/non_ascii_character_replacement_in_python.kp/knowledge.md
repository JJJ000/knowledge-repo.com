---
title: Substitute any non-ascii characters with a single space
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: Use the str.replace() method to replace all non-ASCII characters with a single space.
---

**Contents**

[TOC]

#1 Regular Expressions 
Python's `re` module can be used to replace non-ASCII characters with a single space. The `re.sub()` function can be used to perform a search and replace for a pattern in a string. The following code snippet can be used to replace non-ASCII characters with a single space:

```python
import re

string = "This string contains non-ASCII characters!"
string = re.sub(r'[^\x00-\x7F]+',' ', string)
```

#2 String Manipulation
Python's `str.translate()` method can also be used to replace non-ASCII characters with a single space. The `str.maketrans()` method can be used to create a translation table that specifies which characters should be replaced. The following code snippet can be used to replace non-ASCII characters with a single space:

```python
import string

string = "This string contains non-ASCII characters!"
table = str.maketrans('', '', string.punctuation)
string = string.translate(table)
```

#3 Unicode Normalization
Python's `unicodedata` module can be used to normalize a Unicode string, which can be used to replace non-ASCII characters with a single space. The `unicodedata.normalize()` method can be used to normalize a Unicode string. The following code snippet can be used to replace non-ASCII characters with a single space:

```python
import unicodedata

string = "This string contains non-ASCII characters!"
string = unicodedata.normalize('NFKD', string).encode('ASCII', 'ignore').decode('ASCII')
```

#4 Character Mapping
Python's `str.replace()` method can also be used to replace non-ASCII characters with a single space. The `str.maketrans()` method can be used to create a mapping table that specifies which characters should be replaced. The following code snippet can be used to replace non-ASCII characters with a single space:

```python
import string

string = "This string contains non-ASCII characters!"
table = str.maketrans(string.punctuation, ' '*len(string.punctuation))
string = string.translate(table)
```
