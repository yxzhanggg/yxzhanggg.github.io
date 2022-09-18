---
title: /OOP
layout: page
permalink: /OOP/
---
# Inheritance [IS-A]
Constructors, destructors, friend functions and overloaded operators cannot be inherited.
```c++
// Acceccibility
// | Access        | public | protected | private |
// | Inside class  | yes    | yes       | yes     |
// | Derived class | yes    | yes       | no      |
// | Outside class | yes    | no        | no      |

class Base {
  public: 
   int x;
  protected:
   int y;
  private:
   int z;
};

// Inheritability
// | public | protected | private |
// | yes    | yes       | no      |

class PublicDerived: public Base {
  // x is public
  // y is protected
  // z is not accessible from PublicDerived
};

class ProtectedDerived: protected Base {
  // x is protected
  // y is protected
  // z is not accessible from ProtectedDerived
};

class PrivateDerived: private Base {
  // x is private
  // y is private
  // z is not accessible from PrivateDerived
};

// Derived "IS-A" derivative of Base

// Friend Class A friend class can access private and protected members of other class in which it is declared as friend.
// All access granted.
class A {
  private:
   int x_;
   
  friend class B; // [not member] Just declaration, does not belong to any member of public, protected or private
  friend int foo(A, B); // Friend Function just as Friend Class
  friend int B::bar();
};

class B {
  private:
   int x_;
   
  friend void foo(A, B);
};

int foo(A a, B b) {
  return a.x_+b.x_;
}

```
# Composition [PART-OF] and Delegation
```c++
class A {
  public:
   void foo();
};

class B {
  public:
   void dfoo() { // dfoo is a delegate from a
     a.foo();
   }
  private:
   A a;
};

// B is a composition with A 
// "PART-OF" B is A
```
# Aggregation [HAS-A]
```c++
class A {};

class B {
  private:
   A *a;
};

class C {
  private:
   A *a;
};

// B and C are both aggregates of A 
// B "HAS-A" A, B "USES_A" A
// C "HAS-A" A, C "USES_A" A
```
# Association / Acquaintance [USES-A]
Association / Acquaintance have same implementation in C++, but association / acquaintance has weaker logic relation.
