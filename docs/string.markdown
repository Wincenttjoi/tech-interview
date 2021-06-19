---
layout: default
title: String
nav_order: 5
---

# String

## Join() method

Takes in iterable, returns a string

```python
string.join(iterable)
```

Some of the example of iterables are:

Native data types - List, Tuple, String, Dictionary and Set.

### Example 1

Input

```python
# .join() with lists
numList = ['1', '2', '3', '4']
separator = ', '
print(separator.join(numList))

# .join() with tuples
numTuple = ('1', '2', '3', '4')
print(separator.join(numTuple))

s1 = 'abc'
s2 = '123'

# each element of s2 is separated by s1
# '1'+ 'abc'+ '2'+ 'abc'+ '3'
print('s1.join(s2):', s1.join(s2))

# each element of s1 is separated by s2
# 'a'+ '123'+ 'b'+ '123'+ 'b'
print('s2.join(s1):', s2.join(s1))
```

Output

```
1, 2, 3, 4
1, 2, 3, 4
s1.join(s2): 1abc2abc3
s2.join(s1): a123b123c
```

### Example 2: SEts

Input

```python
# .join() with sets
test = {'2', '1', '3'}
s = ', '
print(s.join(test))

test = {'Python', 'Java', 'Ruby'}
s = '->->'
print(s.join(test))
```

Output

```
2, 3, 1
Python->->Ruby->->Java
```

### Example 3: Dictionaries

Input

```python
# .join() with dictionaries
test = {'mat': 1, 'that': 2}
s = '->'

# joins the keys only
print(s.join(test))

test = {1: 'mat', 2: 'that'}
s = ', '

# this gives error since key isn't string
print(s.join(test))
```

Output

```
mat->that
Traceback (most recent call last):
  File "...", line 12, in <module>
TypeError: sequence item 0: expected str instance, int found
```

The join() method tries to join the keys (not values) of the dictionary with the string separator.
