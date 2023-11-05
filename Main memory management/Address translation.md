---
tags:
  - 🌱
  - OS
  - ComputerScience 
date: 24--Jul--2022
---

# Address translation

[[Logical address]] sent to CPU is divided into 2 components

## Hardware support

- [[Page]] number (*p*)
    - [[Main memory unit|MMU]] will handle the translation of page number
    - Extracts page number and use it as index for [[Page table]]
    - Obtain fame number (*f*) from [[Page table]]
    - Replace *p* with *f*
- Page offset (*d*)
    - Combined with [[Base address]] to define [[Physical address]]

## Procedure

1. Index into page table in memory using the [[Page table base register|PTBR]] to obtain frame number 
2. Access location in memory with frame number and offset

![[paging hardware.png]]

---
Links: 