---
tags:
  - 🌱
  - OS
  - ComputerScience
date: 17--Aug--2022
modified: 22--Oct--2023
---

# Interrupt driven data transfer

CPU is in-charge of managing the data in the buffer.

## Implementation
- CPU will issue an I/O command to the device controller
- For each byte of data, an [[Interrupt]] will be raised
- CPU will have to handle the interrupt and read from the device buffer

This is allows for fast response time by the CPU since each data byte raises an interrupt and is immediately handled compared to [[Direct memory access data transfer]].

---
Links: 