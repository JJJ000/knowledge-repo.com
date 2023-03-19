---
title: What is the process of verifying a legitimate email address?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: Use a regular expression and the re module to check whether the email address matches the correct format.
---

**Contents**

[TOC]

## Using Regular Expression

One of the most common ways to check for valid email addresses is through regular expressions. Here's an example on how to do it:

```python
import re

def valid_email(email):
    if re.match(r'^\w+([\.-]?\w+)*@\w+([\.-]?\w+)*(\.\w{2,3})+$', email):
        return True
    else:
        return False
```

The regular expression used above is just one of many that can be used to check for a valid email address. This one checks for the most common kinds of email addresses (e.g. `example@domain.com`, `example.name@sub.domain.com`, etc.), but it may not be perfect for every case.

## Using Email Validator Library

Another way to check for valid email addresses is to use the `email-validator` library, which provides a more comprehensive approach. 

To install using pip:

```bash
pip install email-validator
```

Here's an example on how to use the `email-validator` library:

```python
from email_validator import validate_email, EmailNotValidError

def valid_email(email):
    try:
        # Validate.
        valid = validate_email(email)
        # Update with the normalized form.
        email = valid.email
        return True
    except EmailNotValidError:
        # Email not valid.
        return False
```

This method uses the `validate_email` function from the `email-validator` library to check if an email is valid. If it's not valid, an `EmailNotValidError` is raised.

## Using built-in Python library: email.utils

Another way to validate email is using `email.address` module which is a part of built-in Python library. 

To use email module for validating email the prerequisites are:

- The email must have an '@' symbol.
- The email must have a dot(.), indicating the end of the domain section.
- Using these two prerequisites we can validate the email using the below code:

```python
from email.utils import parseaddr

def valid_email(email):
    if '@' not in email:
        return False
    if '.' not in email.split('@')[1]:
        return False
    try:
        parseaddr(email)
        return True
    except:
        return False
```

## Conclusion

These are three ways to check for valid email addresses in Python. Each method has its own advantages and disadvantages, so choose the one that best fits your needs.
