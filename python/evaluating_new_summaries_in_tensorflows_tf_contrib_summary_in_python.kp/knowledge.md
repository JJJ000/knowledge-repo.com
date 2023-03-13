---
title: What is the evaluation process for the new tensorflow tf.contrib.summary summaries?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-13 00:00:00
updated_at: 2023-03-13 00:00:00
tldr: The new tf.contrib.summary summaries in TensorFlow are evaluated using a summarized protocol buffer message.
---

**Contents**

[TOC]

# Introduction
TensorFlow is an open source software for numerical computation using data flow graphs. It has become the platform of choice for building and training machine learning models across a wide range of applications. TensorFlow includes a feature called summaries which provides an easy way to record and visualize various aspects of the model’s performance during training. Recently, TensorFlow introduced new summaries called tf.contrib.summary which are evaluated differently compared to the old ones. 

# Overview of tf.contrib.summary
The tf.contrib.summary module is part of TensorFlow's contrib package, which contains experimental or deprecated features that may not be fully supported in the future. The contrib package provides a way to quickly try new features and give feedback to the TensorFlow team. In Tensorflow 2.0 and above, contrib and other high-level APIs have been moved to the tensorflow.compat.v1 package.

The tf.contrib.summary module includes new types of summaries for TensorFlow that can be used to record values during training. These summaries include histograms, scalar values, images, audio, text, and more. Unlike the old summaries, tf.contrib.summary allows for flexible and efficient writing of summaries with support for distributed and asynchronous computation.

# Evaluating tf.contrib.summary Summaries
Evaluation of tf.contrib.summary summaries in Python involves several steps. These are:

1. Importing the Module
The first step is to import the tf.contrib.summary module into the Python environment. This can be done using the following code:

```
import tensorflow as tf
tf.contrib.summary
```
Alternatively, one can use the following code in TensorFlow 2.0 and above:

```
import tensorflow.compat.v1 as tf
tf.contrib.summary
```
This imports the tf module and the tf.contrib.summary module, making the functions in the module accessible in the Python environment.

2. Setting up the Summaries
After importing the module, the next step is to set up the summaries. This involves defining the variables and operations that are to be recorded during training. For example, if one wants to record the loss, accuracy, and gradients during training, the following code can be used:

```
loss_summary = tf.contrib.summary.scalar('loss', loss)
accuracy_summary = tf.contrib.summary.scalar('accuracy', accuracy)
grads_summary = tf.contrib.summary.histogram('gradients', grads)
merged_summary = tf.contrib.summary.merge_all()
```
Here, tf.contrib.summary.scalar is used to record scalar values, tf.contrib.summary.histogram is used to record histograms, and tf.contrib.summary.merge_all is used to merge all summaries into a single operation.

3. Running the Summaries
Once the summaries have been set up, they can be run during training using the following code:

```
with tf.contrib.summary.summary_writer('logdir') as writer:
    for i in range(num_steps):
        # perform training ...
        _, loss_val, accuracy_val, grads_val = sess.run([train_op, loss, accuracy, grads])
        
        # write summaries
        writer.add_summary(sess.run(merged_summary), global_step=i)
```
This code creates a summary writer object and runs summaries for each training step. The summary writer object writes the summaries to a log directory specified in the with statement.

4. Viewing the Summaries
Finally, one can view the summaries using a tool such as TensorBoard, which is included with TensorFlow. TensorBoard is a web-based visualization tool that allows one to view summaries and other aspects of the model’s performance during training. The tool can be started using the following command:

```
tensorboard --logdir=logdir
```
where logdir is the directory where the summaries were written. TensorBoard can be accessed using a web browser by visiting http://localhost:6006. 

# Conclusion
In conclusion, evaluating tf.contrib.summary summaries involves importing the module, setting up the summaries, running the summaries during training, and viewing them using a tool such as TensorBoard. The new summaries provide a flexible and efficient way to record and visualize various aspects of the model’s performance during training.
