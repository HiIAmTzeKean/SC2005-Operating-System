---
tags:
  - 🌱
  - OS
  - ComputerScience 
alias: Short-term scheduler
date: 05--Jul--2022
---

# CPU scheduler

Selects [[Process]] in memory that are in ready queue and allocates CPU to the process.

## Relation to [[Multiprogramming system]]
There is a timer inside the CPU where each process is given finite CPU time. On [[Timer interrupt]], the process is halted and placed in the ready queue. This allows OS to have CPU multiplexed between multiple process to maintain CPU utilisation through rounds of selection of process via [[Scheduling algorithm]].

## Types of [[CPU scheduler]]
1. [[Preemptive scheduling]]
2. [[Non-preemptive scheduling]]

---
Links: 