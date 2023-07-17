---
tags: 🌱
date: 24--Jul--2022
---

# Compaction

Shuffle memory contents to place all free memory together in one large block

## Disadvantages
1. Only possible if reallocation is dynamic -> [[Execution time address binding]]. 
    1. Relocation require moving program and data along with changing [[Relocation register|base register]] to reflect new [[Base address]].
2. System inefficiency during relocation
    1. CPU idle as time needed for process to be relocated
    2. Time is consumed by OS to move [[User program]] instead of useful computation

---
Links: 