---
title: An internallinkedhashmap<string, dynamic> cannot be used as a list<dynamic>
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: No, an InternalLinkedHashMap is not a subtype of List, so it cannot be used as a valid JSON type.
---

**Contents**

[TOC]

## Introduction

When working with JSON data, it is important to ensure that the data types are correctly handled. This is especially true when dealing with nested JSON objects, as the data types of the nested objects must match the data types of the parent object. In this case, an error is thrown when trying to convert an InternalLinkedHashMap<String, dynamic> to a List<dynamic>.

## What is an InternalLinkedHashMap?

An InternalLinkedHashMap is a data structure used to store key-value pairs. It is an implementation of the LinkedHashMap class in the Dart programming language. It is similar to a HashMap, but it maintains the order in which elements are added.

## Why can't an InternalLinkedHashMap be converted to a List?

An InternalLinkedHashMap is a data structure that stores key-value pairs, while a List is a data structure that stores a collection of items. Because the two data structures have different structures, it is not possible to convert one to the other.

## How can this issue be resolved?

The issue can be resolved by first converting the InternalLinkedHashMap to a List of Maps. This can be done by iterating over the InternalLinkedHashMap and creating a Map for each key-value pair. Once the List of Maps has been created, it can then be converted to a List of dynamic objects.
