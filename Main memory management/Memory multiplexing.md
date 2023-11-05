---
tags:
  - 🌱
  - OS
  - ComputerScience 
date: 22--Jul--2022
---

# Memory multiplexing

Complete working state of [[Process]] and kernel is defined by its data in memory. Thus, processes cannot use the same memory or access to each other private memory.

1. Controlled overlap
    1. Process cannot collide in [[Main memory|physical memory]]
    2. Ability to share memory when needed for communication
2. [[Memory protection]]
    1. Prevent access to private memory of other process
    2. [[Kernel data]] protected from [[User program]]
3. [[Address translation]]
    1. Translate access from one [[Address space]] to different one
    2. Process should use logical/virtual address and physical memory use physical address

---
Links: 