---
layout: default
title: Home
nav_order: 1
permalink: /
---

# Introduction

This website is meant for technical interview revision purposes.


# Miscellenous

## Permutation

Watch [here](https://www.youtube.com/watch?v=s7AvT7cGdSo) for explanation.

```python
def permute(self, nums: List[int]) -> List[List[int]]:
  result = []

  #base case
  if len(nums) == 1:
    return [nums[:]] #same as [nums.copy()]

  for i in range(len(nums)):
    n = nums.pop(0)
    perms = self.permute(nums)

    for perm in perms:
      perm.append(n)
    result.extend(perms)
    nums.append(n)
  
  return result
```
