---
title: The task of (run example) was received by celery, but it was not registered
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-17 00:00:00
updated_at: 2023-03-17 00:00:00
tldr: You need to register the `run example` task with Celery using the @app.task decorator.
---

**Contents**

[TOC]

Section 1: Background

Before delving into the solution, let's first understand the problem. Celery is a task queue system that lets you distribute asynchronous tasks across worker nodes. It allows you to divide your code into smaller, reusable units of work known as tasks. These tasks can be executed in the background, while your application continues to respond to user requests. 

When working with Celery, you might encounter the error message "Received unregistered task of type." This means that Celery has received a task that it doesn't recognize or hasn't been registered. The error message usually includes the name of the task that Celery is trying to execute. In this case, the task is "run example." 


Section 2: Solution

The solution to this problem is quite simple. Celery needs to know about all the tasks that you plan to execute, so it can register them before they are executed. If Celery receives a task that hasn't been registered, it will raise an exception. 

To register a task with Celery, you need to define a task function and add a decorator that tells Celery to register the task. Here's an example: 

```python
from celery import Celery

app = Celery('tasks', broker='pyamqp://guest@localhost//')

@app.task
def add(x, y):
    return x + y
```

In this example, we define a task function named "add" and decorate it with "@app.task". This tells Celery to register the "add" task. When Celery receives a task with the name "add", it will execute this function. 

To solve the "Received unregistered task" error message, you need to define the "run example" task and register it with Celery. Here's an example: 

```python
from celery import Celery

app = Celery('tasks', broker='pyamqp://guest@localhost//')

@app.task
def run_example():
    # your code here
    pass
```

In this example, we define a task function named "run_example" and decorate it with "@app.task". This tells Celery to register the "run_example" task. When Celery receives a task with the name "run_example", it will execute this function. 


Section 3: Registering tasks dynamically

If you have a large number of tasks, registering them manually can become tedious. Celery provides a way to dynamically register tasks by discovering all the task functions in a particular module or package. Here's an example: 

```python
from celery import Celery

app = Celery('tasks', broker='pyamqp://guest@localhost//')

app.autodiscover_tasks(['tasks'])
```

In this example, we use the "autodiscover_tasks" method to discover all task functions in a module named "tasks". This method will automatically register all task functions that are decorated with "@app.task" in the "tasks" module. 


Section 4: Conclusion

In conclusion, the "Received unregistered task" error message can be solved by registering the task with Celery. You can define a task function and decorate it with "@app.task" to register it manually, or use the "autodiscover_tasks" method to register tasks dynamically. By properly registering tasks with Celery, you can ensure that your asynchronous tasks are executed smoothly without any errors.
