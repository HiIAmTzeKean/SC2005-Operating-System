---
tags:
  - 🌱
  - OS
  - ComputerScience 
date: 24--Jul--2022
---

# External [[Fragmentation]]

As [[Process]] is loaded and removed from memory, free memory space broken into little pieces. External fragmentation exist when there is **enough total memory** space to satisfy a **request** by available spaces are **not contiguous**. A result of storage being fragmented into large number of small holes.

[[First-fit]] and [[Best fit]] from [[Contiguous allocation]] suffers from this issue.

## Solution

1. [[Compaction]] can be used if relocation is dynamic
2. [[Paging]] can be used if non-contiguous allocation is permitted

---
Links: 