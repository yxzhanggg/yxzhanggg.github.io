---
title: /OOP
layout: page
permalink: /OOP
---
# Inheritance [IS-A]
```c++
class A
{
  private: // will not be inherited
  int x;
  protected: // will be inherited, but is not accessible by A.y;
  int y; 
  public: // is accessible by A.foo();
  void foo();
};
class B : public A
{
  private:
  protected:
  public:
};
// B "IS-A" derivative A 
```
| Access | public | protected | private |
| :-----| ----: | :----: | :----: |
| Inside class | yes | yes | yes |
| Derived class | yes | yes | no |
| Outside class | yes | no | no |

# Composition [PART-OF] and Delegation
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
// B is a composition with A 
// "PART-OF" B is A
```
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
// B and C are both aggregates of A 
// B "HAS-A" A, B "USES_A" A
// C "HAS-A" A, C "USES_A" A
```
# Association / Acquaintance [USES-A]
Association / Acquaintance have same implementation in C++, but association / acquaintance has weaker logic relation.
