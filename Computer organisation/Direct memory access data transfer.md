---
tags: 🌱
alias: DMA data transfer
date: 17--Aug--2022
---

# Direct memory access data transfer

Typically used in high speed I/O devices that can transmit at close to memory speed. CPU does not need to handle the transfer of data, allowing it to execute other programs.

## Implementation

1. OS set up buffer, pointers and counter
2. CPU issue block command to the main memory [[Device controller]]
3. The device controller will transfer blocks of data from the buffer directly to main memory without the need for CPU
4. An [[Interrupt]] generated **per block** transferred by the main memory device controller
5. CPU will read directly from [[Main memory]]

---
Links: 