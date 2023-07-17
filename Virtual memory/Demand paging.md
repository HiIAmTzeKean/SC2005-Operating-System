---
tags: 🌱
date: 31--Jul--2022
---

# Demand paging

To bring in page into memory only when it is needed.

## Architecture

Hardware support uses [[Valid-invalid bit scheme]] in a [[Page table]]. [[Backing store]]/[[Swap device]] will hold pages that are not present in [[Main memory|Physical memory]]. The section of the storage that does this is known as [[Swap space]]

1. Valid indicates [[Page]] is legal and in memory
2. Invalid can indicate 2 scenarios
    1. Not legal (not in [[Logical address space]])
    2. Legal in [[Backing store]] but not loaded in [[Main memory|Physical memory]]

Access to invalid pages will cause a [[Page fault]]. Paging hardware will [[Trap]] the OS as [[Page]] is not in [[Main memory|Physical memory]].

## Performance

Let $p$ be probability of [[Page fault]] occurring, $0 \le p \le 1$. We note that typically memory access time is significantly less than [[Page fault time]].

[[Effective access time]] calculation will follow
$$EAT = (1-p) \times \text{memory access time} + p \times \text{page fault time}$$

## Advantage

1. Less [[Main memory|Physical memory]] used
    1. Pages which are least used store in [[Backing store]]

---
Links: 