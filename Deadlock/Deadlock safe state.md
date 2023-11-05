---
tags:
  - 🌱
  - OS
  - ComputerScience 
date: 19--Jul--2022
---

# Deadlock safe state

A state is safe if OS can allocate resources to each thread in some order and still avoid a deadlock (safe sequence).

## Safe sequence

Given set $\set{T_0,T_1,...}$, there exist a sequence where resources needed by $T_i$ can be satisfied by both
1. Available resources
2. Resources held by $T_j$ for each $j<i$

## Constraints satisfying safe sequence

1. If $T_i$ requires resources that are not immediately available, $T_i$ will wait for $T_j$ to terminate
2. When $T_j$ terminates, $T_i$ will obtain the resources and execute. Once $T_i$ terminates, it returns allocated resources
3. $T_{i+1}$ will obtain needed resources till all threads are completed


---
Links: [[Deadlock unsafe state]]