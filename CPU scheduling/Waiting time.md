---
tags: 🌱
date: 27--Aug--2022
---

# Waiting time

- Sum of periods spent in ready queue
    - Recall from [[Process state]] that process is definitely in idle when it is in [[Ready state]]
    - [[Process]] can also be idle when there are 2 process requesting I/O from the same [[Device controller]]. Then the latter process is also idle as no work is done for the process.
- Calculation formula is $\text{Wait time} = \text{Terminate time} - \text{CPU burst time} - \text{IO burst time} - \text{arrival time}$

---
Links: [[CPU burst]] - [[IO burst]]