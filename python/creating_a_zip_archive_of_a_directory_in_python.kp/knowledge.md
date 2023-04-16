---
title: What is the process for compressing a folder into a zip file?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use the shutil.make\_archive() function to create a zip archive of a directory in Python.
---

**Contents**

[TOC]

# Section 1: Importing the necessary modules

In order to create a zip archive of a directory in Python, we need to import the `shutil` and `zipfile` modules.

```python
import shutil
import zipfile
```

# Section 2: Setting the source and destination paths

Next, we need to define the source and destination paths. The source path is the directory that we want to create a zip archive of, while the destination path is the location where we want to save the archive.

```python
src_path = '/path/to/source/directory'
dest_path = '/path/to/destination/directory'
```

# Section 3: Creating the zip archive

Now, we can create the zip archive using the `zipfile.ZipFile` class. The `shutil.make_archive` function is a convenient way to create a zip archive from a directory.

```python
zip_file = zipfile.ZipFile(dest_path + '/archive.zip', 'w')
shutil.make_archive(dest_path + '/archive', 'zip', src_path)
```

# Section 4: Closing the zip archive

Finally, we need to close the zip archive once we are done creating it.

```python
zip_file.close()
```
