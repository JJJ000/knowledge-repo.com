---
title: What is the method for determining if tensorflow is utilizing gpu acceleration when working in a Python shell?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-02 00:00:00
updated_at: 2023-02-02 00:00:00
tldr: You can use the tf.test.is\_gpu\_available() function to check if TensorFlow is using GPU acceleration.
---

**Contents**

[TOC]

# Section 1 - Check Device List

In the Python shell, you can check if TensorFlow is using GPU acceleration by checking the list of devices it has available. To do this, you can use the command `tf.config.list_physical_devices('GPU')`. This will return a list of available GPUs. If the list is empty, then TensorFlow is not using GPU acceleration. 

# Section 2 - Check Logs

Another way to check if TensorFlow is using GPU acceleration is to look at the logs. TensorFlow will log information about the devices it is using. To view the logs, you can use the command `tf.get_logger().info('List of devices: %s', tf.config.list_physical_devices('GPU'))`. This will print out the list of devices that TensorFlow is using. If the list contains a GPU, then TensorFlow is using GPU acceleration. 

# Section 3 - Check Operations

A third way to check if TensorFlow is using GPU acceleration is to look at the operations that are being performed. If the operations are being performed on a GPU, then TensorFlow is using GPU acceleration. To check this, you can use the command `tf.debugging.set_log_device_placement(True)`. This will print out information about the devices that are being used for each operation. 

# Section 4 - Check Performance

Finally, you can check if TensorFlow is using GPU acceleration by looking at the performance of your model. If the model is running faster than expected, then it is likely that TensorFlow is using GPU acceleration. To check this, you can use the command `tf.test.is_gpu_available()`. This will return a boolean value that indicates whether or not TensorFlow is using GPU acceleration.
