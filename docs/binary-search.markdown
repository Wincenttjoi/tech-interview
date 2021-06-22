---
layout: default
title: Binary Search
nav_order: 6
---

# Questions

![]({{site.url}}/{{site.baseurl}}/assets/images/binary-search-1.JPG)

This question is easy in a sense that one could run an exhaustive iteration to obtain the result. That could work, except that it would run out of time when the input becomes too large. So let us take a step back to look at the problem, before rushing to the implementation.

Assume that the answer is kk, i.e. we've managed to complete kk rows of coins. These completed rows contain in total `1 + 2 + ... + k = k(k+1) / 2` coins.

We could now reformulate the problem as follows:

Find the maximum k such that `k*(k + 1) / 2 <= N`

```python
class Solution:
    def arrangeCoins(self, n: int) -> int:
        left = 0
        right = n

        while left <= right:
            k = (left + right) // 2
            curr = (k * (k + 1)) // 2
            if curr == n:
                return k
            elif n < curr:
                right = k - 1
            else:
                left = k + 1
        return right

```
