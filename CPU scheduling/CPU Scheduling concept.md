---
tags:
  - 🌱
  - OS
  - ComputerScience 
date: 05--Jul--2022
---

# [[CPU Scheduling]] concept

[[Multithread]] systems aim to maximise CPU utilization to have some [[Process]] running at all times. Several processes are kept in memory and CPU allocated by [[CPU scheduler]] based on the [[Process state]] which follows the [[CPU-IO burst cycle]]. 

## Types of process scheduler
 - [[Long-term scheduler]]
 - Medium-term scheduler
 - [[CPU scheduler|Short-term scheduler]]

## Scheduling decision

1. Process switch from [[New state]] to [[Ready state]]
2. Process switch from [[Running state]] to [[Waiting state]] (I/O request)
3. Process switch from [[Running state]] to [[Ready state]] (interrupt)
4. Process switch from [[Waiting state]] to [[Ready state]]
5. Process terminates

## 2 types of scheduling scheme

[[Preemptive scheduling]] and [[Non-preemptive scheduling]]

---
Links: [[Dispatcher]]