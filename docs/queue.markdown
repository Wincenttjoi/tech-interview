---
layout: default
title: Queue
nav_order: 6
---

# Methods

![]({{site.url}}/{{site.baseurl}}/assets/images/deque.JPG)

# Implementation

## Using list as a queue

```python
wmt_stock_price_queue = []
wmt_stock_price_queue.insert(0,135) // insert on left
wmt_stock_price_queue.pop() // pop last element
```

## Using collections.deque as a queue

```python
from collections import deque
q = deque()

q.appendleft(5)
q.appendleft(8)
q.appendleft(10)

q.pop()
==> 5

q
==> deque([10, 8])
```

```python
from collections import deque

class Queue:
    def __init__(self):
        self.buffer = deque()

    def enqueue(self, val):
        self.buffer.appendleft(val)

    def dequeue(self):
        return self.buffer.pop()

    def is_empty(self):
        return len(self.buffer)==0

    def size(self):
        return len(self.buffer)
```
