---
tags:
  - 🌱
  - OS
  - ComputerScience 
date: 24--Jul--2022
---

# Paging

[[Physical address space]] divided into fixed sized blocks called [[Frame]] and [[Logical address space]] into same sized blocks called [[Page]].

## Advantage

There will be no [[External fragmentation]] since any free frame can be mapped to a page → [[Non-contiguous allocation]]

## Disadvantage

- Some [[Internal fragmentation]]. If a process loaded does not fill the whole frame, then there will be excess memory allocated.
- [[Address translation]] requires 2 memory access
    - Implementation of [[Translation lookaside buffer]] to reduce [[Effective access time]]

### Worst case scenario

Given a process that uses 1025 bytes and each frame and page is 1024 bytes. [[Process]] will need 1 page and 1 byte -> 2 pages. Thus, allocation of 2 frames, where the internal fragmentation is almost the whole frame

---
Links: 