---
tags:
  - 🌱
  - OS
  - ComputerScience
  - Thread
date: 03--Jul--2022
---

# Data parallelism

Distributing subset of the same data across computing cores and performing the same operation on each core.

![[Data parallelism.png]]

## Example

Given a problem where we need to sum elements in an array from 0 to N.

On a [[Single threaded]] system, a thread would sum each element till N.

On a [[Multithread]] system with 2 cores, thread 1 can sum from 0 to N/2 and thread 2 sums from N/2+1 to N. Where each [[Thread]] runs in [[Parallelism|parallel]] in separate cores.

> [!summary]
> Distribution of data across cores

---
Links: [[Parallelism]] - [[Multithread]]