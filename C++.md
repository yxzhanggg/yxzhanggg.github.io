---
title: /C++
layout: page
permalink: /C++/
---
# Iterator
iterate through the contents of containers without considering the the size of contents
# Lambda expression / Closure
A function without name
```c++
int N = 100, M = 300;
auto f = [N, &M](int i, int j] -> int { // Capture Clause: [&], [=], [&,=N], [this], [*this], [K=3] 
  M = 20;
  N = 20; // compiler error
  return i + j;
};
cout << f(1,2) << endl; // 3
cout << M << endl; // 20
```
# Classes
Initializer runs faster than assignment in class body.

# Reference
Reference is a synomym of the original value.
```c++
// lvalue (stable value) reference
int a = 1;
int &b = a;
// rvalue (temporary value) reference
string &&c = "hello";
```
