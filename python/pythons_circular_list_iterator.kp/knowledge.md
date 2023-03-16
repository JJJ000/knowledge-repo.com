---
title: An iterator for a circular list implemented in python
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-15 00:00:00
updated_at: 2023-03-15 00:00:00
tldr: The circular list iterator in Python represents an iterator that iterates indefinitely over a circular sequence of elements.
---

**Contents**

[TOC]

# Circular List Implementation in Python

A circular list in Python is a linked list where the tail node points back to the head node, resulting in a circular structure. In this article, we will create a circular list in Python and implement an iterator for it.

## Creating a Circular List

The first step to implement a circular list in Python is to create a Node class. Each node will have a data attribute and a next attribute that will point to the next node in the list. The next attribute of the last node in the list will be set to the head of the list, creating a circular structure. Here is the Node class implementation:
```python
class Node:
    def __init__(self, data):
        self.data = data
        self.next = None
```
Next, we will create a CircularLinkedList class that will have methods to add nodes to the list and to print the list. The add method will create a new node and add it to the end of the list. The print method will traverse the list and print the data attribute of each node. Here is the CircularLinkedList class implementation:

```python
class CircularLinkedList:
    def __init__(self):
        self.head = None
        self.tail = None
    
    def add(self, data):
        new_node = Node(data)
        if self.head is None:
            self.head = new_node
            self.tail = new_node
            new_node.next = self.head
        else:
            self.tail.next = new_node
            self.tail = new_node
            self.tail.next = self.head

    def print_list(self):
        current_node = self.head
        while current_node:
            print(current_node.data)
            current_node = current_node.next
            if current_node == self.head:
                break
```

## Implementing a Circular List Iterator

To implement a circular list iterator, we will create an __iter__ method in the CircularLinkedList class that returns an instance of an iterator class. The iterator will have a __next__ method that returns the data attribute of the next node in the list. When the end of the list is reached, the iterator will wrap around to the beginning of the list. Here is the implementation of the iterator class:

```python
class CircularLinkedListIterator:
    def __init__(self, head):
        self.current_node = head
    
    def __next__(self):
        if self.current_node is None:
            raise StopIteration
        data = self.current_node.data
        self.current_node = self.current_node.next
        if self.current_node is None:
            self.current_node = self.head
        return data
```

And here is the implementation of the __iter__ method in the CircularLinkedList class:

```python
class CircularLinkedList:
    def __init__(self):
        self.head = None
        self.tail = None
    
    def add(self, data):
        new_node = Node(data)
        if self.head is None:
            self.head = new_node
            self.tail = new_node
            new_node.next = self.head
        else:
            self.tail.next = new_node
            self.tail = new_node
            self.tail.next = self.head
    
    def print_list(self):
        current_node = self.head
        while current_node:
            print(current_node.data)
            current_node = current_node.next
            if current_node == self.head:
                break
    
    def __iter__(self):
        return CircularLinkedListIterator(self.head)
```

Now we can use the for loop to iterate over the circular list:

```python
# create the list
clist = CircularLinkedList()
clist.add(1)
clist.add(2)
clist.add(3)

# iterate over the list
for data in clist:
    print(data)
```

Output:
```
1
2
3
1
2
3
1
...
``` 

As you can see, the iterator wraps around to the beginning of the list and continues infinitely. To limit the number of iterations, you can add a counter variable to the iterator class and raise a StopIteration exception after a certain number of iterations.
