---
title: What causes tensorflow 2 to be significantly slower compared to tensorflow 1?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-08 00:00:00
updated_at: 2023-03-08 00:00:00
tldr: Tensorflow 2 has a more dynamic and flexible graph construction which can introduce performance overhead compared to the static graph in TensorFlow 1.
---

**Contents**

[TOC]

## Introduction
TensorFlow is an open source machine learning (ML) library developed by Google. TensorFlow 1 and TensorFlow 2 are two major versions of the TensorFlow library. TensorFlow 2 was released with the aim of improving user experience and ease of use. However, some users have reported that TensorFlow 2 is much slower than TensorFlow 1, and they are looking for reasons behind this observation. In this article, we will explore some of the possible reasons why TensorFlow 2 might be slower than TensorFlow 1.

## Changes in TensorFlow 2
One of the main reasons behind the performance differences between TensorFlow 1 and TensorFlow 2 is the changes made in the latter. TensorFlow 2 introduced a number of new features and updates, such as the use of eager execution by default, the Keras API for model building, and the removal of the tf.contrib module. These changes were made to improve the ease of use and user experience, but they also had an impact on performance. For example, the use of eager execution by default in TensorFlow 2 can result in slower execution times compared to the graph-based execution in TensorFlow 1.

## Hardware and Software Configuration
Hardware and software configuration could also be a reason why TensorFlow 2 is slower than TensorFlow 1. TensorFlow 2 requires a minimum version of Python 3.6, whereas TensorFlow 1 supports Python 2.7, which is an older version of Python. Python 3.6 introduced some changes, such as the use of asynchronous generators and the introduction of f-strings, which could result in slower execution times on some systems. Additionally, TensorFlow 2 relies heavily on new hardware acceleration features, such as AVX2, which might not be available on older systems.

## Optimization and Compilation
Optimization and compilation could also be factors that contribute to the performance differences between TensorFlow 1 and TensorFlow 2. TensorFlow 2 uses the XLA (Accelerated Linear Algebra) compiler to optimize and compile the computations, which can result in faster execution times. However, the XLA compiler has some limitations, such as limited support for dynamic control flow and the need for specific hardware configurations to achieve optimal performance. Additionally, TensorFlow 2 uses a two-stage optimization process, which can result in slower startup times compared to TensorFlow 1.

## Conclusion
In conclusion, there are several reasons why TensorFlow 2 might be slower than TensorFlow 1, including changes in TensorFlow 2, hardware and software configuration, and optimization and compilation. Users who experience slower performance in TensorFlow 2 can try to optimize their system configuration and experiment with alternative optimization strategies to improve the performance. Ultimately, the choice between TensorFlow 1 and TensorFlow 2 will depend on the user's specific needs and requirements.
