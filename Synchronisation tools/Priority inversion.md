---
tags:
  - 🌱
  - OS
  - ComputerScience 
date: 16--Jul--2022
---

# Priority inversion

Occurs during [[CPU Scheduling concept]] when higher priority process needs to modify kernel data accessed by lower priority process.

## [[Liveness failure]] failure priority inversion

Given 3 processes - L, M, H whose priorities are L<M<H. Then, if H requires [[Semaphore]] S which is accessed by L, H will have to wait. If M were to execute and [[Preemptive scheduling]] L, then a lower priority M has affected the wait time of a higher priority H.

> [!important]
> Situation only occurs in systems where there are more than 2 priorities.

## Solution

[[Priority inheritance protocol]] can be used. Where L will inherit H priority, preventing M from preempting its execution. When L is done with S, it will relinquish its inherited priority and S will be contended by H and M.

---
Links: 