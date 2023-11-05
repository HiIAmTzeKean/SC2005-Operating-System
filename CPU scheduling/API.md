---
tags:
  - 🌱
  - OS
  - ComputerScience 
aliases:
  - Application Programming Interface
date: 11--Aug--2022
---
# Application programming interface

API is used to establish connectivity to hardware and applications. APIs provides function calls that can be made to a library to perform an operation.

Programmers use a [[System call]] API to access system call services. These API reside in a library and abstract the hardware from the programmer.

## Example

Programmer was to open a file in C program code. There will be a line "filein = fopen()". This is the API that the programmer use, and the call is from the standard C library.

The compiler will translate this API call by accessing the C library to obtain the full code which maps to the "open()" operation. The open() call is a [[System call]] which request for the OS to open the file.

---
Links: [[Thread library]]