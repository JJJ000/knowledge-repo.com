---
title: What is the process of using Python smtplib to send an email to multiple recipients?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-05 00:00:00
updated_at: 2023-03-05 00:00:00
tldr: Use the `smtplib` library to create an SMTP object and call its `sendmail()` method with a list of recipient email addresses.
---

**Contents**

[TOC]

## Importing necessary modules

The first step is to import necessary modules. We will be using "smtplib" module to send emails and "email" and "email.mime.multipart" modules for email formatting.

```python
import smtplib
from email.mime.multipart import MIMEMultipart
from email.mime.text import MIMEText
```

## Creating email content

Next, we need to create the email content. We will be using "MIMEMultipart" module to create a multipart message that can include both plain text and HTML content. The following code creates an email with subject, sender and message.

```python
msg = MIMEMultipart()
msg['From'] = 'your_email_address'
msg['To'] = ', '.join(['recipient1_email_address', 'recipient2_email_address'])
msg['Subject'] = 'Email subject'

message = 'Email message'
msg.attach(MIMEText(message))
```

## Sending email

Finally, we can send the email using "smtplib" module. We need to provide our email and password for authentication and specify the SMTP server and port.

```python
email = 'your_email_address'
password = 'your_email_password'

server = smtplib.SMTP('smtp.gmail.com', 587)
server.starttls()
server.login(email, password)
text = msg.as_string()
server.sendmail(email, ['recipient1_email_address', 'recipient2_email_address'], text)
server.quit()
```

The above code sends the email to multiple recipients using "server.sendmail" method. We need to provide sender's email address, list of recipients' email addresses and the email content in the form of a string. Finally, we close the connection using "server.quit()" method.
