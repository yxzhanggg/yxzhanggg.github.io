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
int *array[3]; // Pointer array: an array of 3 pointers to integers

int (*p)[3]; // A pinter to an array of 3 integers
```
