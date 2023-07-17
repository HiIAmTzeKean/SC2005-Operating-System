---
tags: 🌱
date: 03--Jul--2022
---

# Amdahl's law

Formula for potential gains from adding computing cores to an application with serial and parallel components.

$$speedup \le \frac{1}{S + \frac{1-S}{N}}$$
As N approaches infinity, speedup converges to $\frac{1}{S}$, limiting the additional gain per core.

> [!summary]
> There is a disproportional effect on performance gain by adding more computing cores.  Less gains for each additional core.

---
Links: [[Thread]] - [[Multithread]]