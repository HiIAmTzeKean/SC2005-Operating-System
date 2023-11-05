---
tags:
  - 🌱
  - OS
  - ComputerScience 
alias: FCFS
date: 04--Jul--2022
---

# First come first serve

CPU serves the [[Process]] in the order that it arrives.

## Properties
- [[Non-preemptive scheduling]]
    - Since process must voluntarily release CPU
- Implementation via FIFO queue
    - [[Process control block|PCB]] linked to tail of ready queue, and CPU is allocated to head of queue.

## Advantage
- Code is simple to write and understand
- Maximising [[Maximum CPU utilisation]] since low overhead from [[Context switch]]

## Disadvantage
- Average [[Waiting time]] under FCFS is not consistent
    - Waiting time depends on which process arrives first
- Convoy effect
    - Short processes suffer long waiting time from long processes. 
- Not suitable for interactive systems due to low [[Response time]]


---
Links: 