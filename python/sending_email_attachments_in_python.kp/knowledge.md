---
title: What is the process for attaching files to an email?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: Use the built-in email package in Python to send email attachments.
---

**Contents**

[TOC]

# Section 1: Setting up the SMTP Server

The Simple Mail Transfer Protocol (SMTP) is a protocol used for sending emails. To send an email with attachments in Python, you need to use the smtplib module. This module defines an SMTP client session object that can be used to send mail to any Internet machine with an SMTP or ESMTP listener daemon.

# Section 2: Sending the Email

Once you have set up the SMTP server, you can use the sendmail() method to send the email. This method takes three parameters: the sender's email address, the recipient's email address, and the message body. The message body should include the email subject, the email body text, and the attachments.

# Section 3: Attaching the Files

To attach files to the email, you need to use the MIME (Multipurpose Internet Mail Extensions) library. The MIME library allows you to encode the files into base64 format, which can then be attached to the email.

# Section 4: Sending the Email

Once the attachments have been encoded and attached to the email, you can use the sendmail() method to send the email. This method takes three parameters: the sender's email address, the recipient's email address, and the message body. Once the email has been sent, the SMTP server will close the connection.
