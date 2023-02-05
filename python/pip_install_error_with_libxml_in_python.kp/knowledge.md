---
title: Error when attempting to install libxml using pip
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: Pip cannot install libxml due to missing build dependencies.
---

**Contents**

[TOC]

# Solution 1: Install libxml Using apt-get
1. Open the terminal and type `sudo apt-get install libxml2-dev libxslt-dev python-dev`
2. Enter your password when prompted
3. Wait for the installation to complete

# Solution 2: Install libxml Using pip
1. Open the terminal and type `pip install lxml`
2. Wait for the installation to complete
