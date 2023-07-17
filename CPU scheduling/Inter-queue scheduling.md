---
tags: 🌱
date: 03--Sep--2022
---

# Inter-queue scheduling

- Fixed priority scheduling
    - Queues are served in priority order
    - Suffers from [[Starvation]] for lower priority queues
- Time-slice based scheduling
    - Each queue gets a fixed time quantum on CPU (similar to [[Round robin|RR]] concept)
    - 80ms for foreground and 20ms for background

---
Links: 