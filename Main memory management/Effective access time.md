---
tags:
  - 🌱
  - OS
  - ComputerScience 
alias: EAT
date: 25--Jul--2022
---

# Effective access time

Let [[Translation lookaside buffer|TLB]] lookup time be $\epsilon$ and memory cycle time be $\mu$. Hit ratio is the percentage of times page found in TLB as $\alpha$.

CPU will always check TLB first, and will incur $\epsilon$ cost. The CPU will also have to access main memory to obtain the data and incur $\mu$. At the minimum, the CPU will take $\mu + \epsilon$ time. If there is a TLB miss, then 
$$EAT = (\mu + \epsilon)\alpha + (2\mu + \epsilon)(1-\alpha)$$

---
Links: 