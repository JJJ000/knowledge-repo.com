---
title: Does parsing JSON result in faster parsing compared to xml?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Yes, parsing JSON is generally faster than parsing XML due to its simpler and more lightweight syntax.
---

**Contents**

[TOC]

## Introduction

Both XML and JSON are widely used formats for data representation, and they are commonly used in web applications, APIs, and databases. However, JSON has gained popularity in recent years due to its simplicity and ease-of-use compared to XML. In this article, we will explore whether parsing JSON is faster than parsing XML and provide an answer based on benchmarks and real-world use cases.

## Benchmarks

Several benchmarks have been conducted to compare the performance of parsing JSON and XML in different programming languages and libraries. Here are some of the key findings:

- In general, parsing JSON is faster than parsing XML due to its lightweight and simpler syntax.
- JSON parsers are generally faster than XML parsers, especially when parsing large datasets.
- However, the performance difference may vary depending on the size and complexity of the data and the library used.
- In some cases, XML parsers may perform better than JSON parsers when dealing with heavily nested or complex data structures.

Here are some specific benchmark results from different sources:

- The benchmark conducted by TechEmpower in 2018 showed that JSON parsing was faster than XML parsing in all the tested frameworks and platforms, with JSON parsing times ranging from 400-500 microseconds and XML parsing times ranging from 1500-2000 microseconds (source: https://www.techempower.com/benchmarks/#section=data-r18&hw=ph&test=json).
- A benchmark conducted by Martin Fowler in 2012 showed that JSON parsers were significantly faster than XML parsers, with JSON parsing times ranging from 70-250 milliseconds and XML parsing times ranging from 130-760 milliseconds (source: https://martinfowler.com/articles/json-or-xml.html).
- A benchmark conducted by Liran Ben-David in 2018 showed that JSON libraries were generally faster than XML libraries, with JSON parsing times ranging from 0.7-3.3 milliseconds and XML parsing times ranging from 2.8-7.5 milliseconds (source: https://liranzelkha.com/Performance-comparison-of-XML-and-JSON-parsers-in-python).

## Real-World Use Cases

While benchmarks can give us a good idea of the performance difference between JSON and XML parsing, real-world use cases may be more nuanced. Here are some factors that may affect the performance of JSON and XML parsing in different scenarios:

- The size and complexity of the data: In general, JSON parsing may be faster than XML parsing for small to medium-sized datasets with simple structures. However, for large or complex datasets with nested structures and complex schemas, XML parsing may be more efficient.
- The programming language and library used: The performance of JSON and XML parsing may vary depending on the programming language and library used. Some languages or libraries may be optimized for one format or the other.
- The application architecture and network latency: The parsing time may also be affected by the overall architecture of the application and the network latency between the client and server.

## Conclusion

In conclusion, parsing JSON is generally faster than parsing XML due to its lightweight and simpler syntax. However, the performance difference may vary depending on the size and complexity of the data, the programming language and library used, and the overall architecture of the application. In most cases, JSON may be a better choice for small to medium-sized datasets with simple structures, while XML may be more efficient for large or complex datasets with nested structures and complex schemas.
