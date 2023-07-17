---
tags: 🌱
alias: PCB
date: 08--Jul--2022
---

# Process control block

Each [[Process]] represented by a PCB (also called task control block). PCB are located in [[Kernel space]] and only accessible by the OS.

## Constituents

![[pcb.png]]

Containing information about the process such as

- [[Process state]]
- Program counter
- CPU registers
- [[CPU Scheduling]] information
    - Process priority, pointer to scheduling queues
- Memory management information
    - Base and limit registers
- Accounting information
    - Amount of CPU and real time used, time limits
- I/O status information
    - List of devices allocated to process

---
Links: 