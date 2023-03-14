---
title: How can I resolve the error "tesseractnotfound error tesseract is either not installed or not in the path" in pytesseract?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-14 00:00:00
updated_at: 2023-03-14 00:00:00
tldr: Install tesseract on your system and add its path to the environment variables.
---

**Contents**

[TOC]

## Introduction

When working with the Pytesseract library in Python, you may encounter the error message "TesseractNotFound Error: tesseract is not installed or it's not in your path". This error occurs when the Pytesseract library is unable to locate the Tesseract OCR engine on your machine. In this tutorial, we will explore several ways to fix this issue.

## Solution 1: Install Tesseract OCR Engine

The first solution to the "TesseractNotFound Error" is to install the Tesseract OCR engine on your machine. You can download the Tesseract OCR engine from the official website and follow the installation instructions provided. Alternatively, you can install Tesseract OCR engine using the following command in your terminal:

```bash
sudo apt-get install tesseract-ocr
```

Once Tesseract OCR engine is installed on your machine, make sure to specify the path to the executable file when using Pytesseract as follows:

```python
import pytesseract
pytesseract.pytesseract.tesseract_cmd = '/usr/bin/tesseract'
```

## Solution 2: Add Tesseract OCR Engine to the PATH Variable

Another solution to resolving the TesseractNotFound error is to add the Tesseract OCR engine to the PATH variable. The PATH variable is a system variable that contains a list of folders that your operating system searches when running commands in the terminal. 

To add Tesseract OCR engine to the PATH variable, you need to identify the directory where the Tesseract OCR engine is installed and append it to the PATH variable using the following command:

```python
import os
os.environ['PATH'] += ':/usr/local/bin'
```

If Tesseract OCR engine is installed in a different directory, make sure to specify the correct path.

## Solution 3: Specify the Tesseract OCR Engine Location

If the first two solutions do not work, you can specify the location of the Tesseract OCR engine when calling Pytesseract in your Python code. 

```python
import pytesseract
pytesseract.pytesseract.tesseract_cmd = '/path/to/your/tesseract'
```

Ensure to replace /path/to/your/tesseract with the actual path to the Tesseract OCR engine on your machine.

## Conclusion

In summary, the TesseractNotFound error message is an indication that Pytesseract is unable to locate the Tesseract OCR engine on your machine. We have explored three possible solutions to fix this issue, including installing Tesseract OCR engine on your machine, adding it to the PATH variable, or specify the location of the Tesseract OCR engine when calling Pytesseract.
