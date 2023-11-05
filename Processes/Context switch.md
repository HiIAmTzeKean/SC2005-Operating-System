---
tags:
  - 🌱
  - OS
  - ComputerScience
  - Process
date: 21--Jul--2022
---

# Context switch

[[Interrupt]] causes OS to change a CPU core from current task to a [[Kernel routine]]. OS will then save context of [[Process]] and restore it later.

> [!summary]
> State save of current process and state restore of different process

## Constraints

Context switch time is pure overhead as no useful work is done. Speed depends on memory speed, number of registers and other factors.

![[context switching.png]]

---
Links: 