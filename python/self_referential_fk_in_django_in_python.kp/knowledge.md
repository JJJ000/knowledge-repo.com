---
title: A foreign key in django that refers back to the same model/entity is called a self-referential foreign key
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-07 00:00:00
updated_at: 2023-03-07 00:00:00
tldr: A self-referential foreign key in Django is a foreign key that relates a model to itself.
---

**Contents**

[TOC]

## Introduction

In Django, a self-referential foreign key is a foreign key that refers to the same model as the one it is defined in. It is often used in situations where an entity relates to itself. For example, a social networking site that allows users to have friends can use a self-referential foreign key to represent the relationship between users who are also friends.


## Defining a self-referential foreign key

To define a self-referential foreign key in Django, we can use the "ForeignKey" field with the "self" argument. Here's an example of how to define a self-referential foreign key in a Django model:

```python
from django.db import models

class Node(models.Model):
    parent = models.ForeignKey('self', on_delete=models.CASCADE, blank=True, null=True, related_name='children')
```

In this example, the "Node" model has a foreign key field called "parent" that refers to the same model ("self"). The "on_delete" argument specifies what happens when the referenced node is deleted. The "blank" and "null" arguments allow the field to be optional. The "related_name" argument is used to specify the name of the reverse relationship from child node back to the parent node.


## Using a self-referential foreign key

Once we have defined a self-referential foreign key in our model, we can use it just like any other foreign key. For example, we can create a node with a parent node like this:

```python
parent_node = Node.objects.create()
child_node = Node.objects.create(parent=parent_node)
```

In this example, we create a parent node and a child node with a reference to the parent node. We can then access the child nodes of a parent node like this:

```python
parent_node.children.all()
```

This will return a QuerySet of all child nodes that have a parent reference to the parent node.


## Conclusion

Self-referential foreign keys are a powerful way to represent relationships between entities that relate to themselves. In Django, they are easy to define and use, and provide a convenient way to model complex relationships within your application.
