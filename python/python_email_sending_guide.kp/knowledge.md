---
title: What is the process for sending an email using python?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: To send an email with Python, you can use the built-in SMTP library or a third-party library such as smtplib.
---

**Contents**

[TOC]

# Introduction
Python provides built-in and third-party libraries for sending email. The `smtplib` module is the standard library for sending email using Simple Mail Transfer Protocol (SMTP). The `email` module is a library for constructing and formatting email messages. In this tutorial, we'll look at how to send an email using Python and the `smtplib` and `email` modules.

# Setting Up SMTP Server and Email Account
Before we can send an email, we need an SMTP server to send the email from and an email account to send the email with. There are many SMTP servers available, including Gmail, Yahoo, and Hotmail. In this tutorial, we'll use Gmail as our SMTP server.

To use Gmail as an SMTP server, we need to enable less secure apps in our Google account. 

1. Go to your Google account settings and click on Security.

2. Scroll down to Less secure app access and turn it on.

3. Next, we need to get our SMTP server details. The SMTP server for Gmail is `smtp.gmail.com` and it uses port 465 with SSL or port 587 with TLS.

4. Finally, we need to create an email account to send the email from. If you already have a Gmail account, you can use that. Otherwise, you can create a new Gmail account.

# Sending Email with smtplib and email
Now that we have our SMTP server details and email account set up, we can proceed to send an email using Python. 

First, we need to import the necessary modules:

```python
import smtplib
from email.message import EmailMessage
```

Next, we need to create an email message:

```python
msg = EmailMessage()
msg['Subject'] = 'Subject line'
msg['From'] = 'sender@example.com'
msg['To'] = 'recipient@example.com'
msg.set_content('Body of the email')
```

In the code above, we create an `EmailMessage` object and set the subject, sender, recipient, and body of the email.

Next, we need to connect to the SMTP server and send the email:

```python
with smtplib.SMTP_SSL('smtp.gmail.com', 465) as smtp:
    smtp.login('sender@example.com', 'password')
    smtp.send_message(msg)
```

In the code above, we use the `smtplib.SMTP_SSL()` method to connect to the SMTP server and login to the email account using the sender's email address and password. We then use the `smtp.send_message()` method to send the email message.

# Conclusion
Sending email using Python is a simple task using the `smtplib` and `email` modules. We first need to set up an SMTP server and email account to send the email from. We then create an email message using the `EmailMessage` class and send the email using the `smtplib` module.
