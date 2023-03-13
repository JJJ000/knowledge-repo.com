---
title: The tensorflow installation without gpu support is unable to load the dynamic library 'cudart64_101.dll'
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-13 00:00:00
updated_at: 2023-03-13 00:00:00
tldr: The error message indicates that there is an attempt to load a CUDA library (cudart64\_101.dll) on a TensorFlow installation without GPU support.
---

**Contents**

[TOC]

## How to install TensorFlow CPU-only?

If you want to use TensorFlow without GPU support, then you can install the CPU-only version. This version does not require a GPU, but it can still provide impressive performance on many tasks.

Here are the steps to install TensorFlow CPU-only:

1. Ensure that you have Python 3.5-3.8 installed on your system.

2. Create a new virtual environment (optional but recommended) and activate it:

```bash
python3 -m venv tf_cpu
source tf_cpu/bin/activate
```

3. Install TensorFlow CPU-only via pip:

```bash
pip install tensorflow-cpu
```

4. Verify that TensorFlow is installed correctly by running the following Python code:

```python
import tensorflow as tf
print(tf.__version__)
```

If all goes well, you should see the version number of TensorFlow that you just installed.

## What is cudart64_101.dll?

cudart64_101.dll is a dynamic link library (DLL) file that is used by CUDA, a toolkit for programming GPUs from NVIDIA. This DLL provides functions that are needed by CUDA applications to communicate with the CPU and other CUDA devices.

## Why is cudart64_101.dll causing an error on TensorFlow CPU-only installation?

If you see an error message like "Could not load dynamic library 'cudart64_101.dll'" when you try to import TensorFlow in Python, it means that TensorFlow is looking for this DLL file but cannot find it.

This error occurs because TensorFlow is compiled with support for CUDA, even though you have installed the CPU-only version. When TensorFlow tries to load the CUDA library, it fails because there is no GPU and therefore no CUDA device available.

## How to fix the cudart64_101.dll error in TensorFlow CPU-only installation?

There are a few ways to fix this error:

1. Install the GPU version of TensorFlow: If you have a compatible NVIDIA GPU and the necessary CUDA drivers installed, you can install the GPU version of TensorFlow instead of the CPU-only version. This will allow TensorFlow to use the GPU and access the cudart64_101.dll library.

2. Uninstall TensorFlow and install the CPU-only version: If you do not need GPU support, then you can uninstall TensorFlow and install the CPU-only version instead. This version does not require the CUDA library and therefore will not look for the cudart64_101.dll file.

3. Ignore the error message: If you do not plan to use GPU support, you can simply ignore the error message. It should not affect the functionality of TensorFlow for CPU-only tasks. However, you may want to suppress the error messages by setting the following environment variable before importing TensorFlow:

```bash
export TF_CPP_MIN_LOG_LEVEL=2
```

This will reduce the log level and prevent some warning messages from being displayed.
