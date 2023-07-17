---
tags: 🌱
date: 09--Jul--2022
---

# Critical section problem

For a system of $n$ [[Process]], each process will have a **segment of code** which **data is shared** called [[Critical section]].

## Necessary condition
- Critical section problem only exist if there is **at least 1 process writing** to the shared data
    - If all processes are only reading, then there is no issue
    - Data not changed -> data is still consistent
- The solution should satisfy [[Critical section solution criteria]]

## Protocol
Synchronise activity where each process must request permission to enter critical section. Each section will contain entry section, exit section, remainder section.
```C
while(1) {
    entrySection()
    citicalSection()
    exitSection()

    remainderSection()
}
```

## Single core environment
Prevent [[Interrupt]] when a shared variable is modified -> No [[Preemptive scheduling|Preemption]] such that there is no unexpected modification

## Multiprocessor environment
Disabling interrupts in [[Multithread]] environment time consuming and not efficient.

## Approach for OS
1. [[Preemptive kernel]] 
    1. More responsive since there is less risk for a process that will run for a long time
    2. Race condition downside
2. [[Non-preemptive kernel]]
    1. Free from race condition

---
Links: 