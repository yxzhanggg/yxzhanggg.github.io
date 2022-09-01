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
// Compared with fixed-size array, pointer array is more compatible 
// with heterogeneous data structure
int array[3][2]; // Fixed-size array

int *array[3];   // Pointer array: an array of 3 pointers to integers
int (*p)[3];     // A pinter to an array of 3 integers

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
int foo();
int *foo(); //a function returns a pointer to int
foo; // the adress of the function, anology of array
int (*foo)(); //foo is a pointer to the function
```
