---
title: Django generates a bad request (400) error when the debug mode is set to false
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-05 00:00:00
updated_at: 2023-03-05 00:00:00
tldr: When DEBUG = False in Django, it does not give detailed error messages and instead gives a generic `Bad Request (400)` error.
---

**Contents**

[TOC]

Section 1: Introduction
In Django, the DEBUG option in the settings file controls whether the application is in debug mode or not. Debug mode is enabled by default, which allows for useful error messages to be displayed in the browser. However, in production environments, it is recommended to set DEBUG to False to prevent sensitive information from being leaked.

Section 2: The cause of Bad Request (400)
When DEBUG = False, Django's default behavior is to not display detailed error messages to the user. Instead, a generic "Bad Request (400)" error message is shown. This is because Django does not want to reveal potentially sensitive information, such as the application's settings or implementation details, to the user.

Section 3: How to handle Bad Request (400)
To handle Bad Request (400) error messages in Django, it is recommended to implement a custom error view. This view can display a more user-friendly message or redirect the user to a different page. To do this, you can define a handler for the 400 error code in the urls.py file like this:

```
handler400 = 'myapp.views.my_custom_bad_request_view'
```

Here, 'myapp.views.my_custom_bad_request_view' is the name of the view function that you want to handle the 400 error code. 

Section 4: Conclusion
When DEBUG = False, Django defaults to displaying a generic "Bad Request (400)" error message to prevent sensitive information from being leaked. To handle this error message, it is recommended to implement a custom error view that either displays a more user-friendly message or redirects the user to a different page.
