---
title: What is the best way to use a tree structure in python?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: You can implement a tree in Python by using the built-in library collections.Tree.
---

**Contents**

[TOC]

# 1. Create a Node class

Creating a Node class is the first step to implementing a tree in Python. A Node class typically contains the following attributes: 

- A `value` attribute, which holds the data contained in the node. 
- A `left` attribute, which points to the left child of the node. 
- A `right` attribute, which points to the right child of the node. 

The following code can be used to create a Node class in Python: 

```
class Node: 
    def __init__(self, value): 
        self.value = value 
        self.left = None 
        self.right = None 
```

# 2. Create a Tree class 

The next step to implementing a tree in Python is to create a Tree class. This class will contain methods to add, search, and traverse nodes within the tree. 

The following code can be used to create a Tree class in Python: 

```
class Tree: 
    def __init__(self): 
        self.root = None 
    
    def add_node(self, value): 
        pass 
    
    def search_node(self, value): 
        pass 
    
    def traverse_tree(self): 
        pass 
```

# 3. Implement Tree class methods

The Tree class methods will be used to add, search, and traverse nodes within the tree. 

The `add_node()` method will be used to add new nodes to the tree. The `search_node()` method will be used to search for a given node within the tree. The `traverse_tree()` method will be used to traverse the tree and print out the values of each node. 

The following code can be used to implement the Tree class methods in Python: 

```
class Tree: 
    def __init__(self): 
        self.root = None 
    
    def add_node(self, value): 
        new_node = Node(value) 
        if self.root is None: 
            self.root = new_node 
        else: 
            current_node = self.root 
            while True: 
                if value < current_node.value: 
                    if current_node.left is None: 
                        current_node.left = new_node 
                        break 
                    else: 
                        current_node = current_node.left 
                else: 
                    if current_node.right is None: 
                        current_node.right = new_node 
                        break 
                    else: 
                        current_node = current_node.right 
    
    def search_node(self, value): 
        if self.root is None: 
            return False 
        else: 
            current_node = self.root 
            while current_node is not None: 
                if current_node.value == value: 
                    return True 
                elif value < current_node.value: 
                    current_node = current_node.left 
                else: 
                    current_node = current_node.right 
            return False 
    
    def traverse_tree(self): 
        if self.root is not None: 
            self._traverse_tree(self.root) 
    
    def _traverse_tree(self, node): 
        if node is not None: 
            self._traverse_tree(node.left) 
            print(node.value) 
            self._traverse_tree(node.right) 
```

# 4. Test the Tree

The last step to implementing a tree in Python is to test the Tree class. The following code can be used to test the Tree class: 

```
tree = Tree() 
tree.add_node(5) 
tree.add_node(3) 
tree.add_node(7) 
tree.add_node(2) 
tree.add_node(4) 
tree.add_node(6) 
tree.add_node(8) 

tree.traverse_tree() 

# Output: 
2 
3 
4 
5 
6 
7 
8

print(tree.search_node(7)) 
# Output: True 
```
