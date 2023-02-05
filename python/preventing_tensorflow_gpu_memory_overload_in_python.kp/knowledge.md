---
title: What is the best way to avoid tensorflow from using all of the gpu memory?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: Set the TensorFlow GPU memory fraction using the `tf.GPUOptions.per\_process\_gpu\_memory\_fraction` parameter.
---

**Contents**

[TOC]

1. Configure the GPU Memory Allocation
-------------------------------------
The memory allocation of a GPU can be configured in TensorFlow using the per_process_gpu_memory_fraction argument of the tf.ConfigProto() function. This argument takes a float value between 0 and 1, representing the fraction of the total GPU memory that TensorFlow should allocate. By setting this value to a lower number, TensorFlow will only allocate a portion of the total GPU memory, preventing it from allocating the totality of the GPU memory.

2. Configure the Logical Devices
--------------------------------
TensorFlow also allows for the configuration of logical devices, which can be used to limit the amount of memory allocated to a specific operation. This can be done by using the log_device_placement argument of the tf.ConfigProto() function. This argument takes a boolean value that indicates whether or not to log every operation’s device placement. By setting this value to True, TensorFlow will log the device placement of each operation and allow for the configuration of logical devices.

3. Use GPU Memory Growth
------------------------
TensorFlow also provides a way to prevent the allocation of the totality of a GPU memory by using the allow_growth argument of the tf.ConfigProto() function. This argument takes a boolean value that indicates whether or not to allocate only as much GPU memory as needed by the runtime operations of the TensorFlow graph. By setting this value to True, TensorFlow will only allocate the amount of GPU memory needed by the operations, preventing it from allocating the totality of the GPU memory.

4. Use the GPU Memory Fraction
------------------------------
Finally, TensorFlow provides the GPU memory fraction argument of the tf.ConfigProto() function. This argument takes a float value between 0 and 1, representing the fraction of the total GPU memory that TensorFlow should allocate. By setting this value to a lower number, TensorFlow will only allocate a portion of the total GPU memory, preventing it from allocating the totality of the GPU memory.
