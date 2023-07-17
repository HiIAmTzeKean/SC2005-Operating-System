---
tags: 🌱
alias: Preempted
date: 05--Jul--2022
---

# Preemptive scheduling

![[CPU Scheduling concept#Scheduling decision]]

CPU can be taken away from a running process **any time** by the [[CPU scheduler]] (which happens during some [[Interrupt]]).

## Conditions
We can check if scheduling is preemptive if a process is taken away from CPU in
- Case 3 (Another process given to CPU after some [[Interrupt]])
- Case 4 (waiting process added to ready queue and [[CPU scheduler]] is invoked)
- Case 1 (New process added to ready queue and [[CPU scheduler]] invoked)


## Advantage
- Responsive system

## Disadvantage
- [[Context switch]] overhead
- Cache misses from switching to other processes

---
Links: 