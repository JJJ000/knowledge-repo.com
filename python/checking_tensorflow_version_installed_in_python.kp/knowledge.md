---
title: What version of tensorflow is installed on my system?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: You can use the tf.version.VERSION attribute to find the version of TensorFlow installed in your system.
---

**Contents**

[TOC]

# Section 1: Using pip

1. Open the command prompt on your Windows system and type `pip list`
2. This will list all the packages installed by pip.
3. Look for the TensorFlow package and note down the version number associated with it.

# Section 2: Using TensorFlow

1. Open the Python interpreter in your system.
2. Import the TensorFlow library using `import tensorflow as tf`
3. To check the version of TensorFlow installed, use `tf.__version__`
4. The output will be the version of TensorFlow installed in your system.
