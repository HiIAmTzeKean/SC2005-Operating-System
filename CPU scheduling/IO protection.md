---
tags:
  - 🌱
  - OS
  - ComputerScience 
date: 17--Aug--2022
---

# IO protection

Users can invoke illegal I/O operation such as illegal access to memory location. OS is designed to prevent user programs from directly accessing hardware.

## Access to hardware

[[User program]] can make [[System call]] to request for OS services to perform some hardware operation -> I/O instructions are privileged instruction.

CPU will generate [[Trap]] for I/O operations that try to bypass OS.

---
Links: 