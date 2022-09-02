---
title: /C
layout: page
permalink: /C/
---
# Specifier
```c
// Lifetime all belows are the whole program runtime

// Global among files
// -file 1
int x;
// -file 2 can access x by declaring extern
extern int x; // Declare outside any function (usually in header file)
              // Defualt value 0
x = 1;

// Private to the file
static int x; // defualt value 0

// Store it in register
register int x;
```
# Array
```c
// The size of array is determined at compile time.
// Compared with fixed-size array, pointer array is more compatible 
// with heterogeneous data structure
char arr[3][2]; // Fixed-size array

char *arr[3];   for (ptr = head; ptr != NULL; ptr = ptr->next)// Pointer array: an array of 3 pointers to chars
char **arr;     // Pointer to pointer to char
char (*p)[3];   // A pinter to an array of 3 chars

//                 +---+         +---+---+---+---+---+
// argv ---------->| 0 |-------->| p | r | o | g | 0 |
//                 +---+         +---+---+---+---+---+
//                 | 1 |-------->| - | a | b | 0 |
//                 +---+         +---+---+---+---+
//                 | 2 |-------->| - | c | 0 |
//                 +---+         +---+---+---+---+---+---+
//                 | 3 |-------->| H | e | l | l | o | 0 |
//                 +---+         +---+---+---+---+---+---+
//                 | 4 |-------->| W | o | r | l | d | 0 |
//                 +---+         +---+---+---+---+---+---+
//                 | 5 |-------->NULL
//                 +---+
*++argv[0];      // equals *++(argv[0]), increase the pointer argv[0],
                 // then dereference (*), which equals 'r' in the case
(*++argv)[0];    // increase the pointer argv, then dereference by *,
                 // then dereference by [0] to the first element,
                 // which equals '-' in the case
```
# function
```c
int foo();          // a simple function declaration
int *foop();        // a function returns a pointer to int
foo;                // the adress of the function, anology of array
int (*pfoo)();      // foo is a pointer to the function
char (*(*x())[])(); // function returning pointer to array of pointer
                    // to function returning char
char (*(*x[])())[]; // array of pointer to function returning pointer
                    // to array of char
```
# sturcture
```c
struct point {
  int x;
  int y;
 };
sturct point *pp; // Pass large structure using pointer
// structure operator . ->
(*pp).x;
pp->x;

// Binary tree
struct tnode {         // The tree node
  char *word;          // Points to the text
  int count;           // Number of occurrences
  struct tnode *left;  // Left child
  struct tnode *right; // Right child
};

union {
  int ival;
  float fval;
  char *sval;
} u;

struct { // bit-field: only take 1-bit without address
  unsigned int is_keyword : 1;
  unsigned int is_extern : 1;
  unsigned int is_static : 1;
} flags;
```
# Lookup idom
```c
for (ptr = head; ptr != NULL; ptr = ptr->next)
```

