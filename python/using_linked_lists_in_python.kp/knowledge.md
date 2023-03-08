---
title: What are the ways to utilize a linked list in python?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-08 00:00:00
updated_at: 2023-03-08 00:00:00
tldr: You can use the built-in `linked list` module in Python or create your own implementation using classes and objects.
---

**Contents**

[TOC]

# Section 1: Introduction
A linked list is a data structure that consists of a sequence of nodes, where each node contains data and a reference to the next node in the sequence. Unlike arrays, linked lists do not have a fixed size and can be easily resized. Python doesn't have built-in support for linked lists, but we can create our own implementation using classes and objects.

# Section 2: Creating a Node Class
The first step in creating a linked list is to create a Node class. This class will represent each node in the linked list and will contain the node's data and a reference to the next node.

```python
class Node:
    def __init__(self, data):
        self.data = data
        self.next = None
```

The `__init__` method initializes the Node object with the value of its data and sets the next pointer to `None`.

# Section 3: Creating a Linked List Class
The next step is to create a LinkedList class. This class will represent the linked list and will contain methods to add, delete, and search for nodes.

```python
class LinkedList:
    def __init__(self):
        self.head = None
```

The `__init__` method initializes the LinkedList object with a `head` pointer that points to the first node in the list (in this case, it is set to `None` because the list is currently empty).

```python
    def add_node(self, data):
        new_node = Node(data)
        new_node.next = self.head
        self.head = new_node
```

The `add_node` method adds a new node to the beginning of the list by creating a new Node object with the supplied data, setting its `next` pointer to the current `head` of the list, and then setting the `head` pointer to the new node.

```python
    def delete_node(self, data):
        temp = self.head
        
        # If the head node needs to be removed
        if temp is not None and temp.data == data:
            self.head = temp.next
            temp = None
            return

        # Search for the node to be deleted
        while temp is not None:
            if temp.data == data:
                break
            prev = temp
            temp = temp.next

        # If the node is not found
        if temp == None:
            return

        # Remove the node
        prev.next = temp.next
        temp = None
```

The `delete_node` method removes a node from the list by searching for the node with the supplied data, and then removing it from the list. If the node to be deleted is the `head` node, the `head` pointer is updated to point to the next node in the list. If the node to be deleted is not found, the method simply returns without making any changes to the list.

```python
    def search_list(self, data):
        temp = self.head

        # Search for the node
        while temp is not None:
            if temp.data == data:
                return True
            temp = temp.next

        # If the node is not found
        return False
```

The `search_list` method searches for a node with the supplied data by iterating through the list using the `next` pointers until the node with the correct data is found.

# Section 4: Using the Linked List
To use the linked list, we first create an instance of the `LinkedList` class and then use its methods to add, delete or search for nodes.

```python
linked_list = LinkedList()

linked_list.add_node(1)
linked_list.add_node(2)
linked_list.add_node(3)

linked_list.delete_node(2)

print(linked_list.search_list(2)) # Output: False
```

The code above creates a linked list with three nodes (1, 2, and 3), deletes the node with data value of 2, and then searches for a node with data value of 2 (which should return False since the node was deleted).
