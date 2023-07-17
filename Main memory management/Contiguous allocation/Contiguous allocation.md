---
tags: 🌱
date: 23--Jul--2022
---

# Contiguous allocation

[[Main memory|Physical memory]] divided into partitions and OS resides in first partition while other partitions store [[User program|User process]]. 2 types of partitioning scheme [[Fixed partitioning]] and [[Dynamic partitioning]].

## Architecture

Memory is allocated in contiguous partitions for [[Process]]

1. [[Relocation register]] and [[Limit register]] used to determine the partition at runtime
    1. Relocation register contains value of smallest physical address
    2. Limit register contains range of [[Logical address]] -> logical address must be less than limit register
2. OS has its own partition
    1. Maintains information of allocated partitions
    2. Tracks free partitions (holes)
3. When a process arrives it is allocated memory from a block of memory large enough to accommodate it → [[Dynamic allocation solutions]]
    1. Process must be contiguously allocated and cannot overlap

---
Links: 