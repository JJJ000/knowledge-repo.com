---
title: What is the difference between behaviorsubject and observable?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-03 00:00:00
updated_at: 2023-02-03 00:00:00
tldr: BehaviorSubject is a type of Observable that always emits the current value, while an Observable can emit any number of values over time.
---

**Contents**

[TOC]

### BehaviorSubject
A BehaviorSubject is a type of subject, a subject is a special type of observable so you can subscribe to messages that are sent to a subject. BehaviorSubjects are unique because they require an initial value and will always return the current value on subscription.

### Observable
An Observable is a stream of values that can be observed and acted upon. Observables are used for asynchronous programming, allowing values to be received over time. Unlike BehaviorSubjects, Observables do not require an initial value and can return multiple values over time.

### Differences
The main difference between BehaviorSubject and Observable is that BehaviorSubject requires an initial value and will always return the current value on subscription, while Observables do not require an initial value and can return multiple values over time.

### Use Cases
BehaviorSubjects are useful when you need to store and emit the current state of a variable, such as a user's authentication status. Observables are useful when you need to listen to a stream of values, such as a stream of data coming from a server.
