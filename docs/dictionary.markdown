---
layout: default
title: Dictionary
nav_order: 3
---

# Initilization

## Standard Initialization

```python
tel = {} // initialize empty dictionary

tel = {'jack': 4098, 'sape': 4139, 'guido': 211}
```

## Initialize using List Comprehension

```python
tel = {x: x**2 for x in range(1, 3)}
==> tel = {1: 2, 2: 4, 3: 9}
```

# Libraries

**list(tel):** Change dictionary to list

**sorted(tel):** Sort according to values

**'guido' in tel:** To check if value of 'guido' exists in 'tel'

To have a COPY of a dictionary:

```python
map = {...}
temp = dict(map)
```

To sort by VALUES:

```python
sort_orders = sorted(orders.items(), key=lambda x: x[1])
```

To sort by VALUES in REVERSE

```python
sort_orders = sorted(orders.items(), key=lambda x: x[1], reverse=True)
```

