---
title: What is the distinction between 'same' and 'valid' padding when using tf.nn.max_pool in tensorflow?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-02 00:00:00
updated_at: 2023-02-02 00:00:00
tldr: SAME padding adds padding to the input such that the output size is the same as the input size, while VALID padding does not add any padding to the input.
---

**Contents**

[TOC]

# SAME

The SAME padding option in tf.nn.max_pool means that the output size will be the same as the input size. This is achieved by adding zeros to the edges of the input tensor such that the output size is the same as the input size.

# VALID

The VALID padding option in tf.nn.max_pool means that the output size will be smaller than the input size. This is achieved by not adding any zeros to the edges of the input tensor such that the output size is smaller than the input size.
