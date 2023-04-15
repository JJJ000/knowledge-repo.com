---
title: What is the syntax for a not equal comparison in django queryset filtering?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-30 00:00:00
updated_at: 2023-04-30 00:00:00
tldr: Use the `exclude()` method to filter out querysets that do not equal a certain value.
---

**Contents**

[TOC]

### Using 'exclude'

The Django `exclude()` method can be used to filter out records that do not match a given criteria. It is used in the same way as the `filter()` method, but it returns the opposite set of results. For example, the following query will return all objects that do not have a `name` equal to `John`:

```
MyModel.objects.exclude(name='John')
```

### Using '!='

The Django `!=` operator can also be used to filter out records that do not match a given criteria. For example, the following query will return all objects that do not have a `name` equal to `John`:

```
MyModel.objects.filter(name__ne='John')
```

### Using 'Q' objects

The Django `Q` objects can be used to create complex queries. For example, the following query will return all objects that do not have a `name` equal to `John`:

```
MyModel.objects.filter(Q(name__ne='John'))
```

### Using '~'

The Django `~` operator can also be used to filter out records that do not match a given criteria. For example, the following query will return all objects that do not have a `name` equal to `John`:

```
MyModel.objects.filter(name__not='John')
```
