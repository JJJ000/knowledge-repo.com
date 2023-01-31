---
title: Extracting files from a zipped archive using python
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-01-30 00:00:00
updated_at: 2023-01-30 00:00:00
tldr: To unzip files in Python, use the zipfile module to extract the contents of the file.
---

**Contents**

[TOC]

1. Importing the Necessary Libraries
------------------------------------
In order to unzip files in Python, we will need to import the `zipfile` library.

```python
import zipfile
```

2. Opening the Zip File
-----------------------
We can open the zip file using the `ZipFile` class. We will need to pass the name of the zip file as an argument to the `ZipFile` class.

```python
zip_ref = zipfile.ZipFile("filename.zip", 'r')
```

3. Extracting the Files
-----------------------
We can extract the files from the zip file using the `extractall` method. We will need to pass the path where the files should be extracted as an argument to the `extractall` method.

```python
zip_ref.extractall("/path/to/extract/")
```

4. Closing the Zip File
-----------------------
Finally, we can close the zip file using the `close` method.

```python
zip_ref.close()
```
