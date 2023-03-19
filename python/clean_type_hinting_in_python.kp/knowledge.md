---
title: Type hinting in Python can be implemented without causing cyclical imports
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-05 00:00:00
updated_at: 2023-03-05 00:00:00
tldr: One way to avoid cyclic imports while using type hinting in Python is to use strings instead of actual class names in the type hints.
---

**Contents**

[TOC]

Introduction
---

Type hinting is a feature introduced in Python 3.5 that allows developers to define the expected types of parameters and the return type of a function. This can be very useful for both the developer and the user of the module because it helps to catch bugs early on and it provides better documentation.

However, type hinting can be tricky to get right when dealing with cyclic imports. Cyclic imports happen when two or more modules import each other, either directly or indirectly. This can cause problems with type hinting because the types may not be defined when they are needed.

In this article, we will explore some strategies to handle type hinting with cyclic imports.



Use Strings
---

One strategy that can be used to handle cyclic imports with type hinting is to use strings instead of the actual type. This is not as desirable as using the actual type, but it can work if the type is not available at the time of type hinting.

For example, consider the following code:

```python
# module_a.py
from typing import List

def get_items() -> List[Item]:
    pass

from module_b import Item

# module_b.py
class Item:
    pass

from module_a import get_items
```

In this case, we have a cyclic import between `module_a` and `module_b`. If we try to use the `List[Item]` type hint in `module_a`, we will get a NameError because `Item` is not defined yet.

To work around this, we can use strings instead of the actual type:

```python
# module_a.py
from typing import List

def get_items() -> List[str]:
    pass

from module_b import Item

# module_b.py
class Item:
    pass

from module_a import get_items
```

In this case, we are using the `str` type instead of `Item` in the type hint for `get_items`. This works because the `str` type is available at the time of type hinting.



Reorganize the Code
---

Another strategy for dealing with cyclic imports and type hinting is to reorganize the code so that the types are defined before they are used.

In the previous example, we could move the definition of `Item` to a separate module and import it in both `module_a` and `module_b`. This would allow us to use the actual type in the type hint for `get_items`:

```python
# item.py
class Item:
    pass

# module_a.py
from typing import List
from item import Item

def get_items() -> List[Item]:
    pass

from module_b import Item

# module_b.py
from item import Item

from module_a import get_items
```

In this case, we have moved the definition of `Item` to a separate module and imported it in both `module_a` and `module_b`. Now, we can use the actual type in the type hint for `get_items`.



Use Forward References
---

Another strategy for dealing with cyclic imports and type hinting is to use forward references. Forward references allow us to refer to a type that has not been defined yet.

For example, consider the following code:

```python
# module_a.py
from typing import List

def get_items() -> List[Item]:
    pass

from module_b import Item

# module_b.py
class Item:
    pass

from module_a import get_items
```

In this case, we can use a forward reference for `Item`:

```python
# module_a.py
from typing import List

def get_items() -> List['Item']:
    pass

from module_b import Item

# module_b.py
class Item:
    pass

from module_a import get_items
```

In this case, we are using `List['Item']` instead of `List[Item]`. The `Item` inside the string is a forward reference, which means that it refers to a type that has not been defined yet. This allows us to use the actual type in the type hint for `get_items`.

Conclusion
---

In this article, we discussed three strategies for dealing with cyclic imports and type hinting in Python: using strings instead of the actual type, reorganizing the code, and using forward references. While using strings or forward references is not as desirable as using the actual type, they can be useful when the type is not available at the time of type hinting. Reorganizing the code can be a more permanent solution that allows us to use the actual type in the type hint.
