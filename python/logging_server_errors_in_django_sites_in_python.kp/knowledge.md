---
title: What is the process for recording server errors on django websites?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: Use Django`s logging framework to log server errors in Python.
---

**Contents**

[TOC]

## Setting Up Logging

The first step to logging server errors in Django is to set up logging. Django comes with logging built-in and the default logging settings can be found in the project's settings.py file. To set up logging, we must create a logger object and specify its settings. Here is an example of basic logging configuration:

```python
import logging

logger = logging.getLogger(__name__)
logger.setLevel(logging.ERROR)

handler = logging.FileHandler('error.log')
handler.setLevel(logging.ERROR)

formatter = logging.Formatter('%(asctime)s - %(levelname)s - %(message)s')
handler.setFormatter(formatter)

logger.addHandler(handler)
```

This creates a logger object that will log messages of level ERROR or higher to an error.log file. The messages are formatted to include a timestamp, level, and message.


## Catching and Logging Exceptions

Once logging is set up, we can catch and log exceptions that occur during execution. In Django, the most common way to catch exceptions is by using middleware. Middleware is a way to add functionality to the request/response processing pipeline. Middleware can be used to catch exceptions and log them. Here is an example of exception-catching middleware:

```python
class ErrorLoggingMiddleware:
    def __init__(self, get_response):
        self.get_response = get_response

    def __call__(self, request):
        try:
            response = self.get_response(request)
        except Exception as e:
            logger.error(str(e))
            response = HttpResponseServerError()

        return response
```

This middleware catches any exception that occurs during processing and logs it using the logger object we created earlier. The response is then set to a 500 error response.


## Viewing Error Logs

Finally, we need a way to view and analyze the error logs. Django comes with a built-in management command called "runserver" that can be used to view logs. By default, runserver logs to the console, but we can redirect the logs to a file. Here's an example:

```shell
python manage.py runserver --noreload > server.log 2>&1
```

This will redirect output to the server.log file. You can then open this file to view the logs. Another option is to use a logging analysis tool like Splunk or ELK to analyze and search logs. These tools can provide more advanced features like alerts, dashboards, and machine learning-based anomaly detection.
