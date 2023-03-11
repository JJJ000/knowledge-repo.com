---
title: What is the process to send an email using django?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-11 00:00:00
updated_at: 2023-03-11 00:00:00
tldr: Email can be sent via Django`s built-in send\_mail() function by importing it from django.core.mail and passing in the necessary arguments.
---

**Contents**

[TOC]

## Installing Required Packages

Before sending email via  Django, make sure the following packages are installed:
- `django` - for creating web applications in Python.
- `django-environ` - for loading environment variables from a `.env` file.
- `django-crispy-forms` - optional package that provides a simple way to create forms in Python.

To install these packages, run the following command in your terminal:
```bash
pip install django django-environ django-crispy-forms
```

## Django Email Configuration

Configure your Django project to use the email backend by updating the `settings.py` file with the following code:

```python
# settings.py

# Email configuration
EMAIL_BACKEND = 'django.core.mail.backends.smtp.EmailBackend'
EMAIL_HOST = 'your-smtp-host'  # e.g. smtp.gmail.com
EMAIL_PORT = 587
EMAIL_USE_TLS = True
EMAIL_HOST_USER = 'your-email-address'
EMAIL_HOST_PASSWORD = 'your-email-password'
```

Replace the placeholders with the appropriate values for your email provider.

## Sending Email in Django

To send email in Django, we first need to import the `send_mail` function from the built-in `django.core.mail` module.

```python
# views.py

from django.core.mail import send_mail

def send_email(request):
    send_mail(
        'Subject here',
        'Here is the message.',
        'sender@example.com',
        ['recipient@example.com'],
        fail_silently=False,
    )
```

The `send_mail` function takes in the following arguments:
- `subject`: The subject of the email.
- `message`: The body of the email.
- `from_email`: The from email address.
- `recipient_list`: A list of recipient email addresses.
- `fail_silently`: If set to `True`, errors during the sending process will be silently ignored.


## Sending HTML-formatted Email in Django

To send HTML-formatted email using Django, you need to make use of the `EmailMultiAlternatives` class instead of the `send_mail` function.

```python
# views.py

from django.core.mail import EmailMultiAlternatives
from django.template.loader import render_to_string

def send_html_email(request):
    subject = 'Subject here'
    from_email = 'sender@example.com'
    to_email = ['recipient@example.com']
    context = {'message': 'Here is the message.'}

    # Plaintext email body
    text_content = render_to_string('email_template.txt', context)
    # HTML email body
    html_content = render_to_string('email_template.html', context)

    # Create the email message
    msg = EmailMultiAlternatives(subject, text_content, from_email, to_email)
    msg.attach_alternative(html_content, "text/html")

    # Send the email
    msg.send()
```

The `EmailMultiAlternatives` takes the same parameters as `send_mail`, but adds an additional parameter, `alternatives`. This should be a list of `(content, mimetype)` tuples that define the various message parts to be sent, such as a plain text version of the message, an HTML version, etc. In this example, we are attaching an HTML email body using the `attach_alternative` method. 

The `render_to_string` function is used to pass context data to the email templates. The first argument is the path to the template relative to your project's root directory, and the second argument is a dictionary of data to pass to the template. The resulting text is returned as a string.
