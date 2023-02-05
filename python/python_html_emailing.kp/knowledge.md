---
title: Create html emails using python
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: Yes, it is possible to send HTML emails with Python using the email and smtplib modules.
---

**Contents**

[TOC]

# Using the Email Package
The email package is the standard Python library for constructing, formatting, and sending emails. It provides a simple interface for creating and sending emails with HTML content.

## Setting up the Message
The first step is to create a message object that contains the HTML content and other details such as the sender, recipient, and subject. To do this, the `EmailMessage()` class is used. The HTML content can be included in the message by setting the `set_content()` method to the HTML content.

## Adding Attachments
Attachments such as images, documents, and other files can be added to the message by using the `add_attachment()` method. The method takes the file path as a parameter and adds the file to the message.

## Sending the Message
The message is sent using the `send()` method. The method takes the recipient address as a parameter and sends the message to the specified address.

## Conclusion
The email package provides a simple interface for creating and sending HTML emails with attachments using Python. By following the steps outlined above, it is possible to send HTML emails with Python.
