---
tags: 🌱
date: 11--Aug--2022
---

# System call

> [!Summary]
> When a non-privileged user program request services of OS, it will invoke system call to to request [[Kernel system]] to do some privileged task.

Provides a way for [[User program]] to interface with [[Kernel system]] in OS. Typically, user programs do not directly access system calls, but does it thorough an [[SC2005 Operating system/CPU scheduling/Application programming interface|API]].

System calls are typically written in assembly language or C.

## How system call work

![[System call interface.png]]

When a user program invokes a system call, the CPU will switch from [[User mode]] to [[Kernel mode]]. The switch will cause the the CPU to [[Trap]] to the OS, allowing the [[Trap handler]] to service the request.

## Concept

[[User program]] run in the [[User space]]. A system call is connected to the [[Kernel system]] which executes in the [[Kernel space]].

Architecture is to maintain [[Memory protection]] through [[Dual-mode operation]] where the computer has to switch between [[User mode]] and [[Kernel mode]].

### Example

When the user is running a [[User program]] such as a text editor and now requires data from [[Kernel memory]] or a new hardware resource. The program will request the help of the OS by executing system call. Through the system call, the program will switch to the kernel mode and access the hardware resources. Once the process is done, it will switch back to user mode.

## When is system call used

- Process control
- File management
- Accessing I/O devices
- Creating and managing new processes

---
Links: 