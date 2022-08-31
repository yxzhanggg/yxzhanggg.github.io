---
title: /C
layout: page
permalink: /C/
---
# Specifier
```c
// lifetime all belows are the whole program runtime

// global among files
// -file 1
int x;
// -file 2 can access x by declaring extern
extern int x; // declare outside any function (usually in header file), defualt value 0
x = 1;

// private to the file
static int x; // defualt value 0

// store it in register
register int x;
```
