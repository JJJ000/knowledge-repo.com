---
title: What is the functioning mechanism of asyncio?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-05 00:00:00
updated_at: 2023-03-05 00:00:00
tldr: Asyncio in Python is a single-threaded, event-driven framework that allows for concurrent execution of multiple tasks by managing coroutine objects and I/O operations.
---

**Contents**

[TOC]

## Introduction

Asyncio is a Python library that allows developers to write concurrent code using the `async/await` syntax. It works by providing a way to write non-blocking code, where multiple functions can run concurrently without blocking each other. In this article, we will explore how asyncio works in Python.

## Event loop

The event loop is the core component of asyncio. It is responsible for scheduling and running coroutines (asynchronous functions). The event loop runs in its own thread and continuously checks for incoming events. These events are usually async tasks that have been scheduled to run. When an event is ready, the event loop will execute it.

The event loop is started by calling the `asyncio.run()` function, which takes an awaitable coroutine as its input. This coroutine will be executed by the event loop until it is complete.

## Coroutines

Coroutines are functions that can be paused and resumed at specific points in their execution. They are defined using the `async` keyword and are executed using the `await` keyword.

When a coroutine is called, it returns a coroutine object, which is not executed immediately. Instead, it is scheduled to run by the event loop. When the event loop runs the coroutine, it will continue to execute until it reaches an `await` statement. At this point, the coroutine will pause and release control back to the event loop, allowing other coroutines to run. When the awaited task is complete, the coroutine will resume execution.

## Tasks

A task is an object that wraps a coroutine, providing additional functionality like cancellation and result access. Tasks are created using the `asyncio.create_task()` function.

Once a task is created, it is added to the event loop's task queue. When the event loop runs, it will execute tasks in the order they were added to the queue. Tasks can be cancelled using the `Task.cancel()` method, which will raise a `CancelledError` exception in the coroutine.

## Conclusion

Asyncio provides an easy-to-use framework for writing concurrent code in Python. It uses an event loop to schedule and execute coroutines, which can be wrapped in tasks for additional functionality. By using asyncio, developers can write performant, non-blocking code that can handle many concurrent tasks without sacrificing readability.
