---
tags:
  - 🌱
  - OS
  - ComputerScience 
date: 27--Jul--2022
---

# Memory protection

## Memory Protection by hardware

[[Dual-mode operation]] to ensure that all [[Privileged instruction]] can only be run in [[Kernel mode]]

![[Pasted image 20220817213129.png]]

CPU also has 2 registers that determine the legal range of addresses program can access
- [[Relocation register|Base register]]
- [[Limit register]]

When [[User program]] wants to access some memory location, OS will load the base and limit register from main memory to CPU to perform a check. Since only the OS controls these register values, the load is done in [[Kernel mode]]. CPU will generate a trap if the check fail.

## Memory protection in [[Paging]]

Implementation by associating protection bits with each [[Page]].

1. Valid bit
    1. Indicate if page is in the process [[Logical address space]]
2. Read/write bit
    1. If page can be R/W
3. Execute bit
    1. If page can be executed

---
Links: 