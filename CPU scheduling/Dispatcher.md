---
tags: 🌱, OS
date: 08--Jul--2022
---

# Dispatcher

Gives control of the CPU core to the [[Process]] selected by the [[CPU scheduler]].

## Main function

- Switching context from processes
- Switching to [[User mode]]
- Jumping to location in [[User program]] to resume

## Dispatcher speed

Must be fast since it is invoked every context switch. The time taken to stop one process and to start running another is the [[Dispatch latency]]. 

## Visual summary

![[role of dispatcher.png]]

---
Links: 