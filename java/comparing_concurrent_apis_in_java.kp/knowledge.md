---
title: What is the distinction between completablefuture, future, and rxjava's observable?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: CompletableFuture is a Java 8 feature which provides a Future with additional methods for composition and chaining, while RxJava`s Observable provides a reactive stream of data or events.
---

**Contents**

[TOC]

## CompletableFuture
CompletableFuture is a class introduced in Java 8 which provides a Future-like API that allows for "completion" of a computation. It provides a way to chain together multiple asynchronous operations and provides powerful methods for composing and combining Futures.

## Future
Future is an interface introduced in Java 5 which provides a way to represent the result of an asynchronous computation. It allows for the retrieval of the result of the computation, but does not provide any methods for combining or chaining Futures together.

## RxJava's Observable
RxJava's Observable is an implementation of the ReactiveX (Rx) library, which provides a powerful set of operators for composing and combining asynchronous operations. Unlike CompletableFuture and Future, RxJava's Observable is not limited to a single result, but can emit multiple values over time. This makes it ideal for working with data streams and event-based applications.
