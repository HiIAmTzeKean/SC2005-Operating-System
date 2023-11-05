---
tags:
  - 🌱
  - OS
  - ComputerScience
  - Thread
date: 04--Jul--2022
---

# Thread library

API for programmer to create and manager threads.

## 2 implementation approach

### User-level library, no kernel support

[[User-level library]] -> Code and data structures exist in [[User space]]. Function call in library results in local function call in [[User space]] and not [[System call]].

### Kernel-level support by OS

[[Kernel-level library]] ->Code and data structure exist in [[Kernel space]]. Function call in API results in system call to kernel.

## 3 thread libraries

1. [[Pthreads]]
2. [[Windows thread library]]
3. [[Java thread API]]

---
Links: 