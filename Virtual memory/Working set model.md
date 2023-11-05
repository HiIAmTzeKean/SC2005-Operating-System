---
tags:
  - 🌱
  - OS
  - ComputerScience 
date: 30--Oct--2022
---

# Working set model

Uses the last $\delta$ pages used by process as working set needed.

The strategy comes from principal of locality where a process is likely to access memory locations near each other. $\delta$ will be set for each process and OS will allocate the number of unique frames in the $\delta$ window to a process. If the total number of frames needed by all processes exceed the total number of frames, processes will be swapped out.

This frees up space for other processes to prevent trashing.

---
Links: 