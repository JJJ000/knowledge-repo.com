---
title: What is the process for extracting text from a pdf file?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: You can use the PyPDF2 library to extract text from a PDF file in Python.
---

**Contents**

[TOC]

#1 Installing Required Libraries

In order to extract text from a PDF file in Python, you will need to install the following libraries: 

- **PyPDF2**: This library enables you to read and write PDF files. 

- **PyMuPDF**: This library enables you to read and extract text from PDF files. 

#2 Opening the PDF File

Once the libraries have been installed, you can open the PDF file with the `open()` function. You can specify the path to the PDF file as an argument. 

#3 Extracting Text from the PDF File

Once the PDF file is opened, you can use the `extractText()` function from the PyMuPDF library to extract the text from the PDF file. This function returns the text as a string. 

#4 Closing the PDF File

Once you have extracted the text from the PDF file, you can use the `close()` function to close the file. This will ensure that the file is not left open and resources are not wasted.
