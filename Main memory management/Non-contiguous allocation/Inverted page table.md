---
tags: 🌱
date: 27--Jul--2022
---

# Inverted page table

Each [[Process]] usually associated with [[Page table]]. For a system with many processes, a lot of memory usage to store the page tables.

## Concept

![[Pasted image 20220727171054.png]]
Inverted page table is sorted by [[Frame]] instead of [[Page]]. Thus, total number of entries would be amount of [[Main memory]] available.

## Advantage

1. Decreases the memory needed to store the page tables for processes

## Disadvantage

1. Longer search time since lookup is on [[Logical address]]
    1. Worst case is whole table must be search to determine if logical address is valid
2. [[Shared memory]] issue
    1. Cannot have [[Shared pages]] since each frame can only be mapped to one [[Logical address|Virtual address]]

---
Links: 