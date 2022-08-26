---
title: /OOP
layout: page
permalink: /OOP
---
# Association / Acquaintance [USES-A]
Association / Acquaintance have same implementation in C++, but association / acquaintance has weaker logic relation.
# Aggregation [HAS-A]
```c++
class A
{
};
class B
{
  private:
    A *a;
};
class C
{
  private:
    A *a;
};
// B and C are both aggregates of A / B "HAS-A" A / C "HAS-A" A
```
# Composition [PART-OF]
```c++
class A
{
  public:
    void foo();
};
class B
{
  private:
    B a;
  public:
    void dfoo() // dfoo is a delegate from a
    {
      a.foo();
    }
};
// B is a composition with A / "PART-OF" B is A
```
