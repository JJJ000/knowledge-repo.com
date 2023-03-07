---
title: An attributeerror occurred in tensorflow 2.0 with the message "module 'tensorflow' has no attribute 'session'."
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-07 00:00:00
updated_at: 2023-03-07 00:00:00
tldr: TensorFlow 2.0 doesn`t support the use of tf.Session() anymore and instead relies on the use of eager execution.
---

**Contents**

[TOC]

# Introduction
One possible reason why you might encounter the "AttributeError: module 'tensorflow' has no attribute 'Session'" error message in Python when working with Tensorflow 2.0 is that the older version of Tensorflow was installed on your system, and you are trying to use programming code that was written for an older version of Tensorflow that included the `Session` attribute. In Tensorflow 2.0, the `Session` attribute has been removed, and a new eager execution mode has been introduced instead. This can lead to some confusion and compatibility issues when upgrading to Tensorflow 2.0 from an older version.

# Solution
To resolve the "AttributeError: module 'tensorflow' has no attribute 'Session'" error message in Tensorflow 2.0, you need to modify your code to use the new eager execution mode instead of relying on the `Session` attribute. The eager execution mode allows you to execute Tensorflow operations immediately as they are called, without the need to build a static graph or use a session to execute the graph. You can enable eager execution mode by adding the following line at the beginning of your code: 

```
import tensorflow as tf
tf.compat.v1.enable_eager_execution()
```

# Example
Here is an example that demonstrates how to modify a simple Tensorflow code snippet that relies on the `Session` attribute to use eager execution mode instead:

```
import tensorflow as tf

# create a Tensorflow constant
a = tf.constant(2)
b = tf.constant(3)

# create a session
# sess = tf.Session()  # replace this line with the lines below to enable eager execution mode
tf.compat.v1.enable_eager_execution()

# print the result of the multiplication operation
# print(sess.run(a * b))  # replace this line with the line below to enable eager execution mode
print(a * b)
```

By replacing the `Session` object with eager execution mode, you can run Tensorflow operations directly as part of your normal program flow, without the need to create a graph or use a session to execute the operations.

# Conclusion
The "AttributeError: module 'tensorflow' has no attribute 'Session'" error message in Python can be resolved by modifying your code to use the new eager execution mode introduced in Tensorflow 2.0, instead of relying on the `Session` attribute that was present in older versions of Tensorflow. By enabling eager execution mode and running Tensorflow operations directly as part of your program flow, you can take advantage of the new features and benefits introduced in Tensorflow 2.0.
