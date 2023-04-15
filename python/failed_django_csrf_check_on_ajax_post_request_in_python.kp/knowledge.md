---
title: The csrf check in django is not successful when an ajax post request is made
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-17 00:00:00
updated_at: 2023-04-17 00:00:00
tldr: Add the CSRF token value from the cookie as a header in your AJAX POST request.
---

**Contents**

[TOC]

# Introduction
Django is a high-level web framework that follows the model-view-template (MVT) architectural pattern. It is designed to assist developers in the smooth creation, deployment, and maintenance of complex web applications. Django's security features include Cross-Site Request Forgery (CSRF) protection, which is essential to prevent unauthorized access and data tampering. Ajax POST requests can sometimes fail CSRF checks in Django, even though they may be properly configured. This article explores some possible reasons for this issue and how to fix it.

# Reason for CSRF Failure in Ajax POST Requests
When making an Ajax POST request in Django, the CSRF token must be included in the request headers for the server to verify its authenticity. Failing to include the CSRF token results in a "CSRF verification failed" error message. However, there are several reasons why the CSRF token may not be included in the headers, leading to a failure in CSRF checks. Some of these reasons include:
- Having an outdated or improperly configured Django version
- Incorrectly implementing the CSRF token in the client-side code
- Submitting the form via JavaScript without including the CSRF token in the headers
- Using third-party tools or libraries that do not handle CSRF protection correctly

# Fixing CSRF Failure in Ajax POST Requests
To fix CSRF failure in Ajax POST requests in Django, consider the following solutions:
### Solution 1: Updating Django Version
Ensure that your Django version is up-to-date and correctly configured to handle CSRF protection. Upgrading to a newer version of Django may solve some of the CSRF-related issues.

### Solution 2: Ensuring CSRF Token Inclusion in Client-side Code
To ensure that the CSRF token is included in the headers of an Ajax POST request, add the following line of code to the JavaScript function handling the POST request:
```javascript
headers: { "X-CSRFToken": document.getElementsByName("csrfmiddlewaretoken")[0].value }
```
This code will get the value of the CSRF token and include it in the request headers as "X-CSRFToken".

### Solution 3: Including CSRF Token in JavaScript Form Submit
Ensure that the CSRF token is included in the headers when submitting the form via JavaScript. To do this, add the following code snippet before the form submission:
```javascript
var form = document.getElementById("my-form-id");
var csrf = document.getElementsByName("csrfmiddlewaretoken")[0].value;
form.action = "/my-url/";
form.method = "POST";
form.enctype = "multipart/form-data"; // if the form contains file inputs
var input = document.createElement("input");
input.type = "hidden";
input.name = "csrfmiddlewaretoken";
input.value = csrf;
form.appendChild(input);
form.submit();
```
This code creates a hidden input field and generates a CSRF token value that gets added to the form data when submitting it via JavaScript.

### Solution 4: Using Third-party Tools with Correct CSRF Handling
When using third-party tools or libraries that submit Ajax POST requests, ensure they have appropriate CSRF protection, or handle the protection in your Django application manually. Most third-party libraries offer options to include or exclude CSRF protection. 

# Conclusion
CSRF checks are essential for securing Django web applications from unauthorized access and data tampering. Ajax POST requests can sometimes fail CSRF checks, leading to CSRF verification errors. This article offers some possible reasons for this error and how to fix them. When working with Django's CSRF protection, always make sure to follow best practices for secure web development.
