---
title: Using python, append text to an existing pdf
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-13 00:00:00
updated_at: 2023-03-13 00:00:00
tldr: You can add text to an existing PDF using Python by using the PyPDF2 library.
---

**Contents**

[TOC]

## Introduction
PDF is one of the most widely used document formats. Sometimes we need to add texts to an already existing PDF document. In this article, we will see how we can add text to an existing PDF using Python.

### Requirements
We will be using the following Python packages in this tutorial.
* **PyPDF2**: It is a Python library for working with PDF files.

## Method 1: Using PyPDF2

We can use the PyPDF2 library to add text to an existing PDF. The following steps can be followed.

1. Import necessary package
```python
import PyPDF2
```

2. Open the PDF file
```python
pdfFileObj = open('example.pdf', 'rb')
pdfReader = PyPDF2.PdfFileReader(pdfFileObj)
```

3. Create a new PDF writer object
```python
pdfWriter = PyPDF2.PdfFileWriter()
```

4. Get first page of PDF reader object
```python
pageObj = pdfReader.getPage(0)
```

5. Create a new object of text element
```python
textObj = PyPDF2.pdf.ContentStream([PyPDF2.pdf.TextObject('Hello, World!').encode('utf-8')])
```

6. Append the text element to the page object
```python
pageObj['/Contents'].append(textObj)
```

7. Add updated page to PDF writer object
```python
pdfWriter.addPage(pageObj)
```

8. Write the updated PDF writer object to a new file
```python
pdfOutputFilename = 'updated.pdf'
pdfOutput = open(pdfOutputFilename, 'wb')
pdfWriter.write(pdfOutput)
pdfOutput.close()
```

9. Close the opened files
```python
pdfFileObj.close()
pdfOutput.close()
```

## Method 2: Using PyMuPDF
We can also use PyMuPDF to add text to an existing PDF. The following steps can be followed.

1. Import the necessary package
```python
import fitz
```

2. Open the PDF file
```python
pdf_file = fitz.open('example.pdf')
```

3. Get the page number
```python
page = pdf_file[0]
```

4. Add text to the page
```python
text = "Hello World!"
textInstance = page.insert_text(fitz.Point(200, 200), text)
```

5. Save the changes to the PDF file
```python
pdf_file.save("updated.pdf")
```

6. Close the opened file
```python
pdf_file.close()
```

## Conclusion
We have seen two methods to add text to an existing PDF using Python. Both PyPDF2 and PyMuPDF are easy to use libraries for creating, modifying, and manipulating PDF files. You can choose the method according to your preference and requirements.
