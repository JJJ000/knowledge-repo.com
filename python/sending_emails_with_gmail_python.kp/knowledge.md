---
title: What is the process for sending an email with gmail as the provider using python?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: Use the smtplib module to connect to the Gmail SMTP server and send the email.
---

**Contents**

[TOC]

## Section 1: Connecting to Gmail

Using the [Python Standard Library's smtplib](https://docs.python.org/3/library/smtplib.html), you can connect to Gmail's SMTP server and send emails.

To connect to Gmail, you will need to use the [Gmail SMTP server](https://support.google.com/a/answer/176600?hl=en) address: `smtp.gmail.com` and port `587`.

## Section 2: Setting up Authentication

To authenticate with Gmail's SMTP server, you will need to provide a username and password. This is done using the [SMTP.login method](https://docs.python.org/3/library/smtplib.html#smtplib.SMTP.login).

You will also need to enable [Less Secure Apps](https://myaccount.google.com/lesssecureapps) in your Google Account settings in order for the authentication to work.

## Section 3: Sending an Email

Once you have connected to Gmail's SMTP server and authenticated, you can send an email using the [SMTP.sendmail method](https://docs.python.org/3/library/smtplib.html#smtplib.SMTP.sendmail).

This method takes three parameters: the sender's email address, the recipient's email address, and the message body.

## Section 4: Disconnecting

Once you have sent the email, you should disconnect from the server using the [SMTP.quit method](https://docs.python.org/3/library/smtplib.html#smtplib.SMTP.quit). This will ensure that the connection is closed properly.
