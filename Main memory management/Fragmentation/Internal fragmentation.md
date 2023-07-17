---
tags: 🌱
date: 24--Jul--2022
---

# Internal [[Fragmentation]]

> [!summary]
> Memory wastage from unused allocation due to size of process being smaller than partition

When OS allocates memory to [[Process]], there is overhead to keep track of holes especially when the hole is small. OS typically breaks down [[Main memory|Physical memory]] into fixed size blocks and allocate memory based on block size. Thus, **memory allocated** to [[Process]] may be slightly **larger** than **requested** memory.

---
Links: 