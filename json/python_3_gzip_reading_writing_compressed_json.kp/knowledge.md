---
title: Read and write JSON objects that are compressed with gzip from/to a file in Python 3
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-15 00:00:00
updated_at: 2023-02-15 00:00:00
tldr: You can use the gzip and JSON modules to read/write compressed JSON objects from/to a gzip file.
---

**Contents**

[TOC]

# Section 1: Reading Compressed JSON Objects from Gzip File

Python 3 has a gzip module that provides a comprehensive interface for the gzip file format. To read compressed JSON objects from a gzip file, use the `gzip.open()` function to open the file in read mode, and then use the `json.load()` function to read the JSON objects from the file.

```python
import gzip
import json

with gzip.open('file.json.gz', 'rb') as f:
    data = json.load(f)
```

# Section 2: Writing Compressed JSON Objects to Gzip File

To write compressed JSON objects to a gzip file, use the `gzip.open()` function to open the file in write mode, and then use the `json.dump()` function to write the JSON objects to the file.

```python
import gzip
import json

data = {'key': 'value'}

with gzip.open('file.json.gz', 'wb') as f:
    json.dump(data, f)
```

# Section 3: Compressing JSON Objects

In addition to reading and writing compressed JSON objects, the gzip module can also be used to compress JSON objects. To compress a JSON object, use the `gzip.compress()` function.

```python
import gzip
import json

data = {'key': 'value'}

compressed_data = gzip.compress(json.dumps(data))
```

# Section 4: Decompressing JSON Objects

The gzip module can also be used to decompress JSON objects. To decompress a JSON object, use the `gzip.decompress()` function.

```python
import gzip
import json

compressed_data = b'\x1f\x8b\x08\x00\x00\x00\x00\x00\x00\x03\xed\xccI\x02\x00\xcd\xc9\xc9W(\xcf/\xcaIQ\xccK\x04\x00\x00\x00'

data = json.loads(gzip.decompress(compressed_data))
```
