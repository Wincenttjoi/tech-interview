---
layout: default
title: Array
nav_order: 2
---

# Libraries

**array.append(x):**
Append a new item with value x to the end of the array.

**array.count(x):**
Return the number of occurrences of x in the array.

**array.index(x):**
Return the smallest i such that i is the index of the first occurrence of x in the array.

**array.insert(i, x):**
Insert a new item with value x in the array before position i. Negative values are treated as being relative to the end of the array.

**array.pop([i]):**
Removes the item with the index i from the array and returns it. The optional argument defaults to -1, so that by default the last item is removed and returned.

**array.reverse():**
Reverse the order of the items in the array.

**array.tobytes():**
Convert the array to an array of machine values and return the bytes representation (the same sequence of bytes that would be written to a file by the tofile() method.)