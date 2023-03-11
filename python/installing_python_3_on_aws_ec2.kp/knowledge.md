---
title: What is the process of installing Python 3 on an aws ec2 instance?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-11 00:00:00
updated_at: 2023-03-11 00:00:00
tldr: To install Python 3 on an AWS EC2 instance, run the command `sudo yum install python3` in the terminal.
---

**Contents**

[TOC]

# Introduction 

Amazon Web Services (AWS) Elastic Compute Cloud (EC2) provides users with virtual machines that can be used as a platform to run various applications. Python 3 is not pre-installed on EC2 instances, but it is easy to install. In this tutorial, we will walk through the steps to install Python 3 on an AWS EC2 instance.

## Step 1: Launch an EC2 Instance

The first step is to launch an EC2 instance. When launching an instance, you need to choose the Amazon Machine Image (AMI) on which the instance will be based. Once you have launched an instance, you can log in and begin installing Python 3.

## Step 2: Update the System

Before installing Python 3, it is important to ensure that the system is up-to-date. This can be done using the following command:

```
sudo yum update
```

## Step 3: Install Python 3

Now that the system is up-to-date, we can install Python 3. This can be done using the following command:

```
sudo yum install python3
```

If prompted to confirm, type 'y' and press Enter.

## Step 4: Verify Python 3 Installation

To verify that Python 3 is installed correctly, we can check the version of Python. This can be done using the following command:

```
python3 -V
```

This should return the version number of Python 3 that was installed.

# Conclusion

In this tutorial, we have seen how to install Python 3 on an AWS EC2 instance. We first launched an instance and then updated the system before installing Python 3. Lastly, we verified that Python 3 was installed correctly by checking the version number. Once Python 3 is installed, users can then use the EC2 instance to run Python applications.
