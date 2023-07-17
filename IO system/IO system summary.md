---
tags: 🌱
date: 03--Nov--2022
---

# IO system summary

- System design objective
    - Efficiency
        - IO tend to be slow compared to [[Main memory]] and CPU
    - [[Generalisation]]
        - Treat all devices the same
        - Implements a linear structure. Device driver interact with device controller on IO device. Device driver interacts with kernel IO system, kernel issue generic instructions to device driver which specialises the instructions.

---
Links: 