---
layout: default
title: Dictionary
nav_order: 3
---

# Initialization

## Standard Initialization

```python
tel = {} // initialize empty dictionary

tel = {'jack': 4098, 'sape': 4139, 'guido': 211}
```

### Dictionary with frequency as the value

```python
  my_list = [..., ..., ...]
  freq = {}
  for item in my_list:
      if (item in freq):
          freq[item] += 1
      else:
          freq[item] = 1
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

# Examples

![]({{site.url}}/{{site.baseurl}}/assets/images/dict-1.JPG)

```python
class Solution:
    def leastInterval(self, tasks: List[str], n: int) -> int:
        res = {}
        for item in tasks:
            if (item in res):
                res[item] += 1
            else:
                res[item] = 1

        maxfreq = max(res.values())
        letters = []
        for key, frequency in res.items():
            if frequency == maxfreq:
                letters.append(key)

        return max((maxfreq - 1) * (n + 1) + len(letters), len(tasks))
        //len(tasks) for when n = 0
```

Explanation:

1. Get frequency of each letter
2. Get the max frequency as benchmark and take note of how many letters with max frequency, lower frequency letter does not matter as they equate to idle (fillers)
3. Draw out the worst case scenario to understand the logic of the return statement

```
[A, A, A, A, B, C], n = 2
A: 4, B: 1, C:1
==> A filler A filler A filler A
==> 3 sets of A filler
// maxfreq - 1 => 3 sets
// n - 1 => A filler grouping
```
