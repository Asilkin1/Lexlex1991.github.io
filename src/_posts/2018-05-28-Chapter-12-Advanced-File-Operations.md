---
layout: post
title: "Chapter 12 - Advanced File Operations"
date: 2018-05-28 11:44:00
categories: CIT237
author: Alex Silkin
tags: "#CIT237"
---

- TOC
{:toc}

### File Operations 
>NOTE: File - a collection of data that is usually stored on a computer's disk.
Data can be saved to files and then later reused.

| __Data type__ | __Description__ |
| `ifstream`| Input file stream. Only can be used to read data from files into RAM.|
| `ofstream`| Output file stream. Can be used to create a file and write data to them.|
| `fstream` | File stream. Can be used to create files, write data to them, and read data from them.|

#### Using fstream with modes

| __Declare__ | __Access flag__ to open in input mode |
| fstream ourFile | ourFile.open("test.txt", ios::in)|

Which means that the file will be opened in read mode.

#### More modes

| __Flag__ | __Description__ |
| ios::app | Append mode.File will be created if it doesn't exist |
| ios::ate | If file exist, the prograg goes to the end of the file.Output can be written anywhere |
| ios::binary | Binary mode. Data is written or read from in a binary format. |
| ios::in | Input mode. Data will be read from the file. If file doens't exist, it won't be created.|
| ios::out | Output mode. Data will be written to the file. File's content will be deleted if it already exists. |
| ios::truncate | If the file alrady exists, its content will be removed.|

#### Several flags
File will be opened for input and output at the same time.
```c++
ourFile.open("test.txt", ios::in | ios::out);
```

File will be opened in wirite mode. Content will be added to the end of the file.
```c++
ourFile.open("text.txt", ios::out | ios:;app);
```
### File Output Formatting
>__NOTE__ File output format can be formatted in a same way that screen output is formatted.

Format for fixed point notation.

```c++
ourFile << fixed;
ourFile << num << endl;
```
Printing three rows of numbers into the file
```c++
#include <iostream>
#include <fstream>
#include <iomanip>
using namespace std;

int main()
{
	const int ROWS = 3;
	const int COLS = 3;
	int nums[ROWS][COLS] = {1,2,3,4,5,6,7,8,9};
	fstream outFile("table.txt", ios::out);

	for(int row = 0; row < ROWS; row++)
	{
		for(int col = 0; col < COLS; col++)
		{
			outFile << setw(8) << nums[row][col]
		}
	}
	
	outFile << endl;
	cout << "Done\n";
	return 0;
}
```
### Passing File Stream Objects to Functions
### More Detailed Error Testing
### Member Functions for Reading and Writing Files 
### Focus on Software Engineering: Working with Multiple Files
### Binary Files
### Creating Records with Structures
### Random-Access Files 
### Opening a File for Both Input and Output 
