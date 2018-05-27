---
layout: post
title: "Chapter 9 - Pointers"
date: 2018-05-25 11:44:00
categories: CIT120
author: Alex Silkin
tags: "#CIT237"
---

# Chapter 9 - Pointers

- TOC
{:toc}


### What is it?

> A pointer is a variable that holds a memory address where a value lives.
>
> A pointer is declared using the `*` operator before an identifier.
>
> As C++ is a statically typed language, the type is required to declare a pointer. This is the type of data that will live at the memory address it points to.


### How to declare?

```c++
// A pointer which pointing to a variable of type int
int *pointerTo;
int x = 1;
// OR in one line
int x = 1, *pointer = &x;
// Store address of x in the pointer;
pointerTo = &x;
```

### Comparing address?

```c++
if(pointerTo < pointer) cout << "Comparing address";
```

### Comparing values?

```c++
if(*pointerTo == *pointer) cout << "Comparing values";
```

