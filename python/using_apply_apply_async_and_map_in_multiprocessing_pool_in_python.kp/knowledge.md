---
title: What are the differences between using apply, apply_async, and map when working with the multiprocessing.pool class?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: Apply should be used when a single argument needs to be passed to a single function, apply\_async should be used when a single argument needs to be passed to a single function asynchronously, and map should be used when a single function needs to be applied to multiple arguments.
---

**Contents**

[TOC]

#apply
`apply` is a synchronous function, meaning that it will block the main program until the function has completed. It is best used when the function is computationally intensive, or when the function is expected to return a result.

#apply_async
`apply_async` is an asynchronous version of `apply`, meaning that it will not block the main program. It is best used when the function is expected to take a long time to complete, or when the function does not need to return a result.

#map
`map` is a synchronous function that is used to apply a function to a sequence of arguments. It is best used when the function is expected to take a long time to complete, or when the function needs to return a result.

#map_async
`map_async` is an asynchronous version of `map`, meaning that it will not block the main program. It is best used when the function is expected to take a long time to complete, or when the function does not need to return a result.
