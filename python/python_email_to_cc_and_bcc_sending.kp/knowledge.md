---
title: How to send an email with to, cc, and bcc in python?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-13 00:00:00
updated_at: 2023-03-13 00:00:00
tldr: To send an email with TO, CC, and BCC using Python, you can use the built-in smtplib library and specify the recipients in the appropriate fields of the message object.
---

**Contents**

[TOC]

## Setting up the email message

To send email with TO, CC and BCC, we first need to create an email message with email addresses as recipients. We start by importing the necessary libraries and setting up the email message. 

```python
import smtplib
from email.message import EmailMessage

msg = EmailMessage()
msg['Subject'] = 'Subject of the email'
msg['From'] = 'sender@domain.com'
msg['To'] = 'recipient1@domain.com, recipient2@domain.com'
msg['Cc'] = 'cc1@domain.com'
msg['Bcc'] = 'bcc1@domain.com'
```

In the above code block, we import the smtplib library to send email and EmailMessage class to create an email message. We set the email subject, sender, recipient as TO, CC and BCC. 

## Setting up the email body

Next, we add the email body as plain text or HTML. 

```python
msg.set_content('Hello, \nThis is the message body.')
```

We can also add an HTML email body using the following code: 

```python
msg.add_alternative("""
    <!DOCTYPE html>
    <html>
        <body>
            <p>Hello,</p>
            <p>This is the HTML message body.</p>
        </body>
    </html>
""", subtype='html')
```

## Sending the email

To send the email, we need to connect to an SMTP server and authenticate the sender before sending the message. 

```python
with smtplib.SMTP('smtp.gmail.com', port=587) as smtp:
    smtp.ehlo()
    smtp.starttls()
    smtp.login('sender@domain.com', 'password')
    smtp.send_message(msg)
```

In this code block, we connect to the Gmail SMTP server with port number 587. We use `ehlo()` to greet the server and `starttls()` to encrypt the connection before authenticating the sender's email address and password. We finally use the `send_message()` method to send the email message.

## Conclusion

By following the above steps, we can send an email with TO, CC, and BCC recipients using Python.
