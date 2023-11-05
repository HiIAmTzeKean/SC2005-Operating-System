---
tags:
  - 🌱
  - OS
  - ComputerScience 
date: 25--Jul--2022
---

# Page table

Kept in [[Main memory]] for faster context switch.

## Architecture

Current machines support large page tables and a pointer to the page table may not be feasible since the number of bits needed typically exceeds a CPU register size. Dedicated registers are made to implement page tables.

1. [[Page table base register]] (PTBR)
2. [[Page table limit register]] (PTLR)

Changing page tables only require changing the PTBR which reduces [[Context switch]] time.


---
Links: 