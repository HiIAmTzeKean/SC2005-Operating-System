---
tags: 🌱
alias: Delayed binding
date: 22--Jul--2022
---

# Load time address binding

When process memory location not known at compile time, compiler generates [[Relocatable code]]. Final binding delayed till load time and if starting address change, only reload user code to incorporate changes.

## Advantage

1. Efficient code and allow for separate compilation
2. Portable and sharing of object code
3. No generation of [[Logical address]]
    1. [[Logical address space]] same as [[Physical address space]]

## Disadvantage

1. Not flexible for memory allocation

---
Links: 