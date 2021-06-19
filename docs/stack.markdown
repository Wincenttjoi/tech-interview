---
layout: default
title: Stack
nav_order: 4
---

# Implementation

## Using List as Stack

```python
s = []
s.append('a') // push
s.pop() // pops last element
s[-1] // to get last element without popping, peek element
```

![](/assets/images/stack-1.JPG)

List is not recommended:

1. Uses dynamic array, poor memory allocation
2. Need to copy over all the existing elements to another array (worse time complexity)

## Using collections.deque

### Initialize deque

```python
from collections import deque
stack = deque()
```

### Implementation of stack

```python
class Stack:
    def __init__(self):
        self.container = deque()
    
    def push(self,val):
        self.container.append(val)
        
    def pop(self):
        return self.container.pop()
    
    def peek(self):
        return  self.container[-1]
    
    def is_empty(self):
        return len(self.container)==0
    
    def size(self):
        return len(self.container)
```

### Supported methods

![](/assets/images/stack-2.JPG)
