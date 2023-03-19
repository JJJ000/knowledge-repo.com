---
title: What is the difference between asyncio.gather and asyncio.wait?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-05 00:00:00
updated_at: 2023-03-05 00:00:00
tldr: asyncio.gather() runs coroutines concurrently and returns the results in a list while asyncio.wait() returns two sets of tasks completed and pending.
---

**Contents**

[TOC]

## Introduction

Asynchronous programming is becoming more and more popular nowadays. In Python, the asyncio module provides an easy and effective way to write asynchronous code. asyncio.gather and asyncio.wait are two functions that can be used to execute coroutines concurrently but in different ways. In this article, we will explain the difference between them and when to use them.

## What is asyncio.gather?

asyncio.gather is a function that takes in a series of coroutines and runs them concurrently. It returns a list of the results of all the coroutines when they are completed. The order of the results in the returned list is the same as the order of the passed coroutines.

For example:

```python
async def count():
    for i in range(1, 11):
        print(i)
        await asyncio.sleep(1)
    return "Counting completed"

async def main():
    tasks = [count(), count(), count()]
    results = await asyncio.gather(*tasks)
    print(results)

asyncio.run(main())
```

In this example, count() is executed concurrently three times with asyncio.gather(). When the execution is completed, all the returned results are collected in the order of the passed coroutines and printed out.


## What is asyncio.wait?

asyncio.wait is a bit different from asyncio.gather. It takes in a series of coroutines and runs them concurrently, but it returns two sets of tasks: one set of completed tasks and one set of pending tasks. 

```python
async def task():
    await asyncio.sleep(1)

async def main():
    coroutines = [task() for _ in range(10)]
    done, pending = await asyncio.wait(coroutines)

asyncio.run(main())
```

In this example, the main() coroutine creates ten instances of task() coroutine and submits them to the event loop using asyncio.wait(). Since each task() coroutine takes one second to run, the entire process would run for ten seconds. 

The asyncio.wait() function returns two sets of coroutines. When a task is completed, it is removed from the pending set and added to the completed set. This function is useful when we want to periodically check the status of the scheduled coroutines or when we want to run coroutines for a specified period.

## When to use asyncio.gather?

asyncio.gather is used when we need to concurrently execute multiple coroutines and wait on the results. This function is useful when we want to run a group of tasks concurrently, and we need to collect their results at the end. 

For example, when downloading multiple images, we can download them in parallel using asyncio.gather.

```python
async def download_image(url):
    async with aiohttp.ClientSession() as session:
        async with session.get(url) as response:
            content = await response.read()
            return content

async def download_images(urls):
    tasks = [download_image(url) for url in urls]
    return await asyncio.gather(*tasks)

asyncio.run(download_images(['url1', 'url2', 'url3']))
```

In this example, we are downloading three images concurrently using aiohttp client, and the result of each download is returned as a bytestring. The asyncio.gather() function allows us to start all the downloads simultaneously and wait for all the results at the end.

## When to use asyncio.wait?

asyncio.wait is used when we need a bit more control over the coroutines we are running. It is particularly useful when we want to impose a timeout on running coroutines.

```python
async def download_image(url):
    async with aiohttp.ClientSession() as session:
        async with session.get(url) as response:
            content = await response.read()
            return content

async def download_images(urls):
    tasks = [download_image(url) for url in urls]
    done, pending = await asyncio.wait(tasks, timeout=5)
    return [t.result() for t in done]

asyncio.run(download_images(['url1', 'url2', 'url3']))
```

In this example, we are downloading three images concurrently using aiohttp client, but we are setting a timeout of five seconds. If any of the coroutines do not complete within five seconds, they will be cancelled. 

In summary, asyncio.gather is useful when we need to execute a group of coroutines in parallel and collect their results at the end, while asyncio.wait is useful when we want to impose a timeout on running coroutines or to periodically check the status of the running coroutines.
