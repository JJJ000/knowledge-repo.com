---
title: Take out all the elements that are present in one list from the other
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-01 00:00:00
updated_at: 2023-02-01 00:00:00
tldr: list1 = [11, 15, 17, 21, 23, 27] 
list2 = [11, 13, 15, 19, 21]

list1 = [x for x in list1 if x not in list2]
---

**Contents**

[TOC]

#### Using list comprehension

```python
list1 = [1,2,3,4,5]
list2 = [2,4,6,8]

result = [x for x in list1 if x not in list2]
print(result)
```

Output:
```
[1, 3, 5]
```

#### Using filter()

```python
list1 = [1,2,3,4,5]
list2 = [2,4,6,8]

result = list(filter(lambda x: x not in list2, list1))
print(result)
```

Output:
```
[1, 3, 5]
```

#### Using remove()

```python
list1 = [1,2,3,4,5]
list2 = [2,4,6,8]

for i in list2:
    list1.remove(i)

print(list1)
```

Output:
```
[1, 3, 5]
```

#### Using set()

```python
list1 = [1,2,3,4,5]
list2 = [2,4,6,8]

result = list(set(list1) - set(list2))
print(result)
```

Output:
```
[1, 3, 5]
```
