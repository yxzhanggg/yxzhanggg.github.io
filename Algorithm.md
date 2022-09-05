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
# Quick power
```c++
// decimal to binary: 10 = 1 0 1 0 
//                         8 4 2 1
//                    a^10 = a^8 * a^2

int quick_pow(int a, int b) {
  int temp = a, ans = 1;
  while (b) {
    if (b % 2) {
    ans = ans * temp;
    }
  b /= 2;
  temp = temp * temp;
  }
  return ans;
}

int main() {
  int a, b;
  while (cin >> a >> b) {
  cout << quick_pow(a, b) << endl;  
  return 0;
  }
}
```
