---
title: The excel xlsx file is unsupported, according to the xlrderror from xlrd.biffh
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: Python`s xlrd module can read .xls files but not .xlsx files.
---

**Contents**

[TOC]

## Introduction

The xlrd.biffh.XLRDError is a type of error that occurs when an Excel .xlsx file is not supported in Python. In this article, we will explore the reasons behind this error and discuss possible solutions.

## Reasons for the xlrd.biffh.XLRDError

1. Version Compatibility: One common reason for this error is version compatibility. XLRDError can occur when an older version of xlrd is used to open a file that was created using a newer version of Excel.

2. File Format: Another reason for this error is the file format. XLRDError can occur if the file is not in a compatible format for Python.

3. Dependencies: Sometimes, this error can be caused by missing or incompatible dependencies required by the xlrd package.

## Solutions for the xlrd.biffh.XLRDError

1. Upgrading xlrd Library: If the error is caused by version compatibility, upgrading to the latest version of xlrd may solve the problem.

2. Converting the File Format: If the error is due to the file format, converting the file to a compatible format such as .csv before opening it with Python may help.

3. Checking Dependencies: If the error is caused by missing dependencies, checking the dependencies required by xlrd and ensuring they are installed and compatible with the current version of Python may help.

4. Using Other Libraries: If none of the above solutions work, trying other Python libraries such as openpyxl for opening .xlsx files may be another option.

## Conclusion

XLRDError can occur when an Excel .xlsx file is not supported in Python due to version compatibility, file format, or missing dependencies. Upgrading xlrd, converting the file format, checking dependencies, or trying other libraries such as openpyxl are possible solutions to the error.
