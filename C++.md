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
// 1. aliasing
int asddsdsdasdasd = 1;
int &b = asddsdsdasdasd;
b = 3;
// 2. avoiding copy large things
auto &x = findMax(arr); // Returns large value
// call-by-reference-to-a-constant / call-by-constant reference (equivalent to call-by-value but smaller memory)
string randomItem(const vector<string> &arr); // call in large array but without requirememt of copying
// 3. passing parameters - call-by-lvalue-reference
void swap( double & a, double & b );
// range loop to change value
for (auto &x : arr) { // without '&', x is a copy of the original one
  ++x;
}

// rvalue (temporary value) reference
string &&c = "hello";
string randomItem(vector<string> && arr); // overloading randomItem
vector<string> v {"hello", "world"};
cout << randomItem(v) << endl; // invokes lvalue method
cout << randomItem({"hello", "world"}) << endl; // invokes rvalue method
```
