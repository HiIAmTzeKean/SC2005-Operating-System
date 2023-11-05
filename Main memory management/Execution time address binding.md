---
tags:
  - 🌱
  - OS
  - ComputerScience 
alias: Late binding
date: 22--Jul--2022
---

# Execution time address binding

Process expected to move during its execution from one memory segment to another, then binding must be delayed till run time.

## Advantage
1. Flexible for memory allocation
    1. Binding is **dynamic**
2. Portable

## Disadvantage
1. Using separate logical and physical addresses
    1. Compiler will generate logical address ([[Logical address space]] different from [[Physical address space]])
    2. Need hardware support for translating logical address to physical address at execution (Done by [[Memory management unit]])

---
Links: 