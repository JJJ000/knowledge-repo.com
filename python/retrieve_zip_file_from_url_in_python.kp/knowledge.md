---
title: Retrieve the zip file that has been returned via the url
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-17 00:00:00
updated_at: 2023-03-17 00:00:00
tldr: Use the urllib.request.urlretrieve() method to download a zip file from a URL in Python.
---

**Contents**

[TOC]

### Section 1: Introduction
In Python, there are different ways to download a file from a URL. One way is to use urllib module or requests module. In this article, we will discuss how to download a returned zip file from a URL using Python.

### Section 2: Downloading Zip file using requests.get() method
To download a zip file from a URL, we can use the requests module's get() method to fetch the file from the server. After getting the file, we can write it to a local file.

Here is how to download a zip file in Python using requests module:

```python
import requests

url = 'https://example.com/file.zip'
r = requests.get(url)

with open('file.zip', 'wb') as f:
    f.write(r.content)
```

This code snippet downloads a zip file from a given URL and saves it as file.zip in the current directory.

### Section 3: Extracting a Zip file in Python
After downloading a zip file, we may need to extract its contents for further processing. Python's zipfile module provides a convenient way of extracting zip files.

Here is an example of how to extract a zip file in Python:

```python
import zipfile

zip_ref = zipfile.ZipFile('file.zip', 'r')
zip_ref.extractall('.')
zip_ref.close()
```

This code first creates a ZipFile object, which is used to open the zip file. The extractall() method is used to extract all the contents of the zip file to the current directory. Finally, the close() method is called to close the zipfile object.

### Section 4: Downloading and Extracting a Zip file in Python
If you want to download and extract a zip file in Python, you can simply combine the code snippets from the previous sections:

```python
import requests
import zipfile

url = 'https://example.com/file.zip'
r = requests.get(url)

with open('file.zip', 'wb') as f:
    f.write(r.content)

zip_ref = zipfile.ZipFile('file.zip', 'r')
zip_ref.extractall('.')
zip_ref.close()
```

This code downloads the zip file, saves it as file.zip, and extracts its contents to the current directory. Finally, it closes the zipfile object.
