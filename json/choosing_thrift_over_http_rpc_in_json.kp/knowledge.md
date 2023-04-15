---
title: What is the reason for using thrift instead of http rpc(json+gzip)?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Thrift offers better performance, fewer network round trips, and support for multiple programming languages compared to HTTP RPC(JSON+gzip) in Json.
---

**Contents**

[TOC]

## Thrift vs. HTTP RPC(JSON+gzip)

### Performance
One of the major reasons why Thrift is preferred over HTTP RPC with JSON+gzip is performance. Thrift is designed for efficient data transmission and serialization across different programming languages. It uses a compact binary format that is optimized for performance and uses less bandwidth than JSON. In contrast, HTTP RPC with JSON+gzip uses a text-based format that is not as efficient and requires more bandwidth.

### Portability
Another key advantage of Thrift is that it is highly portable across different programming languages and platforms. Thrift code can be generated for multiple languages including C++, Java, Python, and Ruby among others. This means that developers can easily write applications in one language and use them in another without having to worry about compatibility issues. In contrast, HTTP RPC using JSON+gzip is less portable as it is primarily designed for web applications.

### Scalability
Thrift is also designed for scalability and can handle large volumes of data and high traffic loads. It supports multiplexing, connection pooling, and other features that make it well-suited for building high-performance and scalable systems. In contrast, HTTP RPC using JSON+gzip has limitations in terms of scalability and may not be suitable for applications that require high levels of performance and scalability.

### Complexity
One of the drawbacks of Thrift is that it is more complex to set up and use than HTTP RPC with JSON+gzip. Thrift requires you to define an interface definition language (IDL) for your services, which can be time-consuming and add to the complexity of your system. In contrast, HTTP RPC using JSON+gzip is simpler and easier to understand, which makes it a good choice for small to medium-sized applications.
