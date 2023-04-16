---
title: Instructions on how to install lxml on ubuntu
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Run `pip install lxml` in the terminal to install lxml on Ubuntu in Python.
---

**Contents**

[TOC]

# Section 1: Prerequisites 
Before installing lxml, you will need to install the development packages of libxml2 and libxslt. 

# Section 2: Installation
1. Install the lxml package by running the following command in the terminal: 
   `pip install lxml`
2. Verify that lxml is installed correctly by running the following command in the terminal: 
   `python -c "import lxml; print(lxml.__version__)"`

# Section 3: Additional Steps
If you are using Ubuntu 16.04 or later, you may need to install the following packages:

1. `sudo apt-get install libxml2-dev libxslt-dev python-dev`
2. `sudo apt-get install libxml2 libxslt libxmlsec1`

# Section 4: Troubleshooting
If you encounter any errors during installation or while running lxml, please refer to the [lxml installation documentation](https://lxml.de/installation.html) for troubleshooting tips.
