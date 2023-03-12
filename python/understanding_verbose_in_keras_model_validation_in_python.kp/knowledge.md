---
title: What purpose does the verbose parameter serve in keras when validating the model?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-12 00:00:00
updated_at: 2023-03-12 00:00:00
tldr: Verbose in Keras while validating the model in Python is used to display the progress of the model training and validation process.
---

**Contents**

[TOC]

# What is verbose in Keras?

In Keras, verbose is a parameter that is used to control the verbosity or the amount of information printed during the model fitting or training process. 

# Why is verbose used in Keras?

Verbose is particularly useful in validating and optimizing deep learning models. By setting the verbosity to a specific level, you can observe the training process and the training progress more closely, identify any issues, and fine-tune the performance of your model more accurately. 

# What are the levels of verbosity supported by Keras?

Keras supports three levels of verbosity:

1. **Verbose=0**: This is the default setting; it displays no output during the training process.

2. **Verbose=1**: This displays a progress bar during training, along with training and validation metrics for each epoch.

3. **Verbose=2**: This produces a verbose output for each epoch, displaying the training and validation metrics and progress bar information.

# Conclusion

By setting the verbose level in Keras while training and validating deep learning models, you can control the amount of information displayed during the process and gather the necessary information for optimizing the model's performance.
