---
title: A django query set ordered by a given field, in either ascending or descending order
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-02 00:00:00
updated_at: 2023-02-02 00:00:00
tldr: To order a QuerySet in ascending order, use the order\_by() method with the `asc` parameter; to order a QuerySet in descending order, use the order\_by() method with the `desc` parameter.
---

**Contents**

[TOC]

## Ascending Order

To order a Django QuerySet in ascending order, you can use the `order_by()` method. This method takes one or more field names as arguments and orders the resulting QuerySet in ascending order (from lowest to highest).

For example, to order a QuerySet of books by title, you would use the following code:

```
Book.objects.order_by('title')
```

## Descending Order

To order a Django QuerySet in descending order, you can use the `order_by()` method with the `descending` parameter. This parameter takes a Boolean value (True or False).

For example, to order a QuerySet of books by title in descending order, you would use the following code:

```
Book.objects.order_by('title', descending=True)
```

## Multiple Fields

You can also use the `order_by()` method to order a QuerySet by multiple fields. To do this, simply pass multiple field names as arguments to the method.

For example, to order a QuerySet of books by title and then by author, you would use the following code:

```
Book.objects.order_by('title', 'author')
```

## Combining Ascending and Descending

You can also combine ascending and descending order when ordering a QuerySet. To do this, simply pass a tuple of field names and Boolean values (True for descending, False for ascending) to the `order_by()` method.

For example, to order a QuerySet of books by title in ascending order and then by author in descending order, you would use the following code:

```
Book.objects.order_by(('title', False), ('author', True))
```
