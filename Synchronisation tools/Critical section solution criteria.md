---
tags:
  - 🌱
  - OS
  - ComputerScience 
date: 09--Jul--2022
---

# Critical section solution criteria
Assumption that each [[Process]] is executing at **non-zero speed**. We do not guarantee any form of speed, but we guarantee process completion in critical section.

## Mutual exclusion
- When a process is in critical section, no other process can execute in critical section

## Progress
- If no process in critical section, and some process request entry to their critical section
- Then the selection of the next process to enter the [[Critical section]] cannot be postponed indefinitely

## Bounded waiting
- After a process request entry to critical section and before the request has been granted, there is a bound on number of times other processes are allowed to enter critical section

---
Links: [[Critical section]] - [[Critical section problem]]