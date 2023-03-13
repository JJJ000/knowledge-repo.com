---
title: The gmail smtp is not accepting the login credentials
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-13 00:00:00
updated_at: 2023-03-13 00:00:00
tldr: The likely cause of login credentials not working with Gmail SMTP in Python is incorrect login information, security settings, or two-factor authentication.
---

**Contents**

[TOC]

Section 1: Introduction
In Python, we can use the Simple Mail Transfer Protocol (SMTP) module to send emails programmatically. Gmail is one of the most popular email services, so many people use it as an SMTP server. However, sometimes login credentials might not work with Gmail SMTP in Python. In this guide, we will explore some possible causes and solutions.

Section 2: Check the credentials
The first thing to check is whether the login credentials are correct. Double-check that the email address and password are correct and have not been changed recently. It might also be helpful to try logging in to the Gmail account from a web browser to ensure that there are no login issues at the source.

Section 3: Enable less secure apps
If the login credentials are correct and the issue persists, the next thing to check is whether less secure apps are enabled in the Gmail account. Gmail considers emails sent via SMTP as less secure, so it disables this functionality by default. To enable less secure apps, go to the Gmail account settings and navigate to the "Security" tab. Scroll down to the "Less secure app access" section and turn it on.

Section 4: Use two-factor authentication (2FA)
If enabling less secure apps does not fix the issue, the Gmail account might have two-factor authentication (2FA) enabled. In this case, an app password is required to access Gmail via SMTP. To create an app password, go to the Gmail account settings and navigate to the "Security" tab. Under the "Signing in to Google" section, click on "App passwords". Follow the instructions to create a new app password specifically for Python or the SMTP library being used. Use this app password as the password when connecting to the Gmail SMTP server.

Section 5: Conclusion
In conclusion, if the login credentials are not working with Gmail SMTP in Python, it could be due to incorrect credentials, disabled less secure apps, or two-factor authentication. By double-checking the credentials, enabling less secure apps, or creating an app password for 2FA, we can ensure that we can send emails programmatically using Gmail SMTP.
