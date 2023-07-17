---
tags: 🌱
alias: SMP
date: 08--Jul--2022
---

# Symmetric multi-processing
Each processor is self-scheduling. [[CPU scheduler]] will run when a core becomes idle to allocate next process. Thus, the [[Scheduling algorithm]] applied for cores is said to be **symmetrical** across all cores.

## Advantage
- No core mapping problem compared to [[Asymmetric multi-processing]]

## Disadvantage
- Migration overhead
    - Process may migrate to other cores. there is a need to migrate private core-specific cache data which consumes time
- There needs to be synchronised clocks across cores
- Only **one** global algorithm for process selection across all cores
    - If the algorithm chosen is FCFS then there will be a single global ready queue, so all processes will suffer from the algorithm disadvantage

---
Links: 