---
tags: 🌱
alias: RR
date: 04--Jul--2022
---

# Round robin

Similar to [[First come first serve|FCFS]] but [[Preemptive scheduling]] is added to enable the system to switch between processes.

## Implementation

Fixed **time quantum** for scheduling (q). Ready queue is treated like circular queue, and [[CPU scheduler]] go around ready queue and allocate CPU to each [[Process]] up to (q) time.

2 scenarios can occur

1. CPU burst of less than (q) and voluntarily releases
2. CPU burst is longer than (q)
    1. Cause an [[Interrupt]] to OS
    2. [[Context switch]] occurs
    3. Process added to tail of ready queue.

Properties

- Higher average waiting time than [[Shortest job first|SJF]] but better response time
- n processes in ready queue implies waiting time is no more than (n-1)q units
- Large q degenerates to [[First come first serve|FCFS]].
- Small q causes to many context switches, high overhead.
- Turn around time varies and no well-defined relationship
- Average CPU time remains fixed once q is larger than max CPU burst length

---
Links: 