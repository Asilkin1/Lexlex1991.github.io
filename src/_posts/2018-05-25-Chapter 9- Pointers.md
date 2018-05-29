---
layout: post
title: "Chapter 9 - Pointers"
date: 2018-05-25 11:44:00
categories: CIT237
author: Alex Silkin
tags: "#CIT237"
publish: true
---


- TOC
{:toc}




### __Getting the Address of a Variable__ 
> Address operator & return the memory address of a variable

```c++
// get an address of a variable
cout << &ourVariable;
```

### __Pointer Variables__ 

#### *Indirection operator* 
This is how indirection operator looks like `*`

#### *Declaration*

```c++
// A pointer which pointing to a variable of type int
int *pointerTo;
int x = 1;
// OR in one line
int x = 1, *pointer = &x;
// Store address of x in the pointer;
pointerTo = &x;
```

#### *Definition*
> NOTE: A pointer is a variable that holds a memory address where a value lives.
> A pointer is declared using the `*` operator before an identifier.
> As C++ is a statically typed language, the type is required to declare a pointer. This is the type of data that will live at the memory address it points to.
>  Pointers are designed to hold memory addresses. Pointers allow to indirectly manipulate 
data stored in other variables.

In the following example a reference variable passed as a parameter of the function is acting like a pointer.

```c++
int num;
getNum(num);

// Definition
void getNum(int &num)
{
cout << "What is the number?";
cin >> num;
}
```
In this example the num parameter is a reference variable, and it receives the *address* of the num variable.

Reference variables are easier to work with, but pointers are necessary for some operations like dynamic memory allocation(When the program will work with an unknonw amount of data).

#### *Creating a pointer*
```c++
int *pointer;
```

Means that the pointer can hold a memory address of the variable of type integer.

#### *Using a pointer*
```c++
int main() 
{
int num = 13;
int *pointer = nullptr;

// Refer to the address of the num
pointer = &num; 
cout << "The value of num is " << num << endl;
cout << "The address of the num is " << pointer << endl;
}
```

### __The Relationship Between Arrays and Pointers__
Concept:
>NOTE: Array names can be used as a constant pointers. Pointers can be used as array names

#### *Dereference array name*

```c++
#include <iostream>
using namespace std;

int main()
{
    int numArray[] = {1,2,3,4,5};
    
    cout << "The first element of the array is ";
    cout << *numArray << endl;
    return 0;
}
```
Will print element with an index 0 which is 1

#### *Processing an array with pointers*
```c++
int main()
{
    // Size of our array
    const int SIZE = 5;
    int count,num[SIZE];
    
    // Get values from the array
    cout << "Provide" << SIZE << " numbers: ";
    for (count = 0; count < SIZE; count++)
        cin >> *(numbers + count);
        
    // Print values
    cout << "Numbers from the array: ";
    for (count = 0; count < SIZE; count++)
        cout << *(numbers + count)<< " ";
    cout << endl;
    return 0;
}
```

### __Pointer Arithmetic__

> NOTE: Not all arithmetic operations might be applied to pointers
Allowed operations:
- `++` and `--` to increment or decrement a pointer variable;
-  `+` or `-` to add or substract an integer from the pointer;
- pointer can be substracted from another pointer;

| R1 | C1 | C2 | C3 |
| sd | dd |
| sd |
| sd |

A content of pointer variable can be changed with math satements such as addition `+` and substraction `-`.

```c++
const int SIZE = 8;
int set[SIZE] = {5, 10, 15, 20, 25, 30, 35, 40};
int *pointer = nullptr; // Pointer
int count; // Counter for for loop

pointer = set;

cout << "Display array content: ";
for(count = 0; count < SIZE; count++)
{
    cout << *pointer << " ";
    pointer++;
}
```
Display the array content backwards 
```c++
cout << "\mDisplya numbers backwards: ";
for(count = 0; count < SIZE; count++)
{
    pointer--;
    cout << *pointer << " ";
}
```
>NOTE: increment operator adds the size of one integer to pointer. As a result it points to the next element in the array. Decrement operator substracts the size of one integer accordingly.

### __Initializing Pointers__

> NOTE: Pointers can be initialized with the address of an existing object

```c++
int value;
int *pointer = &value;
```

### __Comparing Pointers__
>NOTE: First address considered as lower than the second. Can compare with `>< == != >= <=`

For example all of the following statements are true:
```c++
if (&a[1] > &a[0])
if (a < &a[4])
if (a == &a[0])
if (&a[2] != &a[3])
```
#### *Comparing address*

```c++
if(pointerTo < pointer) cout << "Comparing address";
```

#### *Comparing values*

```c++
if(*pointerTo == *pointer) cout << "Comparing values";
```

### __Pointers as Function Parameters__
>NOTE: Pointer as a function argument act very similar to a reference variable

### __Focus on Software Engineering: Dynamic Memory Allocation__ 
### __Focus on Software Engineering: Returning Pointers from Functions__
### __Using Smart Pointers to Avoid Memory Leaks__ 
### __Focus on Problem Solving and Program Design: A Case Study__
