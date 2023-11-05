---
tags:
  - 🌱
  - OS
  - ComputerScience 
date: 03--Sep--2022
---

# Multilevel queue scheduling

Since different [[Process]] have different [[Scheduling criteria]] goals, processes can be categorised into groups and placed into different queues.

## Implementation
Ready queue is partitioned into several queues. Each queue has its own [[Scheduling algorithm]]. [[Inter-queue scheduling]] is then used to schedule which queue to service.

## Example
- Foreground processes require fast [[Response time]] as it needs to handle I/O and interaction. ([[Round robin]] is optimal)
- Background processes need not be interactive and focuses on [[Throughput]]. [[First come first serve]] avoids excessive [[Context switch]] overhead.

---
Links: 