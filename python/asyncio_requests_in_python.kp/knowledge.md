---
title: What are the ways I can utilize requests while using asyncio?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: You can use the aiohttp library, which is built on top of asyncio and provides a simplified interface for making HTTP requests asynchronously.
---

**Contents**

[TOC]

# Using Async Requests with Asyncio in Python

Asynchronous programming in Python helps execute I/O-bound tasks more efficiently. By using asyncio and async/await, you can execute multiple network requests concurrently and achieve high-performance network programming. In this tutorial, we will look at how to use requests in asyncio.

## Install Required Libraries

Before we start, we will need to install the required libraries - asyncio and aiohttp.

```python
pip install asyncio aiohttp
```

## Using the aiohttp Library to make request

The aiohttp library provides an asynchronous HTTP client and server implementation. We will be using it to fetch data asynchronously from a list of URLs.

```python
import asyncio
import aiohttp

async def fetch(session, url):
    async with session.get(url) as response:
        return await response.text()

async def main():
    urls = [
        "https://httpbin.org/uuid",
        "https://httpbin.org/user-agent",
        "https://httpbin.org/headers",
    ]

    async with aiohttp.ClientSession() as session:
        tasks = []
        for url in urls:
            task = asyncio.ensure_future(fetch(session, url))
            tasks.append(task)

        responses = await asyncio.gather(*tasks)
        for response in responses:
            print(response)

if __name__ == "__main__":
    loop = asyncio.get_event_loop()
    loop.run_until_complete(main())
```

In the above code, we have defined two coroutines - the `fetch` coroutine and the `main` coroutine. `fetch` coroutine takes a session object and a URL as inputs and returns the response content for the requested URL. `main` coroutine creates a list of URLs to fetch and creates a task for each URL. We append each task to a list of tasks `tasks`., and then await the response for all of them using the `asyncio.gather` function.

## Using the requests-async Library

If you prefer to keep using the standard `requests` library instead of learning a new HTTP client, there is a library called `requests-async` that provides an asynchronous version of it.

```python
import asyncio
import requests_async as requests

async def main():
    urls = [
        "https://httpbin.org/uuid",
        "https://httpbin.org/user-agent",
        "https://httpbin.org/headers",
    ]

    responses = await asyncio.gather(*[requests.get(url) for url in urls])
    for response in responses:
        print(response.text)

if __name__ == "__main__":
    loop = asyncio.get_event_loop()
    loop.run_until_complete(main())
```

In the above code, we have defined a `main` coroutine that creates a list of URLs to fetch and then uses asyncio's `asyncio.gather` function to gather the response for all of them using the `requests.get` function provided by the `requests-async` library.


## Conclusion

By using asyncio and async/await, we have demonstrated how you can execute multiple network requests concurrently and achieve high-performance network programming in Python. We have also shown how you can use the aiohttp library and the `requests-async` library to make requests asynchronously.
