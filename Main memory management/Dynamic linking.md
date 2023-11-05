---
tags:
  - 🌱
  - OS
  - ComputerScience 
date: 22--Jul--2022
---

# Dynamic linking

Linking postponed to be done by loader and during runtime.

1. OS checks if routine in memory
2. Loades the process [[Address space]] if routine found
3. During runtime, [[stub]] used to locate library routine in address space
4. Stub replaces itself with address of routine and executes the routine

---
Links: 