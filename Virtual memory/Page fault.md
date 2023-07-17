---
tags: 🌱
date: 31--Jul--2022
---

# Page fault

## Condition to occur

1. Access to [[Page]] that has not been loaded to [[Main memory|Physical memory]]
2. Access to page that is not within [[Program]] [[Logical address space]]

## Handling page fault

![[page fault handling.png]]

1. Check internal table in [[Process control block|PCB]] of process to determine if reference is valid -> within [[Logical address space]]
    1. Invalid reference will force OS to terminate [[Process]]
    2. OS will continue servicing if page is legal
2. Raise [[Trap]] to OS for page in
3. Locate free [[Frame]] in [[Free frame list]]
4. Schedule [[Backing store]] to read page into frame
5. When read is complete, modify internal table and [[Page table]] to indicate page is in [[Main memory|Physical memory]]
6. Restart instruction interrupted by [[Trap]]

Handling page fault requires 2 [[Context switch]] time and 1 [[Disk IO]] time -> [[Page fault time]]

## Handling page fault without free frame

The same step 1 is repeated, but since there is no free frame, [[Page replacement]] must occur.

---
Links: 