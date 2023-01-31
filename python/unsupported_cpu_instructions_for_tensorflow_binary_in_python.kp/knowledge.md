---
title: This tensorflow binary was not compiled to use the avx or avx2 instructions that your cpu supports
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-01-30 00:00:00
updated_at: 2023-01-30 00:00:00
tldr: No, Python does not support AVX or AVX2 instructions.
---

**Contents**

[TOC]

Section 1: What is AVX and AVX2?

AVX (Advanced Vector Extensions) and AVX2 are instruction set extensions to the x86 architecture, providing higher performance for certain operations. AVX2 provides a wider range of operations and a larger register size than AVX.

Section 2: What Is TensorFlow?

TensorFlow is an open-source library for numerical computation and machine learning. It is used for deep learning applications such as neural networks.

Section 3: Does TensorFlow Support AVX and AVX2?

TensorFlow does not natively support AVX or AVX2, as it is not compiled to use these instruction sets. However, it is possible to compile TensorFlow to use AVX and AVX2 instructions.

Section 4: How Can I Use AVX and AVX2 with TensorFlow in Python?

In order to use AVX and AVX2 with TensorFlow in Python, you will need to compile TensorFlow from source with the appropriate flags. You can find instructions on how to do this on the TensorFlow website.
