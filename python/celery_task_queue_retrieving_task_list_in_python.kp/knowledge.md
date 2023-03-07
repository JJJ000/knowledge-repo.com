---
title: Obtain a queue's task list through celery
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-07 00:00:00
updated_at: 2023-03-07 00:00:00
tldr: The list of tasks in a queue in Celery can be retrieved using the `celery -A <app\_name> inspect active\_queues` command in the command line.
---

**Contents**

[TOC]

## Setting up Celery
Before we can retrieve a list of tasks in a queue in Celery, we need to set it up in our Python environment. Here's how to do it:

```python
from celery import Celery

# Instantiate a Celery object
app = Celery('tasks', broker='pyamqp://guest@localhost//')

# Define a dummy task
@app.task
def dummy_task():
    pass
```

This is a very basic setup that creates a Celery app with a RabbitMQ broker.

## Creating and Enqueueing Tasks
Now, let's create a few tasks and enqueue them so that we can retrieve them later:

```python
# Enqueue a few tasks
dummy_task.delay()
dummy_task.delay()
dummy_task.delay()
```

We have enqueued three numbers of dummy tasks but one can enqueue the desired task in this way.

## Retrieving a List of Tasks
Finally, it's time to retrieve a list of tasks in the queue. Here's how to do it with Celery:

```python
# Retrieve a list of tasks in the queue
task_list = app.control.inspect().active()

# Print the list of tasks
print(task_list)
```

This code retrieves a list of active tasks and prints them out to the console.

## Conclusion
Congratulations, you now know how to retrieve a list of tasks in a queue in Celery! With this knowledge, you can create even more powerful and flexible applications that use Celery to handle tasks in the background.
