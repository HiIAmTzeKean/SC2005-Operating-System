---
tags:
  - 🌱
  - OS
  - ComputerScience 
date: 20--Oct--2022
---

# Page replacement

## Overhead management
Pages have a dirty bit that indicates if a page has been modified and should be written back to [[Backing store]].

## Replacement algorithm

- FIFO
    - Replace the page that has been in memory for the longest time
    - Suffers from [[Belady anomaly]]
- Optimal
    - Replaces the page that will not be used for the longest time
    - OS must search forward in reference string, which is not possible
    - Optimal algorithm is the most effective way of replacing pages
- LRU
    - Replaces the page that was least recently used
    - A counter field can be used to track the last used time, but there will be overhead of updating and checking incurs O(N)
    - Another way is to use a stack implementation. When page is referenced, it will be moved to top and bottom of stack is the LRU page. Cost to update is also costly, but not search time incurred
- Clock (psudo LRU)
    - Uses a reference bit to indicate if a page has been referenced after loading
    - Uses the idea from LRU, where bit indicates page has been used, but the bit is not able to store information of how many times page was used, nor when it was last used
    - Approximation of LRU allows it to perform near optimal

---
Links: 