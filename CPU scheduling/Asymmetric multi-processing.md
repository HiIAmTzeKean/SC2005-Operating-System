---
tags:
  - 🌱
  - OS
  - ComputerScience 
date: 08--Jul--2022
---

# Asymmetric multi-processing
Processes ae partitioned apriori (at [[Process creation]] time) to each core. Scheme is also known as **Partitioned scheduling**.

## Advantage
- [[Uniprocessor scheduling]] strategy can be used for scheduling
- Easy extension of [[Uniprocessor scheduling]] to multiprocessor scheduling

## Disadvantage
- Mapping of process to core is NP-hard problem -> knapsack problem
- Poor mapping causes uneven load allocation, one core can be idle while other is overloaded
- Similar issue to [[Shortest job first]], where heuristics needed to estimate [[CPU burst]] time

---
Links: 