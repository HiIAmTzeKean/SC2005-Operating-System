---
tags: 🌱
date: 18--Jul--2022
---

# Deadlock conditions

## Necessary conditions

1. Mutual exclusion
    - [[Resource instance]] must be in nonsharable mode. Only one [[Thread]] can access the instance, and every other request will be delayed till instance released
2. Hold and wait
    - Thread is holding one resource and waiting to acquire additional resource from another thread
3. No [[Preemptive scheduling]]
    - Resource cannot be preempted
    - Released only voluntarily by thread holding it after task completion
4. Circular wait
    - Exist a set $\set{T_0,T_1,...,T_n}$ such that $T_i$ is waiting for $T_{i+1}$ and that $T_n$ is waiting for $T_0$

## [[Deadlock detection]] through [[Resource graph allocation]]

![[Resource graph allocation#Conditions for deadlock]]

## [[Deadlock detection]] through [[Deadlock safe state]]

![[Deadlock avoidance#Deadlock problem condition]]

---
Links: 