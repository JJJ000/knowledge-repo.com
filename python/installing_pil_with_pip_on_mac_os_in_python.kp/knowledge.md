---
title: What is the process for using pip to install pil on mac os?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Run `pip install Pillow` in the terminal to install PIL with pip on Mac OS in Python.
---

**Contents**

[TOC]

# Installation Steps
1. Install XCode
2. Install Homebrew
3. Install PIL

## Install XCode
1. Download and install XCode from the App Store. 
2. Open XCode and accept the terms and conditions.

## Install Homebrew
1. Open the Terminal app. 
2. Enter the following command: `/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"`
3. Follow the instructions to install Homebrew.

## Install PIL
1. Open the Terminal app. 
2. Enter the following command: `brew install libtiff libjpeg webp little-cms2`
3. Enter the following command: `pip install Pillow`
4. Enter the following command: `pip install --upgrade Pillow`
