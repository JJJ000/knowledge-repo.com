---
title: Generate urls that are dynamic using flask's url_for() method
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: The url\_for() function in Flask allows us to create dynamic URLs by referencing the function name that handles the specific request.
---

**Contents**

[TOC]

# Introduction

URLs serve as important identifiers for webpages and resources on the internet. In Flask, `url_for()` is a powerful function that can be used to create dynamic, or dynamic, URLs that allow website pages to be navigated, linked and structured more efficiently.


# Basic Usage

To use `url_for()` in Flask, you first need to import the function from the Flask package as shown below:

```python
from flask import Flask, url_for
```

Once you have imported the function, you can use it to create URLs dynamically by using the name of the function or URL rule that handles the specified route. 

```python
@app.route('/user/<username>')
def show_user_profile(username):
  return 'User %s' % username

with app.test_request_context():
  print(url_for('show_user_profile', username='JohnDoe'))
```

The output of the above code will be a dynamic URL for the user 'JohnDoe':

```python
/user/JohnDoe
```

This URL can be included in a hyperlink tag in HTML, or used as a GET request to access data stored on the server.

# Advanced Usage

In addition to using `url_for()` to generate simple URLs, you can also use the function to generate more complex URLs that include variables or URL-specific parameters. One such example is using `url_for()` to generate URLs for static files like images, JavaScript files, and CSS files. 

```python
img_file = 'mypicture.png'
url = url_for('static', filename='images/' + img_file)
```

The output of the above code will be a URL for the `mypicture.png` file located in a subdirectory called `images` in the `static` directory.

```python
/static/images/mypicture.png
```

You can also use `url_for()` along with other Flask functions to generate more complex URLs such as those including a GET parameter:

```python
with app.test_request_context():
  url = url_for('login', next='/')
  print(url)
```

In the above code, `url_for()` is used to generate a URL pointing to the `login` view function while also passing a GET parameter `next` with value `/`. 

```python
/login?next=%2F
```

# Conclusion

With `url_for()`, Flask makes it easy to create dynamic URLs that provide a more structured approach to navigating and linking webpages. The function is extremely flexible and can be used to generate simple to complex URLs in addition to URLs for static files and GET parameters. Ultimately, `url_for()` is a powerful tool that can help improve the readability, usability, and maintainability of websites built with Flask.
