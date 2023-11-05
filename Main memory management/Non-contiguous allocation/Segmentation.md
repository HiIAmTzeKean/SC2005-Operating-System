---
tags:
  - 🌱
  - OS
  - ComputerScience 
date: 30--Jul--2022
---

# Segmentation

[[Program]] is a collection of segments. Segments are logical units such as code, stack and heap.

![[segmentation layout.png]]

## Advantage

1. Memory management that support [[User view]]
    1. Unlike [[Paging]] which
2. Each segment can grow and protected independently
3. [[Segmentation sharing]] is independent
4. Avoid [[Internal fragmentation]]

## Disadvantage

1. [[External fragmentation]]

## Architecture

1. [[Logical address]] consists of
    1. Segment number
    2. Offset
2. [[Segment table]]
3. [[Segment table base register]]
    1. [[Relocation register|Base register]] concept. Points to [[Segment table]] location.
4. [[Segment table length register]]

---
Links: 