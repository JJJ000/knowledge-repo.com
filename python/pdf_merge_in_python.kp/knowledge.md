---
title: Combine pdf documents
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: To merge PDF files in Python, use the PyPDF2 library.
---

**Contents**

[TOC]

Section 1: Introduction
-----------------------
In this tutorial, we will discuss how to merge two or multiple PDF files into a single PDF file using Python. We will use the PyPDF2 library to perform this task. PyPDF2 is a pure-python library that can be used to manipulate PDF files. It allows you to merge, split, crop, encrypt, and decrypt PDF files.

Section 2: Installing PyPDF2 library
------------------------------------
Before we begin, we need to install the PyPDF2 library. You can install it using pip by running the following command in your terminal.

```python
pip install PyPDF2
```

Section 3: Merging PDF files
----------------------------
Once you have installed the PyPDF2 library, you can start merging PDF files. We will create a function that takes a list of PDF file names as input and merges them into a single PDF file. Here's the Python code for merging PDF files:

```python
import PyPDF2

def merge_pdfs(pdfs, output):
    merger = PyPDF2.PdfFileMerger()
    for pdf in pdfs:
        merger.append(pdf)
    merger.write(output)
```

In the above code, we import the PyPDF2 library and define a function `merge_pdfs` that takes two arguments: a list of PDF file names and the name of the output PDF file. We then create a `PdfFileMerger` object and loop through the list of PDF files, appending each one to the merger object. Finally, we write the merged PDF file to disk.

Section 4: Running the code
---------------------------
To run this code, you need to provide a list of PDF files that you want to merge and the name of the output PDF file. Here's how you can use the `merge_pdfs` function:

```python
pdfs = ["file1.pdf", "file2.pdf", "file3.pdf"]
merge_pdfs(pdfs, "merged.pdf")
```

In the above code, we provide a list of PDF files `file1.pdf`, `file2.pdf`, `file3.pdf` and specify the output file name `merged.pdf`. The `merge_pdfs` function will merge these PDF files into a single PDF file named `merged.pdf`.

Conclusion
----------
In this tutorial, we learned how to merge multiple PDF files into a single PDF file in Python using the PyPDF2 library. We created a function that takes a list of PDF file names as input and merges them into a single PDF file. The PyPDF2 library provides many other functionalities to manipulate PDF files such as splitting, cropping, encrypting, and decrypting PDF files.
