---
title: Routing to a specific url in flask
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: In Flask, you can redirect to a URL using the redirect() function.
---

**Contents**

[TOC]

#### Redirecting

Flask provides a function called `redirect()` which redirects the user to a specified URL with a response of HTTP status code `302`. The syntax for using this function is as follows:

`return redirect(url_for('endpoint'))`

Where `url_for()` is a function that generates the URL for a given endpoint.

#### Arguments

The `redirect()` function accepts two arguments: `location` and `statuscode`. The `location` argument is the URL to be redirected to, and the `statuscode` argument is the HTTP status code. The default value of the `statuscode` argument is `302`.

#### Example

The following code snippet shows an example of how to use the `redirect()` function:

```
@app.route('/redirect')
def redirect_example():
    return redirect(url_for('endpoint'), code=302)
```

#### Additional Notes

The `redirect()` function can also be used to redirect to an external URL by passing the URL as a string instead of the `url_for()` function. For example:

`return redirect('https://www.example.com')`
