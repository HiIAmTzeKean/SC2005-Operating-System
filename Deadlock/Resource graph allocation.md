---
tags:
  - 🌱
  - OS
  - ComputerScience 
date: 18--Jul--2022
---

# Resource graph allocation

Deadlocks can be described using a directed graph.

Vertices are partitioned into 2 types of od nodes. Active [[Thread]]  $T=\set{T_1,T_2,...}$  and resources $R=\set{R_1,R_2,...}$

1. Directed edge from thread to resource (**Request edge**)
    1. $T_i \rightarrow R_i$
    2. Indicates thread is requesting for [[Resource instance]]
2. Direct edge from resource to thread (**assignment edge**)
    1. $R_i \rightarrow T_i$
    2. Indicates resource assigned to thread


## Conditions for deadlock

1. Graph has no cycles
    1. No deadlock
2. Graph has cycles and 1 instance available per resource
    1. Deadlock will occur
3. Graph has cycles and several instances available per resource
    1. Deadlock possibility
    2. If there is a deadlock, there might exist a solution to rectify

## Examples


---
Links: 