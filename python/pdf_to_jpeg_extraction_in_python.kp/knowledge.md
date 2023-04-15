---
title: Convert a pdf page to jpeg format
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use the PyPDF2 library in Python to extract a page from a pdf as a jpeg.
---

**Contents**

[TOC]

# Importing Required Libraries

To extract pages from a PDF in Python, we need to use the `PyPDF2` library. To install it, we can use `pip`

```python
!pip install PyPDF2
```

Once it is installed, we'll import the required libraries.

```python
import os
import PyPDF2
from PIL import Image
```

# Converting PDF Pages to JPEG

Now that the required libraries are imported, let's write the code to extract a page from a PDF as a JPEG. 

First, we need to open the PDF file using the `open` method from the `PyPDF2` library.

```python
# Open the PDF file
pdf_file = open('path/to/pdf/file.pdf', 'rb')
```

Next, we'll use the `PdfFileReader` method to read the opened PDF file and then use the `getPage` method to extract the required page.

```python
# Read the PDF file
pdf_reader = PyPDF2.PdfFileReader(pdf_file)

# Extract the required page
page = pdf_reader.getPage(0)
```

We can now use the `PIL` library to convert the extracted page to JPEG format.

```python
# Convert the extracted page to JPEG format
image = page.to_image()

# Save the JPEG file to disk
image.save('path/to/destination/file.jpg', 'JPEG')
```

# Putting it All Together

The complete code to extract a PDF page as a JPEG is given below.

```python
import os
import PyPDF2
from PIL import Image

# Open the PDF file
pdf_file = open('path/to/pdf/file.pdf', 'rb')

# Read the PDF file
pdf_reader = PyPDF2.PdfFileReader(pdf_file)

# Extract the required page
page = pdf_reader.getPage(0)

# Convert the extracted page to JPEG format
image = page.to_image()

# Save the JPEG file to disk
image.save('path/to/destination/file.jpg', 'JPEG')
```

This code will extract the first page of the PDF file as a JPEG and save it to the destination folder. You can modify it to extract different pages of the PDF file or save them in different formats.

# Conclusion

In this tutorial, we learned how to extract a page from a PDF as a JPEG in Python. We used the `PyPDF2` and `PIL` libraries to achieve this. You can use this code to extract pages from PDF files and save them in different formats like JPEG, PNG, etc.
