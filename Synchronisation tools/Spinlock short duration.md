---
tags:
  - 🌱
  - OS
  - ComputerScience 
date: 14--Jul--2022
---

# [[Spinlock]] short duration

Assume $t$ is the time taken for 1 context switch. 

Given a case where $P_0$ is in the critical section and $P_1$ is requesting to enter critical section. Since $P_0$ is in critical section, $P_1$ has to wait. Then, $P_1$ should be move to [[Waiting state]] and be restored to [[Running state]]. Since there are 2 context switches that are needed, the total time taken is $2t$.

Thus, if a local is to be held for less than $2t$, spinlocks should be used since the time difference allows the [[Process]] to complete some work.

---
Links: 