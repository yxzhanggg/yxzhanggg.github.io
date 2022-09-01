---
title: /Algorithm
layout: page
permalink: /Algorithm/
---
# Sort
Sort = comparison + exchange + loop invariant
```c++
void swap(void *v[], int i, int j)
{
  void *temp,
  temp = v[i];
  v[i] = v[j];
  v[j] = temp;
}
```
