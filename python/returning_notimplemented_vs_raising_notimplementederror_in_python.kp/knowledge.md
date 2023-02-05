---
title: What are the advantages of returning notimplemented instead of raising notimplementederror?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: Returning NotImplemented allows abstract methods in an abstract base class to indicate that a subclass must override the method, without raising an error.
---

**Contents**

[TOC]

# Advantages

Returning NotImplemented instead of raising NotImplementedError in Python has several advantages. 

First, it allows for a more flexible and extensible codebase. By returning NotImplemented instead of raising an error, developers can provide a default behavior for a given function, while still allowing for the possibility of overriding that behavior in the future. This makes it easier to add new features or modify existing ones without having to rewrite the entire codebase.

Second, returning NotImplemented instead of raising an error can help to reduce the amount of code bloat. By avoiding the need to raise an error, developers can keep their codebase lean and efficient.

Finally, returning NotImplemented instead of raising an error can help to improve code readability. By providing a clear indication that a particular behavior is not yet implemented, developers can make their code more understandable and maintainable.

# Disadvantages

Returning NotImplemented instead of raising NotImplementedError in Python also has some disadvantages. 

First, it can make debugging more difficult. By returning NotImplemented instead of raising an error, developers may not be able to easily identify the source of a given bug or issue.

Second, returning NotImplemented instead of raising an error can lead to unexpected behavior. If a developer is not careful to properly document the behavior of their code, other developers may be unaware that a given behavior is not yet implemented and may end up relying on it.

Finally, returning NotImplemented instead of raising an error can lead to confusion. If a developer is not careful to properly document their code, other developers may not be aware that a given behavior is not yet implemented and may end up expecting it to be implemented.
